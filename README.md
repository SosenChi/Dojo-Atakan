# Ai Sensei Atakan
// Karate Eğitim Uygulaması - Mobil Arayüz (React Native / Expo uyumlu örnek)

import React from 'react'; import { ScrollView, View, Text, TouchableOpacity } from 'react-native'; import { SafeAreaView } from 'react-native-safe-area-context'; import { Ionicons } from '@expo/vector-icons';

export default function HomeScreen() { const modules = [ { title: '🥋 El Kitabı', description: 'Temel teknikler, duruşlar ve açıklamalar' }, { title: '📘 Sözlük', description: 'Karate terimleri ve anlamları' }, { title: '🗓️ Ajanda', description: 'Antrenman planı, hedefler ve sınavlar' }, { title: '👨‍🏫 Antrenör Paneli', description: 'Öğrenci yönetimi, sınav kayıtları' }, { title: '🤖 Sensei ile Konuş', description: 'Yapay zeka destekli danışmanlık' }, ];

return ( <SafeAreaView style={{ flex: 1, backgroundColor: '#fff' }}> <ScrollView contentContainerStyle={{ padding: 20 }}> <Text style={{ fontSize: 26, fontWeight: 'bold', marginBottom: 20 }}> Karate Dijital Sensei </Text>

{modules.map((mod, index) => (
      <TouchableOpacity
        key={index}
        style={{
          backgroundColor: '#f5f5f5',
          padding: 20,
          borderRadius: 16,
          marginBottom: 16,
          shadowColor: '#000',
          shadowOffset: { width: 0, height: 2 },
          shadowOpacity: 0.1,
          shadowRadius: 4,
          elevation: 2,
        }}>
        <Text style={{ fontSize: 20, fontWeight: '600' }}>{mod.title}</Text>
        <Text style={{ color: '#555', marginTop: 4 }}>{mod.description}</Text>
      </TouchableOpacity>
    ))}

    <View style={{ marginTop: 40, alignItems: 'center' }}>
      <Ionicons name="logo-karate" size={40} color="#333" />
      <Text style={{ marginTop: 8, color: '#999' }}>
        Türk Karatesi Dijital Rehber v1.0
      </Text>
    </View>
  </ScrollView>
</SafeAreaView>

); }



