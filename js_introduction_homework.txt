Man = function()
{
  this.name = "";
  this.age = 0;
  this.live = function()
  {
     console.log("Man lives");
  }
}

Student = function()
{
  Man.call(this);
  this.study = function()
  {
    console.log("Student studies");
  }
}

duckType = function(argument)
{
  if(argument.hasOwnProperty('study'))
    {
      console.log("It is a student");
    }
  else if(argument.hasOwnProperty('name') && argument.hasOwnProperty('age')
     && argument.hasOwnProperty('live'))
    {
      console.log("It is a man");
    }
  else 
    {
      console.log("It is not a man nor a student");
    } 
}

var student = new Student();
duckType(student);

var man = new Man();
duckType(man);