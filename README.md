//////////////////////////////////////////////////////////////////////
///  Basic Screen Navigation, Author: Chuck Bagby, MIT License     ///
//////////////////////////////////////////////////////////////////////
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: FirstScreen(),
    );
  }
}

//////////////////////////////////////////////////////////////////////
// FirstScreen - This would typically be in another code file      ///
//////////////////////////////////////////////////////////////////////
class FirstScreen extends StatelessWidget {
 TextEditingController nameController = TextEditingController();
  TextEditingController passwordController = TextEditingController();

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.blue,
      appBar: AppBar(
        title: Text('HR CONTROL'),
        backgroundColor: Colors.black,
      ),
      body: Padding(
        padding: EdgeInsets.all(50),
        child: Column(
          children: <Widget>[
             Image.network(
  'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQdlfYhSS92m1xLE0jecL77o7GkhFOvFWkjbA&usqp=CAU',
),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                controller: nameController,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'User Name',
                ),
              ),
            ),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                obscureText: true,
                controller: passwordController,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'Password',
                ),
              ),
            ),
            RaisedButton(
            child: Text('summite'),
            onPressed: () {
              if(nameController.text=="pentoz"&&passwordController.text=="123")
              {
                 Navigator.push(context,
                  MaterialPageRoute(builder: (context) => SecondScreen()));
              }
              else
              {
                print('wrong');
              }
             
            },
          ),
          ],
        )
      )
    );
  }
}

//////////////////////////////////////////////////////////////////////
// SecondScreen - This would typically be in another code file     ///
//////////////////////////////////////////////////////////////////////
class SecondScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Container(
      color: Colors.blue,
      child: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: <Widget>[
           Image.network(
  'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQdlfYhSS92m1xLE0jecL77o7GkhFOvFWkjbA&usqp=CAU',
),
          Text('control panel', style: Theme.of(context).textTheme.headline4),
          RaisedButton(
            child: Text('OD'),
            onPressed: () {
              Navigator.push(context,
                  MaterialPageRoute(builder: (context) => ThirdScreen()));
            },
          ),
           RaisedButton(
            child: Text('leave'),
            onPressed: () {
              Navigator.push(context,
                  MaterialPageRoute(builder: (context) => lev()));
            },
          ),
           RaisedButton(
            child: Text('update'),
            onPressed: () {
              Navigator.push(context,
                  MaterialPageRoute(builder: (context) => upd()));
            },
          ),
           RaisedButton(
            child: Text('attdeance'),
            onPressed: () {
              Navigator.push(context,
                  MaterialPageRoute(builder: (context) => att()));
            },
          ),
          SizedBox(height: 10.0),
          RaisedButton(
            child: Text('back'),
            color:Colors.blue,
            onPressed: () {
              Navigator.pop(context);
            },
          ),
        ],
      ),
    );
  }
}

//////////////////////////////////////////////////////////////////////
// ThirdScreen - This would typically be in another code file      ///
//////////////////////////////////////////////////////////////////////

class ThirdScreen extends StatelessWidget {
   TextEditingController nameController = TextEditingController();
  TextEditingController passwordController = TextEditingController();
  TextEditingController date = TextEditingController();
  
  

  @override
  Widget build(BuildContext context) {
    return Scaffold(
       backgroundColor: Colors.blue,
      appBar: AppBar(
        title: Text('od form'),
      backgroundColor: Colors.black,
      ),
      body: Padding(
        
        padding: EdgeInsets.all(10),
        child: Column(
          children: <Widget>[
             Image.network(
  'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRc4KXKOUGiYT3l3MzeZz0MbLm9k4QK76-daQ&usqp=CAU',
),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                controller: nameController,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'company name',
                 
                ),
              ),
            ),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                
                controller: date,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'work purpose',
                ),
              ),
            ),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                
                controller: passwordController,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'no of days',
                ),
              ),
            ),
            RaisedButton(
              textColor: Colors.black,
              color: Colors.white,
              child: Text('Login'),
              onPressed: (){
               
                  print('company name :${nameController.text}');
                print('work purpose :${date.text}');
                print('no of days :${passwordController.text}');
               
                  
               
              },
            )
          ],
        )
        
      )
       
    );
  }
}
class lev extends StatelessWidget {
  TextEditingController nameController = TextEditingController();
  TextEditingController passwordController = TextEditingController();
  TextEditingController date = TextEditingController();
  
  

  @override
  Widget build(BuildContext context) {
    return Scaffold(
       backgroundColor: Colors.blue,
      appBar: AppBar(
        title: Text('leave letter'),
         backgroundColor: Colors.black,
      ),
      body: Padding(
        padding: EdgeInsets.all(10),
        child: Column(
          children: <Widget>[
             Image.network(
  'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRc4KXKOUGiYT3l3MzeZz0MbLm9k4QK76-daQ&usqp=CAU',
),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                controller: nameController,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'Resion',
                ),
              ),
            ),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                
                controller: date,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'data in this month',
                ),
              ),
            ),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                
                controller: passwordController,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  labelText: 'no of days',
                ),
              ),
            ),
            RaisedButton(
              textColor: Colors.white,
              color: Colors.blue,
              child: Text('Login'),
              onPressed: (){
               
                  print('your resion is :${nameController.text}');
                print('we are permitted you upto ${passwordController.text+date.text}');
               
                  
               
              },
            )
          ],
        )
      )
    );
  }
}
class upd extends StatelessWidget {
 TextEditingController nameController = TextEditingController();
  
  TextEditingController date = TextEditingController();
  
  

  @override
  Widget build(BuildContext context) {
    return Scaffold(
       backgroundColor: Colors.blue,
      appBar: AppBar(
        title: Text('updata form'),
        backgroundColor: Colors.black,
      ),
      body: Padding(
        padding: EdgeInsets.all(10),
        child: Column(
          children: <Widget>[
             Image.network(
  'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRc4KXKOUGiYT3l3MzeZz0MbLm9k4QK76-daQ&usqp=CAU',
),
             Text('form 9:00am to 1:00pm'),
            Padding(
              padding: EdgeInsets.all(10),
              
              child: TextField(
                controller: nameController,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  
                ),
              ),
            ),
           Text('form 1:30pm to 5:00pm'),
            Padding(
              padding: EdgeInsets.all(10),
              child: TextField(
                
                controller: date,
                decoration: InputDecoration(
                  border: OutlineInputBorder(),
                  
                ),
              ),
            ),
           
            RaisedButton(
              textColor: Colors.white,
              color: Colors.blue,
              child: Text('sumite'),
              onPressed: (){
               
                  print('form 9:00am to 1:00pm :${nameController.text}');
                print('form 1:30pm to 5:00pm :${date.text}');
               
               
                  
               
              },
            )
          ],
        )
      )
    );
  }
}
class att extends StatelessWidget {
 
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.blue,
      appBar: AppBar(
        title: Text('attendance form'),
         backgroundColor: Colors.black,
      ),
      body: Padding(
        padding: EdgeInsets.all(10),
        child: Column(
          children: <Widget>[
                         Image.network(
  'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRc4KXKOUGiYT3l3MzeZz0MbLm9k4QK76-daQ&usqp=CAU',
),
             
          Text('click this button for summite your attendance'),
           
            RaisedButton(
              textColor: Colors.white,
              color: Colors.blue,
              child: Text('sumite'),
              onPressed: (){
               print('you attendance was updated');
                  
               
               
                  
               
              },
            )
          ],
        )
      )
    );
  }
}


