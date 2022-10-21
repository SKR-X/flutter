import 'package:flutter/material.dart';
import 'package:flutter/src/widgets/container.dart';
import 'package:flutter/src/widgets/framework.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: AuthWidget(),
      theme: ThemeData(
          appBarTheme:
              AppBarTheme(backgroundColor: Color.fromRGBO(3, 37, 65, 1))),
    );
  }
}

class AuthWidget extends StatefulWidget {
  const AuthWidget({super.key});

  @override
  State<AuthWidget> createState() => _AuthWidgetState();
}

class _AuthWidgetState extends State<AuthWidget> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        centerTitle: true,
        title: Text("Login to your account"),
      ),
      body: 
      ListView(
        children: [
          SizedBox(
            height: 20,
          ),
          _FormWidget(),
          SizedBox(
            height: 25,
          ),
          _HeaderWidget(),
        ],
      ),
    );
  }
}

class _HeaderWidget extends StatelessWidget {
  const _HeaderWidget({super.key});

  final textStyle = const TextStyle(fontSize: 16, color: Colors.black);

  @override
  Widget build(BuildContext context) {
    return Padding(
      padding: EdgeInsets.symmetric(horizontal: 10.0),
      child: Column(
        children: [
          Text(
              'In order to use the editing and rating capabilities of TMDB, as well as get personal recommendations you will need to login to your account. If you do not have an account, registering for an account is free and simple. Click here to get started.',
              style: textStyle),
          SizedBox(
            height: 25,
          ),
          Text(
              'If you signed up but didn\'t get your verification email, click here to have it resent.',
              style: textStyle)
        ],
      ),
    );
  }
}

class _FormWidget extends StatefulWidget {
  const _FormWidget({super.key});

  @override
  State<_FormWidget> createState() => __FormWidgetState();
}

class __FormWidgetState extends State<_FormWidget> {
  final textStyle = const TextStyle(fontSize: 16, color: Color(0xFF212529));

  final inputDerorator = const InputDecoration(
      border: OutlineInputBorder(),
      isCollapsed: true,
      contentPadding: EdgeInsets.symmetric(horizontal: 10, vertical: 10));

  final color = const Color(0xFF01B4E4);

  final _loginTextController = TextEditingController();
  final _passwordTextController = TextEditingController();
  String? alert = null;

  void _auth() {
    final login = _loginTextController.text;
    final password = _passwordTextController.text;
    if (login == "admin" && password == "pass") {
      alert = null;
    } else {
      alert = "Ошибка!";
    }
    setState(() {
      
    });
  }

  void _resetPassword() {
    print('object');
  }

  @override
  Widget build(BuildContext context) {
            final alertText = this.alert;
    return Padding(
      padding: const EdgeInsets.symmetric(horizontal: 10.0),
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          if (alertText != null) Text(alertText),
          Text(
            'Username',
            style: textStyle,
          ),
          SizedBox(
            height: 5,
          ),
          TextField(
            controller: _loginTextController,
            decoration: inputDerorator,
          ),
          SizedBox(
            height: 20,
          ),
          Text(
            'Password',
            style: textStyle,
          ),
          SizedBox(
            height: 5,
          ),
          TextField(
            controller: _passwordTextController,
            decoration: inputDerorator,
          ),
          SizedBox(height: 20,),
          Row(
            children: [
              TextButton(
                onPressed: _auth,
                child: Text('Login'),
                style: ButtonStyle(
                    padding: MaterialStateProperty.all(
                        EdgeInsets.symmetric(horizontal: 30)),
                    backgroundColor: MaterialStateProperty.all(color),
                    foregroundColor: MaterialStateProperty.all(Colors.white)),
              ),
              SizedBox(width: 20,),
              TextButton(onPressed: _resetPassword, child: Text('Reset Password'))
            ],
          )
        ],
      ),
    );
  }
}
