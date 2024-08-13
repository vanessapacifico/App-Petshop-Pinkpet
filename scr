import React, { useState } from 'react';
import { View, Text, Button } from 'react-native';
import { Calendar } from 'react-native-calendars';
import { Picker } from '@react-native-picker/picker';

const AgendamentoScreen = () => {
  const [selectedDate, setSelectedDate] = useState(new Date());
  const [selectedService, setSelectedService] = useState('');
  const [selectedProfessional, setSelectedProfessional] = useState('');
  const [selectedTime, setSelectedTime] = useState('');

  const services = ['Banho', 'Tosa', 'Consulta'];
  const professionals = ['João', 'Maria', 'Pedro'];
  const availableTimes = ['9:00', '10:00', '11:00']; // Exemplo de horários disponíveis

  const onDayPress = (day) => {
    setSelectedDate(day);
  };

  return (
    <View>
      <Calendar
        onDayPress={onDayPress}
        markedDates={{ [selectedDate.toString()]: { selected: true } }}
      />
      <Picker
        selectedValue={selectedService}
        onValueChange={(itemValue, itemIndex) =>
          setSelectedService(itemValue)
        }
      >
        {services.map((item, index) => (
          <Picker.Item label={item} value={item} key={index} />
        ))}
      </Picker>
      {/* Similar para o picker de profissionais */}
      <Picker
        selectedValue={selectedTime}
        onValueChange={(itemValue, itemIndex) =>
          setSelectedTime(itemValue)
        }
      >
        {availableTimes.map((item, index) => (
          <Picker.Item label={item} value={item} key={index} />
        ))}
      </Picker>
      <Button title="Agendar" onPress={() => console.log('Agendando...')} />
    </View>
  );
};

export default AgendamentoScreen;
