= README for rtmilk =
rtmilk is a [Remember the Milk](http://www.rememberthemilk.com/) wrapper library.

# Usages #
The followings are usage examples for each API method.

## tasks ##
note: variable "task" refers to an instance of "RTM::Task".

### rtm.tasks.getList ###
    RTM::Task.find_all({:list => "listid"})
    RTM::Task.find_all({:list => "listid", :name => "TestTask"})
    RTM::Task.find_all({:list => nil, :filter => 'name:TestTask'})
    RTM::Task.find_all({:list => nil, :filter => 'completedAfter:5/18/2012 completedBefore:5/20/2012'})

### rtm.tasks.add
    RTM::Task.new({:name => "TestTask"})

### rtm.tasks.delete ###
    task.delete

### rtm.tasks.complete ###
    task.complete

### rtm.tasks.uncomplete ###
    task.uncomplete

### rtm.tasks.setDueDate ###
    task.set_due_date('2012-12-12')
    task.set_due_date('2012-12-11T17:00:00Z', "1")
    task.set_due_date  # remove due date

### rtm.tasks.addTags ###
    task.add_tags("test_tag")
    task.add_tags("test_tag1,test_tag2")

### rtm.tasks.removeTags ###
    task.remove_tags("test_tag1")

### rtm.tasks.removeTags ###
    task.set_tags("test_tag1,test_tag2")
