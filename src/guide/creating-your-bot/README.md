const app = express();
app.use(express.json());

const accountSid = 'TU_ACCOUNT_SID';
const authToken = 'TU_AUTH_TOKEN';
const client = new twilio(accountSid, authToken);

app.post('/whatsapp', (req, res) => {
  const message = req.body.message;
  const groupId = req.body.groupId;
  const participants = req.body.participants;

  if (message.startsWith('/integrantes')) {
    const integrantes = participants.map((participant) => @${participant.name}).join(', ');
    client.messages
      .create({
        from: 'whatsapp:const express = require('express');
const twilio = require('twilio');

const app = express();
app.use(express.json());

const accountSid = 'TU_ACCOUNT_SID';
const authToken = 'TU_AUTH_TOKEN';
const client = new twilio(accountSid, authToken);

app.post('/whatsapp', (req, res) => {
  const message = req.body.message;
  const groupId = req.body.groupId;
  const participants = req.body.participants;

  if (message.startsWith('/integrantes')) {
    const integrantes = participants.map((participant) => @${participant.name}).join(', ');
    client.messages
      .create({
        from: 'whatsapp:+17253100591',
        to: groupId,
        body: Integrantes del grupo: ${integrantes},
      })
      .done();
  } else if (message.startsWith('/Eliminar')) {
    const participantesAEliminar = message.split(' ').slice(1);
    participantesAEliminar.forEach((participante) => {
      const participant = participants.find((p) => p.name === participante);
      if (participant) {
        client.messages
          .create({
            from: 'whatsapp:TU_NUMERO_DE_TELEFONO',
            to: groupId,
            body: Eliminando a @${participant.name} del grupo...,
          })
          .done();
        // Aquí debes implementar la lógica para eliminar al participante del grupo
      }
    });
  }

  res.status(200).send('OK');
});

app.listen(3000, () => {
  console.log('Servidor escuchando en el puerto 3000');',
        to: groupId,
        body: Integrantes del grupo: ${integrantes},
      })
      .done();
  } else if (message.startsWith('/Eliminar')) {
    const participantesAEliminar = message.split(' ').slice(1);
    participantesAEliminar.forEach((participante) => {
      const participant = participants.find((p) => p.name === participante);
      if (participant) {
        client.messages
          .create({
            from: 'whatsapp:TU_NUMERO_DE_TELEFONO',
            to: groupId,
            body: Eliminando a @${participant.name} del grupo...,
          })
          .done();
        // Aquí debes implementar la lógica para eliminar al participante del grupo
      }
    });
  }

  res.status(200).send('OK');
});

app.listen(3000, () => {
  console.log('Servidor escuchando en el puerto 3000');
});
