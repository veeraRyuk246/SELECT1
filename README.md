# SELECT1
import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(
  home: SubjectChooser(),
  debugShowCheckedModeBanner: false,
));

class SubjectChooser extends StatefulWidget {
  @override
  _SubjectChooserState createState() => _SubjectChooserState();
}

class _SubjectChooserState extends State<SubjectChooser> {
  String subject = '';

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Choose Subject for Elective'),
        backgroundColor: Colors.green,
      ),
      body: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          ListTile(
            title: Text('Data Science'),
            leading: Radio(
              value: 'Data Science',
              groupValue: subject,
              onChanged: (val) {
                setState(() => subject = val!);
              },
            ),
          ),
          ListTile(
            title: Text('Networking'),
            leading: Radio(
              value: 'Networking',
              groupValue: subject,
              onChanged: (val) {
                setState(() => subject = val!);
              },
            ),
          ),
          ListTile(
            title: Text('MAD'),
            leading: Radio(
              value: 'MAD',
              groupValue: subject,
              onChanged: (val) {
                setState(() => subject = val!);
              },
            ),
          ),
          ListTile(
            title: Text('IOT'),
            leading: Radio(
              value: 'IOT',
              groupValue: subject,
              onChanged: (val) {
                setState(() => subject = val!);
              },
            ),
          ),
          SizedBox(height: 20),
          Text('Selected: $subject', style: TextStyle(fontSize: 18)),
        ],
      ),
    );
  }
}
