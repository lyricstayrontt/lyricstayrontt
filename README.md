import 'package:flutter/material.dart';

void main() {
  runApp(RitmixApp());
}

class RitmixApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      theme: ThemeData.dark(),
      home: ProfileScreen(),
    );
  }
}

class ProfileScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Profil"),
        backgroundColor: Colors.black,
      ),
      body: Column(
        children: [
          SizedBox(height: 20),
          CircleAvatar(
            radius: 50,
            backgroundImage: NetworkImage("https://via.placeholder.com/100"), // Kullanıcı fotoğrafı
          ),
          SizedBox(height: 10),
          Text("Kullanıcı Adı", style: TextStyle(fontSize: 24, fontWeight: FontWeight.bold)),
          SizedBox(height: 10),
          Text("Takip Edilen Sanatçılar: 10", style: TextStyle(fontSize: 18, color: Colors.grey)),
          SizedBox(height: 20),
          Expanded(
            child: ListView(
              children: [
                ListTile(
                  leading: Icon(Icons.history),
                  title: Text("Dinleme Geçmişi"),
                  onTap: () {},
                ),
                ListTile(
                  leading: Icon(Icons.favorite),
                  title: Text("Favori Şarkılar"),
                  onTap: () {},
                ),
              ],
            ),
          ),
        ],
      ),
    );
  }
}
