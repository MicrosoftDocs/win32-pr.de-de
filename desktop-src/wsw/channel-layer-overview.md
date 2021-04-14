---
title: Übersicht über die Kanal Schicht
description: Die Kanal Schicht stellt eine Abstraktion des Transport Kanals und der Nachrichten bereit, die auf dem Kanal gesendet werden.
ms.assetid: d7dddcc6-8eb0-4ee6-8cf5-7701a2be7a19
keywords:
- Übersicht über die Kanal Schicht Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e52c4844bee472d4d22df7681fece16330f30cf
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104552923"
---
# <a name="channel-layer-overview"></a>Übersicht über die Kanal Schicht

Die Kanal Schicht stellt eine Abstraktion des Transport Kanals und der Nachrichten bereit, die auf dem Kanal gesendet werden. Sie enthält auch Funktionen für die Serialisierung von C-Datentypen in und aus SOAP-Strukturen. Die Kanal Schicht ermöglicht die vollständige Kontrolle über die Kommunikation mithilfe von [Nachrichten](message.md) , die aus gesendeten oder empfangenen Daten bestehen und den Text und Header enthalten, sowie von [Kanälen](channel.md) , die Nachrichtenaustausch Protokolle abstrahieren und Eigenschaften zum Anpassen von Einstellungen bereitstellen.

## <a name="message"></a>`Message`

Bei einer [Nachricht](message.md) handelt es sich um ein Objekt, das Netzwerkdaten kapselt – insbesondere Daten, die über ein Netzwerk übertragen oder empfangen werden. Die Nachrichtenstruktur wird durch SOAP definiert, mit einem diskreten Satz von Headern und einem Nachrichtentext. Die Header werden in einen Arbeitsspeicher Puffer eingefügt, und der Nachrichtentext wird mit einer Stream-API gelesen oder geschrieben.

![Diagramm, das die Kopfzeile und den Text einer Meldung anzeigt.](images/messageenvelope.png)

