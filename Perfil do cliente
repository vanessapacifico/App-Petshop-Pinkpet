import React, { useState, useEffect } from 'react';
import { View, Text, FlatList, Button } from 'react-native';

const PerfilScreen = () => {
  const [usuario, setUsuario] = useState({
    nome: 'João Silva',
    email: 'joaosilva@email.com',
    telefone: '(11) 98765-4321',
    animais: [
      { nome: 'Rex', raca: 'Labrador', dataNascimento: '01/01/2020' },
      { nome: 'Nina', raca: 'Poodle', dataNascimento: '15/03/2022' },
    ],
    agendamentos: [
      // ... dados dos agendamentos
    ],
  });

  return (
    <View>
      <Text>Perfil</Text>
      <Text>Nome: {usuario.nome}</Text>
      <Text>Email: {usuario.email}</Text>
      <Text>Telefone: {usuario.telefone}</Text>

      <Text>Animais Cadastrados:</Text>
      <FlatList
        data={usuario.animais}
        renderItem={({ item }) => (
          <View>
            <Text>{item.nome} - {item.raca}</Text>
          </View>
        )}
      />

      <Text>Histórico de Agendamentos:</Text>
      <FlatList
        data={usuario.agendamentos}
        renderItem={({ item }) => (
          <View>
            <Text>{item.servico} - {item.data}</Text>
          </View>
        )}
      />

      <Button title="Editar Perfil" onPress={() => console.log('Editar perfil')} />
    </View>
  );
};

export default PerfilScreen;