Obwohl das Datenmodell einer Nachricht immer das XML-Datenmodell ist, ist das tatsächliche Wire-Format flexibel. Bevor eine Nachricht übertragen wird, wird Sie mit einer bestimmten Codierung (z. b. Text, binary oder MTOM) codiert. Weitere Informationen zu Codierungen finden Sie unter [**WS- \_ Codierung**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .

![Diagramm mit mehreren Nachrichten Codierungs Formaten.](images/messageandencodings.png)

## <a name="channel"></a>Channel

Ein [Kanal](channel.md) ist ein Objekt, das zum Senden und empfangen von Nachrichten in einem Netzwerk zwischen zwei oder mehr Endpunkten verwendet wird.

Kanäle verfügen über zugeordnete Daten, die beschreiben, wie die Nachricht beim Senden [adressiert](endpoint-address.md) wird. Das Senden einer Nachricht in einem Kanal ähnelt dem Platzieren der Nachricht in einer Chute – der Kanal enthält die Informationen, in denen die Nachricht zu finden ist, und wie Sie Sie dort erhalten.

![Das Diagramm zeigt die Kanäle für Nachrichten an.](images/channelsaschute.png)

Kanäle werden in [**Kanaltypen**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)kategorisiert. Ein Kanaltyp gibt an, welche Richtung Nachrichten übertragen werden können. Der Kanaltyp gibt auch an, ob der Kanal Sitzungs basiert ist oder sessionless ist. Eine Sitzung wird als abstrakte Methode zum Korrelieren von Nachrichten zwischen zwei oder mehr Parteien definiert. Ein Beispiel für einen Sitzungs basierten Kanal ist ein TCP-Channel, bei dem die TCP-Verbindung als konkrete Sitzungs Implementierung verwendet wird. Ein Beispiel für einen sessionless-Kanal ist UDP, das über keinen zugrunde liegenden Sitzungs Mechanismus verfügt. Obwohl HTTP über zugrunde liegende TCP-Verbindungen verfügt, wird dieser Fakt nicht direkt über diese API verfügbar gemacht. Daher wird http auch als Sitzungs loser Kanal betrachtet.

![Diagramm, das Sitzungs basierte und Sitzungs lose Kanaltypen anzeigt.](images/channeltypes.png)

Obwohl Channeltypen die Richtung und Sitzungsinformationen eines Kanals beschreiben, geben Sie nicht an, wie der Kanal implementiert wird. Welches Protokoll sollte der Kanal verwenden? Wie schwierig sollte der Kanal versuchen, die Nachricht zu übermitteln? Welche Art von Sicherheit wird verwendet? Handelt es sich um einen singlecast oder einen Multicast? Diese Einstellungen werden als "Bindung" des Kanals bezeichnet. Die Bindung besteht aus den folgenden Elementen:

-   Eine [**WS \_ - \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), die das zu verwendende Übertragungsprotokoll (TCP, UDP, http, NamedPipe) identifiziert.
-   Eine [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), die angibt, wie der Kanal gesichert werden soll.
-   Eine Set [**WS \_ Channel- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), die zusätzliche optionale Einstellungen angibt. Eine Liste der Eigenschaften finden Sie unter [**WS- \_ \_ channeleigenschafts- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) .

![Diagramm, das eine Liste der Kanaleigenschaften anzeigt.](images/channelsandbindings.png)

## <a name="listener"></a>Listener

Um mit der Kommunikation zu beginnen, erstellt der Client ein Channel-Objekt. Aber wie erhält der Dienst sein Channelobjekt? Dies erfolgt durch Erstellen eines [Listener](listener.md). Zum Erstellen eines Listener sind die gleichen Bindungs Informationen erforderlich, die zum Erstellen eines Kanals erforderlich sind. Nachdem ein Listener erstellt wurde, kann die Anwendung Kanäle vom Listener akzeptieren. Da die Anwendung auf die Annahme von Kanälen zurückgreifen kann, behalten Listener in der Regel eine Warteschlange von Kanälen, die akzeptiert werden können (bis zu einem Kontingent).

![Diagramm mit Kanälen in der listenerwarteschlange.](images/channelaccept.png)

## <a name="initiating-communication-client"></a>Initiieren der Kommunikation (Client)

Verwenden Sie die folgende Sequenz, um die Kommunikation auf dem Client zu initiieren.

``` syntax
WsCreateChannel
for each address being sent to
{
    WsOpenChannel           // open channel to address
    // send and/or receive messages
    WsCloseChannel          // close channel
    WsResetChannel?         // reset if opening again
}
WsFreeChannel
```

## <a name="accepting-communication-server"></a>Akzeptieren der Kommunikation (Server)

Verwenden Sie die folgende Sequenz, um die eingehende Kommunikation auf dem Server zu akzeptieren.

``` syntax
WsCreateListener
WsOpenListener
for each channel being accepted (can be done in parallel)
{
    WsCreateChannelForListener
    for each accept
    {
        WsAcceptChannel     // accept the channel
        // send and/or receive messages
        WsCloseChannel      // close the channel
        WsResetChannel?     // reset if accepting again
    }
    WsFreeChannel
}
WsCloseListener
WsFreeListener
```

## <a name="sending-messages-client-or-server"></a>Senden von Nachrichten (Client oder Server)

Um Nachrichten zu senden, verwenden Sie die folgende Sequenz.

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

Die [**wssendmessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) -Funktion lässt kein Streaming zu und geht davon aus, dass der Text nur ein Element enthält. Verwenden Sie die folgende Sequenz anstelle von **wssendmessage**, um diese Einschränkungen zu vermeiden.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

Die Funktion [**wsschreitebody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) verwendet die Serialisierung zum Schreiben der Body-Elemente. Um die Daten direkt in den XML-Writer zu schreiben, verwenden Sie die folgende Sequenz anstelle von **wswrite**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

Die [**wsaddcustomheader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) -Funktion verwendet die Serialisierung, um die Header auf den Header Puffer der Nachricht festzulegen. Um den XML-Writer zum Schreiben eines Headers zu verwenden, verwenden Sie die folgende Sequenz anstelle von **wsaddcustomheader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a>Empfangen von Nachrichten (Client oder Server)

Um Nachrichten zu empfangen, verwenden Sie die folgende Sequenz.

``` syntax
WsCreateMessageForChannel
for each message being received
{
    WsReceiveMessage            // receive a message
    WsGetHeader*                // optionally access standard headers such as To or Action
    WsResetMessage              // reset if reading another message
}
WsFreeMessage
```

Die [**wsreceivemess Age**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) -Funktion lässt kein Streaming zu und geht davon aus, dass der Text nur ein Element enthält und dass der Typ der Nachricht (Aktion und Schema des Texts) im Vordergrund bekannt ist. Verwenden Sie die folgende Sequenz anstelle von **wsreceivemess**, um diese Einschränkungen zu vermeiden.

``` syntax
WsReadMessageStart              // read all headers into header buffer
for each standard header
{
    WsGetHeader                 // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader           // deserialize application defined header
}
for each element of the body
{
    WsFillBody?                 // optionally fill the body
    WsReadBody                  // deserialize element of body
}
WsReadMessageEnd                // read end of message
```

Die [**wslebody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) -Funktion verwendet die Serialisierung zum Lesen der Body-Elemente. Um die Daten direkt aus dem [XML-Reader](xml-reader.md)zu lesen, verwenden Sie die folgende Sequenz anstelle von **wslebody**.

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

Die [**wsgetcustomheader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) -Funktionen verwenden die Serialisierung, um die Header aus dem Header Puffer der Nachricht zu erhalten. Um den [XML-Reader](xml-reader.md) zum Lesen eines Headers zu verwenden, verwenden Sie die folgende Sequenz anstelle von **wsgetcustomheader**.

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateReader                      // create an xml reader
WsSetInputToBuffer                  // specify input of reader should be buffer
WsMoveReader*                       // move to inside header element
while looking for header to read
{
    WsReadToStartElement            // see if the header matches the application header
    if header matched
    {
        WsGetHeaderAttributes?      // get the standard header attributes
        WsReadStartElement          // consume the start of the header element
        // use the read functions to read the contents of the header element
        WsReadEndElement            // consume the end of the header element
    }
    else
    {
        WsSkipNode                  // skip the header element
    }
}                
```

## <a name="request-reply-client"></a>Anforderungs Antwort (Client)

Die Ausführung einer Anforderung/Antwort auf dem Client kann mit der folgenden Sequenz erfolgen.

``` syntax
WsCreateMessageForChannel               // create request message 
WsCreateMessageForChannel               // create reply message 
for each request reply
{
    WsRequestReply                      // send request, receive reply
    WsResetMessage?                     // reset request message (if repeating)
    WsResetMessage?                     // reset reply message (if repeating)
}
WsFreeMessage                           // free request message
WsFreeMessage                           // free reply message
```

Die [**wsrequestresponse**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) -Funktion geht von einem einzelnen-Element für den Text der Anforderungs-und Antwort Nachrichten aus, und der Typ der Nachricht (Aktion und Schema des Texts) ist im Vorfeld bekannt. Um diese Einschränkungen zu vermeiden, können die Anforderungs-und Antwortnachricht manuell gesendet werden, wie in der folgenden Sequenz gezeigt. Diese Sequenz entspricht der früheren Sequenz für das Senden und Empfangen einer Nachricht, sofern nicht anders angegeben.

``` syntax
WsInitializeMessage     // initialize message to WS_BLANK_MESSAGE
WsSetHeader             // serialize action header into header buffer
WsAddressMessage?       // optionally address message

// the following block is specific to sending a request
{
    generate a unique MessageID for request
    WsSetHeader         // set the message ID            
}

for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message

WsReadMessageStart      // read all headers into header buffer

// the following is specific to receiving a reply
{
    WsGetHeader         // deserialize RelatesTo ID of reply
    verify request MessageID is equal to RelatesTo ID
}

for each standard header
{
    WsGetHeader         // deserialize standard header such as To or Action
}
for each application defined header
{
    WsGetCustomHeader   // deserialize application defined header
}
for each element of the body
{
    WsFillBody?         // optionally fill the body
    WsReadBody          // deserialize element of body
}
WsReadMessageEnd        // read end of message                
```

## <a name="request-reply-server"></a>Anforderungs Antwort (Server)

Um eine Anforderungs Nachricht auf dem Server zu empfangen, verwenden Sie die gleiche Sequenz wie im vorherigen Abschnitt zum Empfangen von Nachrichten beschrieben.

Um eine Antwort oder eine Fehlermeldung zu senden, verwenden Sie die folgende Sequenz.

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

Die [**wssendreplymess Age**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) -Funktion geht von einem einzelnen Element im Text aus und lässt das Streaming nicht zu. Um diese Einschränkungen zu vermeiden, verwenden Sie die folgende Sequenz. Dies entspricht der früheren Sequenz für das Senden einer Nachricht. bei der Initialisierung wird jedoch die [**WS- \_ Antwort \_ Nachricht**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) anstelle der **WS- \_ leeren \_ Nachricht** verwendet.

``` syntax
// the following block is specific to sending a reply
{
    WsInitializeMessage // initialize message to WS_REPLY_MESSAGE
}
WsSetHeader             // serialize action header into header buffer                                
WsAddressMessage?       // optionally address message
for each application defined header
{
    WsAddCustomHeader   // serialize application-defined headers into header buffer
}
WsWriteMessageStart     // write out the headers of the message
for each element of the body
{
    WsWriteBody         // serialize the element of the body
    WsFlushBody?        // optionally flush the body
}
WsWriteMessageEnd       // write the end of the message
```

## <a name="message-exchange-patterns"></a>Nachrichtenaustauschmuster

Der [**WS \_ - \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) bestimmt das Nachrichtenaustausch Muster, das für einen bestimmten Kanal möglich ist. Der unterstützte Typ variiert gemäß der-Bindung wie folgt:

-   [**WS \_ Die HTTP- \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt die [**WS- \_ \_ Kanaltyp- \_ Anforderung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) auf dem Client und die **WS- \_ \_ Kanaltyp- \_ Antwort** auf dem Server
-   [**WS \_ Die TCP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt auf dem Client und der **WS- \_ \_ Kanaltyp- \_ Duplex \_ Sitzung** auf dem Server eine [**\_ \_ \_ Duplex \_ Sitzung des WS-Kanals**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) .
-   [**WS \_ Die UDP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt den [**WS- \_ \_ Kanaltyp \_ Duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) auf dem Client und die **WS- \_ \_ Kanaltyp- \_ Eingabe** auf dem Server.
-   [**WS \_ Die NamedPipe- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt den [**WS- \_ \_ Kanaltyp \_ Duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) auf dem Client und die **WS- \_ \_ Kanaltyp- \_ Eingabe** auf dem Server.

## <a name="message-loops"></a>Nachrichten Schleifen

Für jedes Nachrichtenaustausch Muster gibt es eine bestimmte "Schleife", die zum Senden oder empfangen von Nachrichten verwendet werden kann. Die Schleife beschreibt die gesetzliche Reihenfolge von Vorgängen, die zum Senden/Empfangen mehrerer Nachrichten erforderlich sind. Die Schleifen werden im folgenden als Grammatik-Produktionen beschrieben. Der ' End '-Begriff ist ein Empfang, bei dem das **WS \_ S- \_ Ende** zurückgegeben wird (siehe [Rückgabewerte der Windows-Webdienste](windows-web-services-return-values.md)) Die parallele Produktion gibt an, dass der Vorgang x parallel (x & y) gleichzeitig mit y ausgeführt werden kann.

Die folgenden Schleifen werden auf dem Client verwendet:

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

Die folgenden Schleifen werden auf dem Server verwendet:

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

Die Verwendung der [**WS- \_ Sicherheits \_ Kontext Nachrichten- \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) auf dem Server erfordert vor dem Senden einen erfolgreichen Empfang, auch bei einem Kanal vom Typ " [**WS- \_ \_ Kanaltyp \_ Duplex \_ Sitzung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)". Nach dem ersten Empfang. die reguläre Schleife wird angewendet.

Beachten Sie, dass Kanäle vom Typ " [**WS \_ Channel \_ Type \_ Request**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) " und " **WS \_ Channel \_ Type \_ Reply** " verwendet werden können, um unidirektionale Nachrichten zu senden und zu empfangen (und das standardmäßige Anforderung-Antwort-Muster). Dies wird erreicht, indem der Antwort Kanal geschlossen wird, ohne dass eine Antwort gesendet wird. In diesem Fall wird keine Antwort auf dem Anforderungs Kanal empfangen. Der Rückgabewert von **WS \_ S \_ endet** mithilfe der WS- [**\_ Sicherheits \_ Kontext Nachrichten- \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) auf dem Server erfordert einen erfolgreichen Empfangsvorgang, bevor das Senden auch mit einem Kanal vom Typ " **WS- \_ \_ Kanaltyp \_ Duplex \_ Sitzung**" zugelassen wird. Nachdem der erste Empfangs Empfang ist, gilt die reguläre Schleife.

wird zurückgegeben und gibt an, dass keine Meldung verfügbar ist.

Client-oder Server Schleifen können parallel untereinander mithilfe mehrerer Kanal Instanzen ausgeführt werden.

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a>Nachrichtenfilterung

Ein Serverchannel filtert möglicherweise empfangene Nachrichten, die nicht für die Anwendung vorgesehen sind, z. b. Nachrichten, die einen [Sicherheitskontext](security-context.md)einrichten In diesem Fall wird das **WS \_ S- \_ Ende** von [**wsread messagestart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) zurückgegeben, und es sind keine Anwendungs Nachrichten auf diesem Kanal verfügbar. Dies bedeutet jedoch nicht, dass der Client die Kommunikation mit dem Server beenden soll. Möglicherweise sind weitere Meldungen in einem anderen Kanal verfügbar. Siehe [**wsshutdownsessionchannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).

## <a name="cancellation"></a>Abbruch

Die [**wsabortchannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) -Funktion wird verwendet, um ausstehende e/a-Vorgänge für einen Kanal abzubrechen. Diese API wartet nicht auf den Abschluss der e/a-Vorgänge. Weitere Informationen finden Sie im [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) -channelstatusdiagramm und in der Dokumentation zu **wsabortchannel** .

Die [**wsabortlistener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) -API wird verwendet, um ausstehende e/a-Vorgänge für einen Listener abzubrechen. Diese API wartet nicht auf den Abschluss der e/a-Vorgänge. Das Abbrechen eines Listener bewirkt, dass alle ausstehenden Annahmen ebenfalls abgebrochen werden. Weitere Informationen finden Sie unter Status Diagramm des [**WS- \_ \_ listenerzustands**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) und **wsabortlistener** .

## <a name="tcp"></a>TCP

Die [**WS- \_ TCP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt SOAP über TCP. Die SOAP over TCP-Spezifikation basiert auf dem .NET-Rahmen Mechanismus.

Die Port Freigabe wird in dieser Version nicht unterstützt. Jeder Listener, der geöffnet wird, muss eine andere Portnummer verwenden.

## <a name="udp"></a>UDP

Die [**WS- \_ UDP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt SOAP über UDP.

Die UDP-Bindung hat eine Reihe von Einschränkungen:

-   Die Sicherheit wird nicht unterstützt.
-   Nachrichten können verloren gehen oder dupliziert werden.
-   Es wird nur eine Codierung unterstützt: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).
-   Die Nachrichten sind grundsätzlich auf 64 KB beschränkt und haben häufig die Wahrscheinlichkeit, dass Sie verloren gehen, wenn die Größe die MTU des Netzwerks überschreitet.

## <a name="http"></a>HTTP

Die [**WS- \_ http- \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt SOAP über http.

Informationen zum Steuern von HTTP-spezifischen Headern auf dem Client und dem Server finden Sie unter [**WS \_ http \_ Message \_ Mapping**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).

Um nicht-SOAP-Nachrichten auf dem Server zu senden und zu empfangen, verwenden Sie [**WS \_ Encoding \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) für die [**WS- \_ \_ channeleigenschaftscodierung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

## <a name="namedpipes"></a>Namedpipes

Die [**WS- \_ NamedPipe- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt SOAP über Named Pipes und ermöglicht die Kommunikation mit dem Windows Communication Foundation (WCF)-Dienst mithilfe von NetNamedPipeBinding.

## <a name="correlating-requestreply-messages"></a>Korrelieren von Anforderungs-/Antwort-Nachrichten

Anforderungs-/Antwort-Nachrichten werden auf eine von zwei Arten korreliert:

-   Die Korrelation erfolgt mithilfe des Kanals als Korrelations Mechanismus. Wenn beispielsweise der [**WS- \_ Adressierungs \_ Versions \_ Transport**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) und die [**WS-http- \_ \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) verwendet werden, wird die Antwort für die Anforderungs Nachricht von der Tatsache, dass es sich um den Entitäts Text der HTTP-Antwort handelt, mit der Anforderung korreliert.
-   Die Korrelation erfolgt mithilfe der MessageId-und RelatesTo-Header. Dieser Mechanismus wird mit [**WS- \_ Adressierungs \_ Version \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) und **WS- \_ Adressierung, \_ Version \_ 0 \_ 9** , verwendet (auch bei Verwendung der [**WS-http- \_ \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)). In diesem Fall enthält die Anforderungs Nachricht den MessageId-Header. Die Antwortnachricht enthält einen RelatesTo-Header mit dem Wert der MessageId-Kopfzeile der Anforderung. Der RelatesTo-Header ermöglicht es dem Client, eine Antwort mit einer gesendeten Anforderung zu korrelieren.

Die folgenden channelebenenapis verwenden automatisch die entsprechenden Korrelations Mechanismen basierend auf der [**WS- \_ Adressierungs \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) des Kanals.

-   [**Wsrequestreply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [**Wssendreplymess**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [**Wssendfaultmessageforerror**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

Wenn diese APIs nicht verwendet werden, können die Header manuell hinzugefügt und mithilfe von [**wssetheader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) oder [**wsgetheader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)aufgerufen werden.

## <a name="custom-channels-and-listeners"></a>Benutzerdefinierte Kanäle und Listener

Wenn der vordefinierte Satz von Kanal Bindungen nicht den Anforderungen der Anwendung entspricht, kann eine benutzerdefinierte Kanal-und Listenerimplementierung definiert werden, indem beim Erstellen des Kanals oder Listener die [**\_ benutzerdefinierte WS- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) angegeben wird. Die tatsächliche Implementierung des Kanals/Listener wird als Satz von Rückrufen über die [**\_ \_ \_ benutzerdefinierten \_ \_ channelrückrufe der WS-Channeleigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) oder die Eigenschaften der [**\_ \_ \_ benutzerdefinierten \_ listenerrückrufe \_ der WS-Listenereigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) angegeben. Sobald ein benutzerdefinierter Kanal oder Listener erstellt wurde, ist das Ergebnis ein [WS- \_ Channel](ws-channel.md) -oder [WS- \_ Listenerobjekt](ws-listener.md) , das mit vorhandenen APIs verwendet werden kann.

Ein benutzerdefinierter Kanal und ein benutzerdefinierter Listener können auch mit dem Dienst Proxy und dem [Dienst Host](service-host.md) verwendet werden, indem der **\_ benutzerdefinierte WS- \_ Kanal \_ Bindungs** Wert in der [**WS- \_ \_ channelbindungsenumeration**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) und die benutzerdefinierten channelrückrufe der WS- [**\_ \_ Channeleigenschaft \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) und [**\_ \_ \_ benutzerdefinierte \_ Listener \_ -Eigenschaften der WS-Listenereigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) bei der Erstellung des Dienst Proxys

## <a name="security"></a>Sicherheit

Der Kanal ermöglicht das Einschränken der Menge an Arbeitsspeicher, die für verschiedene Aspekte von Vorgängen verwendet wird, wie z. b.:

-   [**WS \_ \_Channeleigenschaft \_ Maximale \_ \_ \_ Größe der gepufferten Nachricht**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_maximal zulässige \_ \_ \_ Nachrichten \_ Größe für Channeleigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ Maximale streamingeigenschaftsstartgröße \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ Maximale Größe der \_ http \_ - \_ Anforderungs \_ Header \_ -Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)
-   [**WS \_ \_ \_ Maximale Größe der \_ Sitzungs \_ Wörterbücher \_ für die Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Diese Eigenschaften verfügen über Standardwerte, die für die meisten Szenarien konservativ und sicher sind. Standardwerte und ggf. vorgenommenen Änderungen sollten sorgfältig gegen mögliche Angriffsvektoren ausgewertet werden, die einen Denial-of-Service-Angriff durch einen Remote Benutzer verursachen können.

Der Kanal ermöglicht das Festlegen von Timeout Werten für verschiedene Aspekte von Vorgängen durch Eigenschaften wie z. b.:

-   [**WS \_ \_ \_ Verbindungs \_ Timeout für Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ Sende \_ Timeout für Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ Empfangs \_ Antwort \_ Timeout für Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ \_ \_ Empfangs \_ Timeout für Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),
-   [**WS \_ Kanal \_ Eigenschaft \_ Auflösungs \_ Timeout**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)
-   [**WS \_ Das \_ \_ Close- \_ Timeout der Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).

Diese Eigenschaften verfügen über Standardwerte, die für die meisten Szenarien konservativ und sicher sind. Das erhöhen von Timeout Werten erhöht die Zeitspanne, die eine Remote Partei eine lokale Ressource aufrechterhalten kann, z. b. Arbeitsspeicher, Sockets und Threads, die synchrone e/a-Vorgänge durchgeführt haben. Eine Anwendung sollte die Standardwerte auswerten und beim erhöhen eines Timeouts Vorsicht walten lassen, da dadurch möglicherweise potenzielle Angriffsvektoren geöffnet werden, die zu einem Denial-of-Service-Angriff von einem Remote Computer führen können.

Einige andere Konfigurationsoptionen und Überlegungen zum Anwendungs Entwurf, die bei der Verwendung der wwsapi-Kanal-API sorgfältig ausgewertet werden sollten:

-   Wenn die Kanal-/listenerebene verwendet wird, besteht die Anwendung darin, Kanäle auf der Serverseite zu erstellen und zu akzeptieren. Ebenso besteht die Anwendung darin, Kanäle auf der Clientseite zu erstellen und zu öffnen. Eine Anwendung sollte eine Obergrenze für diese Vorgänge festlegen, da jeder Kanal Arbeitsspeicher und andere begrenzte Ressourcen wie z. b. Sockets beansprucht. Eine Anwendung sollte besonders vorsichtig sein, wenn Sie einen Kanal als Reaktion auf Aktionen erstellen, die von einer Remote Partei ausgelöst werden.
-   Die Anwendung muss die Logik zum Erstellen von Kanälen schreiben und Sie akzeptieren. Jeder Kanal beansprucht begrenzte Ressourcen wie z. b. Arbeitsspeicher und Sockets. Eine Anwendung sollte über eine obere Grenze für die Anzahl der Kanäle verfügen, die Sie akzeptieren soll, oder eine Remote Partei könnte viele Verbindungen treffen, was zu OOM und somit zu einem Denial-of-Service führt. Außerdem sollte er mithilfe eines kleinen Timeouts aktiv Nachrichten von diesen Verbindungen empfangen. Wenn keine Nachrichten empfangen werden, tritt ein Timeout für den Vorgang auf, und die Verbindung sollte freigegeben werden.
-   Eine Anwendung kann eine Antwort oder einen Fehler senden, indem Sie die SOAP-Header "ReplyTo" oder "FaultTo" interpretiert. Die sichere Vorgehensweise ist, nur einen ReplyTo-oder FaultTo-Header zu beachten, der "Anonym" ist, was bedeutet, dass die vorhandene Verbindung (TCP, http) oder Quell-IP (UDP) zum Senden der SOAP-Antwort verwendet werden soll. Anwendungen sollten bei der Erstellung von Ressourcen (z. b. einem Kanal) äußerst vorsichtig sein, um auf eine andere Adresse zu antworten, es sei denn, die Nachricht wurde von einer Partei signiert, die für die Adresse sprechen kann, an die die Antwort gesendet wird.
-   Die in der Kanal Ebene ausgeführte Validierung ist kein Ersatz für die durch die Sicherheit erzielte Datenintegrität. Eine Anwendung muss sich auf Sicherheitsfeatures der wwsapi stützen, um sicherzustellen, dass Sie mit einer vertrauenswürdigen Entität kommuniziert und auch auf der Sicherheit basieren muss, um die Datenintegrität sicherzustellen.

Ebenso gibt es Optionen für die Nachrichten Konfiguration und den Anwendungs Entwurf, die bei der Verwendung der wwsapi-Nachrichten-API sorgfältig ausgewertet werden sollten:

-   Die Größe des Heaps, der zum Speichern der Header einer Nachricht verwendet wird, kann mithilfe der Eigenschaft [**\_ \_ \_ Eigenschaften Heap \_ Eigenschaften von WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) -Nachrichten konfiguriert werden. Wenn Sie diesen Wert erhöhen, kann mehr Arbeitsspeicher von den Headern der Nachricht genutzt werden, was zu OOM führen kann.
-   Der Benutzer des Message-Objekts muss erkennen, dass die Header Zugriffs-APIs in Bezug auf die Anzahl der Header in der Nachricht O (n) sind, da Sie auf Duplikate überprüfen. Entwürfe, bei denen viele Header in einer Nachricht erforderlich sind, können zu einer übermäßigen CPU-Auslastung führen.
-   Die maximale Anzahl von Headern in einer Nachricht kann mithilfe der Eigenschaft [**Eigenschaft \_ \_ Max. \_ \_ verarbeitete \_ Header der WS-Nachrichten Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) konfiguriert werden. Es gibt auch einen impliziten Grenzwert, der auf der Größe des Heaps der Nachricht basiert. Wenn beide Werte vergrößert werden, können mehr Header vorhanden sein, wodurch die erforderliche Zeit für die Suche nach einem Header (bei Verwendung der Header Zugriffs-APIs) anwächst.

 

 




