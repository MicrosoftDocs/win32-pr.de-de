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
# <a name="channel-layer-overview"></a><span data-ttu-id="610c7-106">Übersicht über die Kanal Schicht</span><span class="sxs-lookup"><span data-stu-id="610c7-106">Channel Layer Overview</span></span>

<span data-ttu-id="610c7-107">Die Kanal Schicht stellt eine Abstraktion des Transport Kanals und der Nachrichten bereit, die auf dem Kanal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-107">The Channel Layer provides an abstraction of the transport channel as well as messages sent out on the channel.</span></span> <span data-ttu-id="610c7-108">Sie enthält auch Funktionen für die Serialisierung von C-Datentypen in und aus SOAP-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="610c7-108">It also includes functions for the serialization of C data types to and from SOAP structures.</span></span> <span data-ttu-id="610c7-109">Die Kanal Schicht ermöglicht die vollständige Kontrolle über die Kommunikation mithilfe von [Nachrichten](message.md) , die aus gesendeten oder empfangenen Daten bestehen und den Text und Header enthalten, sowie von [Kanälen](channel.md) , die Nachrichtenaustausch Protokolle abstrahieren und Eigenschaften zum Anpassen von Einstellungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="610c7-109">The Channel Layer enables full control of communications by means of [messages](message.md) consisting of data sent or received and containing bodies and headers, and [channels](channel.md) that abstract message exchange protocols and provide properties for customizing settings.</span></span>

## <a name="message"></a><span data-ttu-id="610c7-110">`Message`</span><span class="sxs-lookup"><span data-stu-id="610c7-110">Message</span></span>

<span data-ttu-id="610c7-111">Bei einer [Nachricht](message.md) handelt es sich um ein Objekt, das Netzwerkdaten kapselt – insbesondere Daten, die über ein Netzwerk übertragen oder empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-111">A [message](message.md) is an object that encapsulates network data — specifically, data that is transmitted or received over a network.</span></span> <span data-ttu-id="610c7-112">Die Nachrichtenstruktur wird durch SOAP definiert, mit einem diskreten Satz von Headern und einem Nachrichtentext.</span><span class="sxs-lookup"><span data-stu-id="610c7-112">The message structure is defined by SOAP, with a discrete set of headers and a message body.</span></span> <span data-ttu-id="610c7-113">Die Header werden in einen Arbeitsspeicher Puffer eingefügt, und der Nachrichtentext wird mit einer Stream-API gelesen oder geschrieben.</span><span class="sxs-lookup"><span data-stu-id="610c7-113">The headers are placed in a memory buffer, and the message body is read or written using a stream API.</span></span>

![Diagramm, das die Kopfzeile und den Text einer Meldung anzeigt.](images/messageenvelope.png)

<span data-ttu-id="610c7-115">Obwohl das Datenmodell einer Nachricht immer das XML-Datenmodell ist, ist das tatsächliche Wire-Format flexibel.</span><span class="sxs-lookup"><span data-stu-id="610c7-115">Although the data model of a message is always the XML data model, the actual wire format is flexible.</span></span> <span data-ttu-id="610c7-116">Bevor eine Nachricht übertragen wird, wird Sie mit einer bestimmten Codierung (z. b. Text, binary oder MTOM) codiert.</span><span class="sxs-lookup"><span data-stu-id="610c7-116">Before a message is transmitted, it is encoded using a particular encoding (such as Text, Binary, or MTOM).</span></span> <span data-ttu-id="610c7-117">Weitere Informationen zu Codierungen finden Sie unter [**WS- \_ Codierung**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) .</span><span class="sxs-lookup"><span data-stu-id="610c7-117">See [**WS\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for more information on encodings.</span></span>

![Diagramm mit mehreren Nachrichten Codierungs Formaten.](images/messageandencodings.png)

## <a name="channel"></a><span data-ttu-id="610c7-119">Channel</span><span class="sxs-lookup"><span data-stu-id="610c7-119">Channel</span></span>

<span data-ttu-id="610c7-120">Ein [Kanal](channel.md) ist ein Objekt, das zum Senden und empfangen von Nachrichten in einem Netzwerk zwischen zwei oder mehr Endpunkten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="610c7-120">A [channel](channel.md) is an object used to send and receive messages on a network between two or more endpoints.</span></span>

<span data-ttu-id="610c7-121">Kanäle verfügen über zugeordnete Daten, die beschreiben, wie die Nachricht beim Senden [adressiert](endpoint-address.md) wird.</span><span class="sxs-lookup"><span data-stu-id="610c7-121">Channels have associated data that describes how to [address](endpoint-address.md) the message when it is sent.</span></span> <span data-ttu-id="610c7-122">Das Senden einer Nachricht in einem Kanal ähnelt dem Platzieren der Nachricht in einer Chute – der Kanal enthält die Informationen, in denen die Nachricht zu finden ist, und wie Sie Sie dort erhalten.</span><span class="sxs-lookup"><span data-stu-id="610c7-122">Sending a message on a channel is like placing it in a chute — the channel includes the information where the message should go and how to get it there.</span></span>

![Das Diagramm zeigt die Kanäle für Nachrichten an.](images/channelsaschute.png)

<span data-ttu-id="610c7-124">Kanäle werden in [**Kanaltypen**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)kategorisiert.</span><span class="sxs-lookup"><span data-stu-id="610c7-124">Channels are categorized into [**channel types**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="610c7-125">Ein Kanaltyp gibt an, welche Richtung Nachrichten übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="610c7-125">A channel type specifies which direction messages can flow.</span></span> <span data-ttu-id="610c7-126">Der Kanaltyp gibt auch an, ob der Kanal Sitzungs basiert ist oder sessionless ist.</span><span class="sxs-lookup"><span data-stu-id="610c7-126">The channel type also identifies whether the channel is sessionful, or sessionless.</span></span> <span data-ttu-id="610c7-127">Eine Sitzung wird als abstrakte Methode zum Korrelieren von Nachrichten zwischen zwei oder mehr Parteien definiert.</span><span class="sxs-lookup"><span data-stu-id="610c7-127">A session is defined as an abstract way of correlating messages between two or more parties.</span></span> <span data-ttu-id="610c7-128">Ein Beispiel für einen Sitzungs basierten Kanal ist ein TCP-Channel, bei dem die TCP-Verbindung als konkrete Sitzungs Implementierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="610c7-128">An example of a sessionful channel is a TCP channel, which uses the TCP connection as the concrete session implementation.</span></span> <span data-ttu-id="610c7-129">Ein Beispiel für einen sessionless-Kanal ist UDP, das über keinen zugrunde liegenden Sitzungs Mechanismus verfügt.</span><span class="sxs-lookup"><span data-stu-id="610c7-129">An example of a sessionless channel is UDP, which does not have an underlying session mechanism.</span></span> <span data-ttu-id="610c7-130">Obwohl HTTP über zugrunde liegende TCP-Verbindungen verfügt, wird dieser Fakt nicht direkt über diese API verfügbar gemacht. Daher wird http auch als Sitzungs loser Kanal betrachtet.</span><span class="sxs-lookup"><span data-stu-id="610c7-130">Although HTTP does have underlying TCP connections, this fact is not directly exposed through this API and therefore HTTP is also considered a sessionless channel.</span></span>

![Diagramm, das Sitzungs basierte und Sitzungs lose Kanaltypen anzeigt.](images/channeltypes.png)

<span data-ttu-id="610c7-132">Obwohl Channeltypen die Richtung und Sitzungsinformationen eines Kanals beschreiben, geben Sie nicht an, wie der Kanal implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="610c7-132">Although channel types describe the direction and session information for a channel, they do not specify how the channel is implemented.</span></span> <span data-ttu-id="610c7-133">Welches Protokoll sollte der Kanal verwenden?</span><span class="sxs-lookup"><span data-stu-id="610c7-133">What protocol should the channel use?</span></span> <span data-ttu-id="610c7-134">Wie schwierig sollte der Kanal versuchen, die Nachricht zu übermitteln?</span><span class="sxs-lookup"><span data-stu-id="610c7-134">How hard should the channel try to deliver the message?</span></span> <span data-ttu-id="610c7-135">Welche Art von Sicherheit wird verwendet?</span><span class="sxs-lookup"><span data-stu-id="610c7-135">What kind of security is used?</span></span> <span data-ttu-id="610c7-136">Handelt es sich um einen singlecast oder einen Multicast?</span><span class="sxs-lookup"><span data-stu-id="610c7-136">Is it singlecast or multicast?</span></span> <span data-ttu-id="610c7-137">Diese Einstellungen werden als "Bindung" des Kanals bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="610c7-137">These settings are referred to as the "binding" of the channel.</span></span> <span data-ttu-id="610c7-138">Die Bindung besteht aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="610c7-138">The binding consists of the following:</span></span>

-   <span data-ttu-id="610c7-139">Eine [**WS \_ - \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), die das zu verwendende Übertragungsprotokoll (TCP, UDP, http, NamedPipe) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="610c7-139">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use (TCP, UDP, HTTP, NAMEDPIPE).</span></span>
-   <span data-ttu-id="610c7-140">Eine [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), die angibt, wie der Kanal gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="610c7-140">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="610c7-141">Eine Set [**WS \_ Channel- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), die zusätzliche optionale Einstellungen angibt.</span><span class="sxs-lookup"><span data-stu-id="610c7-141">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings.</span></span> <span data-ttu-id="610c7-142">Eine Liste der Eigenschaften finden Sie unter [**WS- \_ \_ channeleigenschafts- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) .</span><span class="sxs-lookup"><span data-stu-id="610c7-142">See [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) for the list of properties.</span></span>

![Diagramm, das eine Liste der Kanaleigenschaften anzeigt.](images/channelsandbindings.png)

## <a name="listener"></a><span data-ttu-id="610c7-144">Listener</span><span class="sxs-lookup"><span data-stu-id="610c7-144">Listener</span></span>

<span data-ttu-id="610c7-145">Um mit der Kommunikation zu beginnen, erstellt der Client ein Channel-Objekt.</span><span class="sxs-lookup"><span data-stu-id="610c7-145">To start communicating, the client creates a Channel object.</span></span> <span data-ttu-id="610c7-146">Aber wie erhält der Dienst sein Channelobjekt?</span><span class="sxs-lookup"><span data-stu-id="610c7-146">But how does the service get its Channel object?</span></span> <span data-ttu-id="610c7-147">Dies erfolgt durch Erstellen eines [Listener](listener.md).</span><span class="sxs-lookup"><span data-stu-id="610c7-147">It does so by creating a [Listener](listener.md).</span></span> <span data-ttu-id="610c7-148">Zum Erstellen eines Listener sind die gleichen Bindungs Informationen erforderlich, die zum Erstellen eines Kanals erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="610c7-148">Creating a listener requires the same binding information that is necessary to create a channel.</span></span> <span data-ttu-id="610c7-149">Nachdem ein Listener erstellt wurde, kann die Anwendung Kanäle vom Listener akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="610c7-149">Once a Listener has been created, the application can Accept Channels from the Listener.</span></span> <span data-ttu-id="610c7-150">Da die Anwendung auf die Annahme von Kanälen zurückgreifen kann, behalten Listener in der Regel eine Warteschlange von Kanälen, die akzeptiert werden können (bis zu einem Kontingent).</span><span class="sxs-lookup"><span data-stu-id="610c7-150">Since the application may fall behind in accepting channels, listeners typically keep a queue of channels that are ready to accept (up to some quota).</span></span>

![Diagramm mit Kanälen in der listenerwarteschlange.](images/channelaccept.png)

## <a name="initiating-communication-client"></a><span data-ttu-id="610c7-152">Initiieren der Kommunikation (Client)</span><span class="sxs-lookup"><span data-stu-id="610c7-152">Initiating Communication (client)</span></span>

<span data-ttu-id="610c7-153">Verwenden Sie die folgende Sequenz, um die Kommunikation auf dem Client zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="610c7-153">To initiate communication on the client, use the following sequence.</span></span>

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

## <a name="accepting-communication-server"></a><span data-ttu-id="610c7-154">Akzeptieren der Kommunikation (Server)</span><span class="sxs-lookup"><span data-stu-id="610c7-154">Accepting Communication (server)</span></span>

<span data-ttu-id="610c7-155">Verwenden Sie die folgende Sequenz, um die eingehende Kommunikation auf dem Server zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="610c7-155">To accept incoming communications on the server, use the following sequence.</span></span>

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

## <a name="sending-messages-client-or-server"></a><span data-ttu-id="610c7-156">Senden von Nachrichten (Client oder Server)</span><span class="sxs-lookup"><span data-stu-id="610c7-156">Sending Messages (client or server)</span></span>

<span data-ttu-id="610c7-157">Um Nachrichten zu senden, verwenden Sie die folgende Sequenz.</span><span class="sxs-lookup"><span data-stu-id="610c7-157">To send messages, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each message being sent
{
    WsSendMessage       // send message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="610c7-158">Die [**wssendmessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) -Funktion lässt kein Streaming zu und geht davon aus, dass der Text nur ein Element enthält.</span><span class="sxs-lookup"><span data-stu-id="610c7-158">The [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage) function does not allow for streaming, and assumes that the body contains only one element.</span></span> <span data-ttu-id="610c7-159">Verwenden Sie die folgende Sequenz anstelle von **wssendmessage**, um diese Einschränkungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="610c7-159">To avoid these constraints, use the following sequence instead of **WsSendMessage**.</span></span>

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

<span data-ttu-id="610c7-160">Die Funktion [**wsschreitebody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) verwendet die Serialisierung zum Schreiben der Body-Elemente.</span><span class="sxs-lookup"><span data-stu-id="610c7-160">The [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody) function uses serialization to write the body elements.</span></span> <span data-ttu-id="610c7-161">Um die Daten direkt in den XML-Writer zu schreiben, verwenden Sie die folgende Sequenz anstelle von **wswrite**.</span><span class="sxs-lookup"><span data-stu-id="610c7-161">To write the data directly to the XML Writer, use the following sequence instead of **WsWriteBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_WRITER     // get the writer used to write the body
WsWriteStartElement
// use the writer functions to write the body
WsWriteEndElement
// optionally flush the body
WsFlushBody?        
```

<span data-ttu-id="610c7-162">Die [**wsaddcustomheader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) -Funktion verwendet die Serialisierung, um die Header auf den Header Puffer der Nachricht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="610c7-162">The [**WsAddCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsaddcustomheader) function uses serialization to set the headers to the header buffer of the message.</span></span> <span data-ttu-id="610c7-163">Um den XML-Writer zum Schreiben eines Headers zu verwenden, verwenden Sie die folgende Sequenz anstelle von **wsaddcustomheader**.</span><span class="sxs-lookup"><span data-stu-id="610c7-163">To use the XML Writer to write a header, use the following sequence instead of **WsAddCustomHeader**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_HEADER_BUFFER   // get the header buffer 
WsCreateWriter                      // create an xml writer
WsSetOutputToBuffer                 // specify output of writer should go to buffer
WsMoveWriter*                       // move to inside envelope header element
WsWriteStartElement                 // write application header start element
// use the writer functions to write the header 
WsWriteEndElement                   // write appilcation header end element
```

## <a name="receiving-messages-client-or-server"></a><span data-ttu-id="610c7-164">Empfangen von Nachrichten (Client oder Server)</span><span class="sxs-lookup"><span data-stu-id="610c7-164">Receiving Messages (client or server)</span></span>

<span data-ttu-id="610c7-165">Um Nachrichten zu empfangen, verwenden Sie die folgende Sequenz.</span><span class="sxs-lookup"><span data-stu-id="610c7-165">To receive messages, use the following sequence.</span></span>

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

<span data-ttu-id="610c7-166">Die [**wsreceivemess Age**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) -Funktion lässt kein Streaming zu und geht davon aus, dass der Text nur ein Element enthält und dass der Typ der Nachricht (Aktion und Schema des Texts) im Vordergrund bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="610c7-166">The [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage) function does not allow for streaming, and assumes that the body contains only one element, and that the type of the message (action and schema of the body) is known up front.</span></span> <span data-ttu-id="610c7-167">Verwenden Sie die folgende Sequenz anstelle von **wsreceivemess**, um diese Einschränkungen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="610c7-167">To avoid these constraints, use the following sequence instead of **WsReceiveMessage**.</span></span>

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

<span data-ttu-id="610c7-168">Die [**wslebody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) -Funktion verwendet die Serialisierung zum Lesen der Body-Elemente.</span><span class="sxs-lookup"><span data-stu-id="610c7-168">The [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody) function uses serialization to read the body elements.</span></span> <span data-ttu-id="610c7-169">Um die Daten direkt aus dem [XML-Reader](xml-reader.md)zu lesen, verwenden Sie die folgende Sequenz anstelle von **wslebody**.</span><span class="sxs-lookup"><span data-stu-id="610c7-169">To read the data directly from the [XML Reader](xml-reader.md), use the following sequence instead of **WsReadBody**.</span></span>

``` syntax
WS_MESSAGE_PROPERTY_BODY_READER     // get the reader used to read the body
WsFillBody?                         // optionally fill the body
WsReadToStartElement                // read up to the body element
WsReadStartElement                  // consume the start of the body element
// use the read functions to read the contents of the body element
WsReadEndElement                    // consume the end of the body element
```

<span data-ttu-id="610c7-170">Die [**wsgetcustomheader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) -Funktionen verwenden die Serialisierung, um die Header aus dem Header Puffer der Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="610c7-170">The [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader) functions use serialization to get the headers from the header buffer of the message.</span></span> <span data-ttu-id="610c7-171">Um den [XML-Reader](xml-reader.md) zum Lesen eines Headers zu verwenden, verwenden Sie die folgende Sequenz anstelle von **wsgetcustomheader**.</span><span class="sxs-lookup"><span data-stu-id="610c7-171">To use the [XML Reader](xml-reader.md) to read a header, use the following sequence instead of **WsGetCustomHeader**.</span></span>

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

## <a name="request-reply-client"></a><span data-ttu-id="610c7-172">Anforderungs Antwort (Client)</span><span class="sxs-lookup"><span data-stu-id="610c7-172">Request Reply (client)</span></span>

<span data-ttu-id="610c7-173">Die Ausführung einer Anforderung/Antwort auf dem Client kann mit der folgenden Sequenz erfolgen.</span><span class="sxs-lookup"><span data-stu-id="610c7-173">Performing a request-reply on the client can be done with the following sequence.</span></span>

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

<span data-ttu-id="610c7-174">Die [**wsrequestresponse**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) -Funktion geht von einem einzelnen-Element für den Text der Anforderungs-und Antwort Nachrichten aus, und der Typ der Nachricht (Aktion und Schema des Texts) ist im Vorfeld bekannt.</span><span class="sxs-lookup"><span data-stu-id="610c7-174">The [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) function assumes a single element for the body of the request and reply messages, and that the type of the message (action and schema of the body) are known up front.</span></span> <span data-ttu-id="610c7-175">Um diese Einschränkungen zu vermeiden, können die Anforderungs-und Antwortnachricht manuell gesendet werden, wie in der folgenden Sequenz gezeigt.</span><span class="sxs-lookup"><span data-stu-id="610c7-175">To avoid these limitations, the request and reply message can be sent manually, as shown in the following sequence.</span></span> <span data-ttu-id="610c7-176">Diese Sequenz entspricht der früheren Sequenz für das Senden und Empfangen einer Nachricht, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="610c7-176">This sequence matches the earlier sequence for sending and receiving a message, except where noted.</span></span>

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

## <a name="request-reply-server"></a><span data-ttu-id="610c7-177">Anforderungs Antwort (Server)</span><span class="sxs-lookup"><span data-stu-id="610c7-177">Request Reply (server)</span></span>

<span data-ttu-id="610c7-178">Um eine Anforderungs Nachricht auf dem Server zu empfangen, verwenden Sie die gleiche Sequenz wie im vorherigen Abschnitt zum Empfangen von Nachrichten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="610c7-178">To receive a request message on the server, use the same sequence as outlined in the previous section on receiving messages.</span></span>

<span data-ttu-id="610c7-179">Um eine Antwort oder eine Fehlermeldung zu senden, verwenden Sie die folgende Sequenz.</span><span class="sxs-lookup"><span data-stu-id="610c7-179">To send a reply or fault message, use the following sequence.</span></span>

``` syntax
WsCreateMessageForChannel
for each reply being sent
{
    WsSendReplyMessage | WsSendFaultMessageForError  // send reply or fault message
    WsResetMessage?     // reset if sending another message
}
WsFreeMessage
```

<span data-ttu-id="610c7-180">Die [**wssendreplymess Age**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) -Funktion geht von einem einzelnen Element im Text aus und lässt das Streaming nicht zu.</span><span class="sxs-lookup"><span data-stu-id="610c7-180">The [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage) function assumes a single element in the body and does not allow for streaming.</span></span> <span data-ttu-id="610c7-181">Um diese Einschränkungen zu vermeiden, verwenden Sie die folgende Sequenz.</span><span class="sxs-lookup"><span data-stu-id="610c7-181">To avoid these limitations, use the following sequence.</span></span> <span data-ttu-id="610c7-182">Dies entspricht der früheren Sequenz für das Senden einer Nachricht. bei der Initialisierung wird jedoch die [**WS- \_ Antwort \_ Nachricht**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) anstelle der **WS- \_ leeren \_ Nachricht** verwendet.</span><span class="sxs-lookup"><span data-stu-id="610c7-182">This is the same as the earlier sequence for sending a message, but uses [**WS\_REPLY\_MESSAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) instead of **WS\_BLANK\_MESSAGE** when initializing.</span></span>

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

## <a name="message-exchange-patterns"></a><span data-ttu-id="610c7-183">Nachrichtenaustauschmuster</span><span class="sxs-lookup"><span data-stu-id="610c7-183">Message Exchange Patterns</span></span>

<span data-ttu-id="610c7-184">Der [**WS \_ - \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) bestimmt das Nachrichtenaustausch Muster, das für einen bestimmten Kanal möglich ist.</span><span class="sxs-lookup"><span data-stu-id="610c7-184">The [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) dictates the message exchange pattern possible for a given channel.</span></span> <span data-ttu-id="610c7-185">Der unterstützte Typ variiert gemäß der-Bindung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="610c7-185">The type supported, varies according to the binding, as follows:</span></span>

-   <span data-ttu-id="610c7-186">[**WS \_ Die HTTP- \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt die [**WS- \_ \_ Kanaltyp- \_ Anforderung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) auf dem Client und die **WS- \_ \_ Kanaltyp- \_ Antwort** auf dem Server</span><span class="sxs-lookup"><span data-stu-id="610c7-186">[**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_REPLY** on the server.</span></span>
-   <span data-ttu-id="610c7-187">[**WS \_ Die TCP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt auf dem Client und der **WS- \_ \_ Kanaltyp- \_ Duplex \_ Sitzung** auf dem Server eine [**\_ \_ \_ Duplex \_ Sitzung des WS-Kanals**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) .</span><span class="sxs-lookup"><span data-stu-id="610c7-187">[**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION** on the server.</span></span>
-   <span data-ttu-id="610c7-188">[**WS \_ Die UDP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt den [**WS- \_ \_ Kanaltyp \_ Duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) auf dem Client und die **WS- \_ \_ Kanaltyp- \_ Eingabe** auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="610c7-188">[**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>
-   <span data-ttu-id="610c7-189">[**WS \_ Die NamedPipe- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt den [**WS- \_ \_ Kanaltyp \_ Duplex**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) auf dem Client und die **WS- \_ \_ Kanaltyp- \_ Eingabe** auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="610c7-189">[**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports [**WS\_CHANNEL\_TYPE\_DUPLEX**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) on the client and **WS\_CHANNEL\_TYPE\_INPUT** on the server.</span></span>

## <a name="message-loops"></a><span data-ttu-id="610c7-190">Nachrichten Schleifen</span><span class="sxs-lookup"><span data-stu-id="610c7-190">Message Loops</span></span>

<span data-ttu-id="610c7-191">Für jedes Nachrichtenaustausch Muster gibt es eine bestimmte "Schleife", die zum Senden oder empfangen von Nachrichten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="610c7-191">For each message exchange pattern, there is a specific "loop" that can be used to send or receive messages.</span></span> <span data-ttu-id="610c7-192">Die Schleife beschreibt die gesetzliche Reihenfolge von Vorgängen, die zum Senden/Empfangen mehrerer Nachrichten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="610c7-192">The loop describes the legal order of operations necessary to send/receive multiple messages.</span></span> <span data-ttu-id="610c7-193">Die Schleifen werden im folgenden als Grammatik-Produktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="610c7-193">The loops are describes below as grammar productions.</span></span> <span data-ttu-id="610c7-194">Der ' End '-Begriff ist ein Empfang, bei dem das **WS \_ S- \_ Ende** zurückgegeben wird (siehe [Rückgabewerte der Windows-Webdienste](windows-web-services-return-values.md))</span><span class="sxs-lookup"><span data-stu-id="610c7-194">The 'end' term is a receive where **WS\_S\_END** is returned (See [Windows Web Services Return Values](windows-web-services-return-values.md)), indicating no more messages are available on the channel.</span></span> <span data-ttu-id="610c7-195">Die parallele Produktion gibt an, dass der Vorgang x parallel (x & y) gleichzeitig mit y ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="610c7-195">The parallel production specifies that for parallel(x & y) that operation x may be done concurrently with y.</span></span>

<span data-ttu-id="610c7-196">Die folgenden Schleifen werden auf dem Client verwendet:</span><span class="sxs-lookup"><span data-stu-id="610c7-196">The following loops are used on the client:</span></span>

``` syntax
client-loop := client-request-loop | client-duplex-session-loop | client-duplex-loop
client-request-loop := open (send (receive | end))* close // WS_CHANNEL_TYPE_REQUEST
client-duplex-session-loop := open parallel(send* & receive*) parallel(send? & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
client-duplex-loop := open parallel(send & receive)* close // WS_CHANNEL_TYPE_DUPLEX
```

<span data-ttu-id="610c7-197">Die folgenden Schleifen werden auf dem Server verwendet:</span><span class="sxs-lookup"><span data-stu-id="610c7-197">The following loops are used on the server:</span></span>

``` syntax
server-loop: server-reply-loop | server-duplex-session-loop | server-duplex-loop
server-reply-loop := accept receive end* send? end* close // WS_CHANNEL_TYPE_REPLY
server-duplex-session-loop := accept parallel(send* & receive*) parallel(send* & end*) close // WS_CHANNEL_TYPE_DUPLEX_SESSION
server-input-loop := accept receive end* close // WS_CHANNEL_TYPE_INPUT
```

<span data-ttu-id="610c7-198">Die Verwendung der [**WS- \_ Sicherheits \_ Kontext Nachrichten- \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) auf dem Server erfordert vor dem Senden einen erfolgreichen Empfang, auch bei einem Kanal vom Typ " [**WS- \_ \_ Kanaltyp \_ Duplex \_ Sitzung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)".</span><span class="sxs-lookup"><span data-stu-id="610c7-198">Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type [**WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type).</span></span> <span data-ttu-id="610c7-199">Nach dem ersten Empfang.</span><span class="sxs-lookup"><span data-stu-id="610c7-199">After the first receive.</span></span> <span data-ttu-id="610c7-200">die reguläre Schleife wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="610c7-200">the regular loop applies.</span></span>

<span data-ttu-id="610c7-201">Beachten Sie, dass Kanäle vom Typ " [**WS \_ Channel \_ Type \_ Request**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) " und " **WS \_ Channel \_ Type \_ Reply** " verwendet werden können, um unidirektionale Nachrichten zu senden und zu empfangen (und das standardmäßige Anforderung-Antwort-Muster).</span><span class="sxs-lookup"><span data-stu-id="610c7-201">Note that channels of type [**WS\_CHANNEL\_TYPE\_REQUEST**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) and **WS\_CHANNEL\_TYPE\_REPLY** can be used to send and receive one-way messages (as well as the standard request-reply pattern).</span></span> <span data-ttu-id="610c7-202">Dies wird erreicht, indem der Antwort Kanal geschlossen wird, ohne dass eine Antwort gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="610c7-202">This is accomplished by closing the reply channel without sending a reply.</span></span> <span data-ttu-id="610c7-203">In diesem Fall wird keine Antwort auf dem Anforderungs Kanal empfangen.</span><span class="sxs-lookup"><span data-stu-id="610c7-203">In this case, there will be no reply received on the request channel.</span></span> <span data-ttu-id="610c7-204">Der Rückgabewert von **WS \_ S \_ endet** mithilfe der WS- [**\_ Sicherheits \_ Kontext Nachrichten- \_ \_ Sicherheits \_ Bindung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) auf dem Server erfordert einen erfolgreichen Empfangsvorgang, bevor das Senden auch mit einem Kanal vom Typ " **WS- \_ \_ Kanaltyp \_ Duplex \_ Sitzung**" zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="610c7-204">The return value **WS\_S\_END** Using the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) on the server requires a successful receive before sending is allowed even with a channel of type **WS\_CHANNEL\_TYPE\_DUPLEX\_SESSION**.</span></span> <span data-ttu-id="610c7-205">Nachdem der erste Empfangs Empfang ist, gilt die reguläre Schleife.</span><span class="sxs-lookup"><span data-stu-id="610c7-205">After the first receive the regular loop applies.</span></span>

<span data-ttu-id="610c7-206">wird zurückgegeben und gibt an, dass keine Meldung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="610c7-206">will be returned, indicating no message available.</span></span>

<span data-ttu-id="610c7-207">Client-oder Server Schleifen können parallel untereinander mithilfe mehrerer Kanal Instanzen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-207">Client or server loops may be done in parallel with each other by using multiple channel instances.</span></span>

``` syntax
parallel-client: parallel(client-loop(channel1) & client-loop(channel2) & ...)
parallel-server: parallel(server-loop(channel1) & server-loop(channel2) & ...)
```

## <a name="message-filtering"></a><span data-ttu-id="610c7-208">Nachrichtenfilterung</span><span class="sxs-lookup"><span data-stu-id="610c7-208">Message Filtering</span></span>

<span data-ttu-id="610c7-209">Ein Serverchannel filtert möglicherweise empfangene Nachrichten, die nicht für die Anwendung vorgesehen sind, z. b. Nachrichten, die einen [Sicherheitskontext](security-context.md)einrichten</span><span class="sxs-lookup"><span data-stu-id="610c7-209">A server channel may filter received messages that are not intended for the application, such as messages that establish a [security context](security-context.md).</span></span> <span data-ttu-id="610c7-210">In diesem Fall wird das **WS \_ S- \_ Ende** von [**wsread messagestart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) zurückgegeben, und es sind keine Anwendungs Nachrichten auf diesem Kanal verfügbar.</span><span class="sxs-lookup"><span data-stu-id="610c7-210">In that case **WS\_S\_END** will be returned from [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) and no application messages will be available on that channel.</span></span> <span data-ttu-id="610c7-211">Dies bedeutet jedoch nicht, dass der Client die Kommunikation mit dem Server beenden soll.</span><span class="sxs-lookup"><span data-stu-id="610c7-211">However, this does not signal that the client intended to end communication with the server.</span></span> <span data-ttu-id="610c7-212">Möglicherweise sind weitere Meldungen in einem anderen Kanal verfügbar.</span><span class="sxs-lookup"><span data-stu-id="610c7-212">More messages may be available on another channel.</span></span> <span data-ttu-id="610c7-213">Siehe [**wsshutdownsessionchannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span><span class="sxs-lookup"><span data-stu-id="610c7-213">See [**WsShutdownSessionChannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel).</span></span>

## <a name="cancellation"></a><span data-ttu-id="610c7-214">Abbruch</span><span class="sxs-lookup"><span data-stu-id="610c7-214">Cancellation</span></span>

<span data-ttu-id="610c7-215">Die [**wsabortchannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) -Funktion wird verwendet, um ausstehende e/a-Vorgänge für einen Kanal abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="610c7-215">The [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) function is used to cancel pending IO for a channel.</span></span> <span data-ttu-id="610c7-216">Diese API wartet nicht auf den Abschluss der e/a-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="610c7-216">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="610c7-217">Weitere Informationen finden Sie im [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) -channelstatusdiagramm und in der Dokumentation zu **wsabortchannel** .</span><span class="sxs-lookup"><span data-stu-id="610c7-217">See the [**WS\_CHANNEL\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) state diagram and documentation for **WsAbortChannel** for more information.</span></span>

<span data-ttu-id="610c7-218">Die [**wsabortlistener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) -API wird verwendet, um ausstehende e/a-Vorgänge für einen Listener abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="610c7-218">The [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener) API is used to cancel pending IO for a listener.</span></span> <span data-ttu-id="610c7-219">Diese API wartet nicht auf den Abschluss der e/a-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="610c7-219">This API will not wait for the IO operation(s) to complete.</span></span> <span data-ttu-id="610c7-220">Das Abbrechen eines Listener bewirkt, dass alle ausstehenden Annahmen ebenfalls abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-220">Aborting a listener will cause any pending accepts to be aborted as well.</span></span> <span data-ttu-id="610c7-221">Weitere Informationen finden Sie unter Status Diagramm des [**WS- \_ \_ listenerzustands**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) und **wsabortlistener** .</span><span class="sxs-lookup"><span data-stu-id="610c7-221">See the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) state diagram and **WsAbortListener** for more information.</span></span>

## <a name="tcp"></a><span data-ttu-id="610c7-222">TCP</span><span class="sxs-lookup"><span data-stu-id="610c7-222">TCP</span></span>

<span data-ttu-id="610c7-223">Die [**WS- \_ TCP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt SOAP über TCP.</span><span class="sxs-lookup"><span data-stu-id="610c7-223">The [**WS\_TCP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over TCP.</span></span> <span data-ttu-id="610c7-224">Die SOAP over TCP-Spezifikation basiert auf dem .NET-Rahmen Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="610c7-224">The SOAP over TCP specification builds upon the .NET Framing mechanism.</span></span>

<span data-ttu-id="610c7-225">Die Port Freigabe wird in dieser Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="610c7-225">Port sharing is not supported in this version.</span></span> <span data-ttu-id="610c7-226">Jeder Listener, der geöffnet wird, muss eine andere Portnummer verwenden.</span><span class="sxs-lookup"><span data-stu-id="610c7-226">Each listener that is opened must use a different port number.</span></span>

## <a name="udp"></a><span data-ttu-id="610c7-227">UDP</span><span class="sxs-lookup"><span data-stu-id="610c7-227">UDP</span></span>

<span data-ttu-id="610c7-228">Die [**WS- \_ UDP- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt SOAP über UDP.</span><span class="sxs-lookup"><span data-stu-id="610c7-228">The [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over UDP.</span></span>

<span data-ttu-id="610c7-229">Die UDP-Bindung hat eine Reihe von Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="610c7-229">There are a number of limitations with the UDP binding:</span></span>

-   <span data-ttu-id="610c7-230">Die Sicherheit wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="610c7-230">There is no support for security.</span></span>
-   <span data-ttu-id="610c7-231">Nachrichten können verloren gehen oder dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-231">Messages may be lost or duplicated.</span></span>
-   <span data-ttu-id="610c7-232">Es wird nur eine Codierung unterstützt: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span><span class="sxs-lookup"><span data-stu-id="610c7-232">Only one encoding is supported: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding).</span></span>
-   <span data-ttu-id="610c7-233">Die Nachrichten sind grundsätzlich auf 64 KB beschränkt und haben häufig die Wahrscheinlichkeit, dass Sie verloren gehen, wenn die Größe die MTU des Netzwerks überschreitet.</span><span class="sxs-lookup"><span data-stu-id="610c7-233">Messages are fundamentally limited to 64k, and frequently have a greater chance being lost if the size exceeds the MTU of the network.</span></span>

## <a name="http"></a><span data-ttu-id="610c7-234">HTTP</span><span class="sxs-lookup"><span data-stu-id="610c7-234">HTTP</span></span>

<span data-ttu-id="610c7-235">Die [**WS- \_ http- \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt SOAP über http.</span><span class="sxs-lookup"><span data-stu-id="610c7-235">The [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over HTTP.</span></span>

<span data-ttu-id="610c7-236">Informationen zum Steuern von HTTP-spezifischen Headern auf dem Client und dem Server finden Sie unter [**WS \_ http \_ Message \_ Mapping**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span><span class="sxs-lookup"><span data-stu-id="610c7-236">To control HTTP specific headers on the client and server, see [**WS\_HTTP\_MESSAGE\_MAPPING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping).</span></span>

<span data-ttu-id="610c7-237">Um nicht-SOAP-Nachrichten auf dem Server zu senden und zu empfangen, verwenden Sie [**WS \_ Encoding \_ RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) für die [**WS- \_ \_ channeleigenschaftscodierung \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="610c7-237">To send and receive non-SOAP messages on the server, use [**WS\_ENCODING\_RAW**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding) for [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

## <a name="namedpipes"></a><span data-ttu-id="610c7-238">Namedpipes</span><span class="sxs-lookup"><span data-stu-id="610c7-238">NAMEDPIPES</span></span>

<span data-ttu-id="610c7-239">Die [**WS- \_ NamedPipe- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) unterstützt SOAP über Named Pipes und ermöglicht die Kommunikation mit dem Windows Communication Foundation (WCF)-Dienst mithilfe von NetNamedPipeBinding.</span><span class="sxs-lookup"><span data-stu-id="610c7-239">The [**WS\_NAMEDPIPE\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) supports SOAP over named pipes, allowing communication with the Windows Communication Foundation (WCF) service using NetNamedPipeBinding.</span></span>

## <a name="correlating-requestreply-messages"></a><span data-ttu-id="610c7-240">Korrelieren von Anforderungs-/Antwort-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="610c7-240">Correlating Request/Reply Messages</span></span>

<span data-ttu-id="610c7-241">Anforderungs-/Antwort-Nachrichten werden auf eine von zwei Arten korreliert:</span><span class="sxs-lookup"><span data-stu-id="610c7-241">Request/Reply messages are correlated in one of two ways:</span></span>

-   <span data-ttu-id="610c7-242">Die Korrelation erfolgt mithilfe des Kanals als Korrelations Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="610c7-242">Correlation is done using the channel as the correlation mechanism.</span></span> <span data-ttu-id="610c7-243">Wenn beispielsweise der [**WS- \_ Adressierungs \_ Versions \_ Transport**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) und die [**WS-http- \_ \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) verwendet werden, wird die Antwort für die Anforderungs Nachricht von der Tatsache, dass es sich um den Entitäts Text der HTTP-Antwort handelt, mit der Anforderung korreliert.</span><span class="sxs-lookup"><span data-stu-id="610c7-243">For example, when using [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) the reply for the request message is correlated to the request by the fact that is it is the entity body of the HTTP response.</span></span>
-   <span data-ttu-id="610c7-244">Die Korrelation erfolgt mithilfe der MessageId-und RelatesTo-Header.</span><span class="sxs-lookup"><span data-stu-id="610c7-244">Correlation is done using the MessageID and RelatesTo headers.</span></span> <span data-ttu-id="610c7-245">Dieser Mechanismus wird mit [**WS- \_ Adressierungs \_ Version \_ 1 \_ 0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) und **WS- \_ Adressierung, \_ Version \_ 0 \_ 9** , verwendet (auch bei Verwendung der [**WS-http- \_ \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span><span class="sxs-lookup"><span data-stu-id="610c7-245">This mechanism is used with [**WS\_ADDRESSING\_VERSION\_1\_0**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) and **WS\_ADDRESSING\_VERSION\_0\_9** (even when using [**WS\_HTTP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)).</span></span> <span data-ttu-id="610c7-246">In diesem Fall enthält die Anforderungs Nachricht den MessageId-Header.</span><span class="sxs-lookup"><span data-stu-id="610c7-246">In this case, the request message includes the MessageID header.</span></span> <span data-ttu-id="610c7-247">Die Antwortnachricht enthält einen RelatesTo-Header mit dem Wert der MessageId-Kopfzeile der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="610c7-247">The response message includes a RelatesTo header that has the value of the request's MessageID header.</span></span> <span data-ttu-id="610c7-248">Der RelatesTo-Header ermöglicht es dem Client, eine Antwort mit einer gesendeten Anforderung zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="610c7-248">The RelatesTo header allows the client to correlate a response with a request it sent.</span></span>

<span data-ttu-id="610c7-249">Die folgenden channelebenenapis verwenden automatisch die entsprechenden Korrelations Mechanismen basierend auf der [**WS- \_ Adressierungs \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) des Kanals.</span><span class="sxs-lookup"><span data-stu-id="610c7-249">The following channel layer APIs automatically use the appropriate correlation mechanisms based on the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) of the channel.</span></span>

-   [<span data-ttu-id="610c7-250">**Wsrequestreply**</span><span class="sxs-lookup"><span data-stu-id="610c7-250">**WsRequestReply**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)
-   [<span data-ttu-id="610c7-251">**Wssendreplymess**</span><span class="sxs-lookup"><span data-stu-id="610c7-251">**WsSendReplyMessage**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)
-   [<span data-ttu-id="610c7-252">**Wssendfaultmessageforerror**</span><span class="sxs-lookup"><span data-stu-id="610c7-252">**WsSendFaultMessageForError**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror)

<span data-ttu-id="610c7-253">Wenn diese APIs nicht verwendet werden, können die Header manuell hinzugefügt und mithilfe von [**wssetheader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) oder [**wsgetheader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-253">If these APIs are not used, the headers can be manually added and accessed using [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader) or [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader).</span></span>

## <a name="custom-channels-and-listeners"></a><span data-ttu-id="610c7-254">Benutzerdefinierte Kanäle und Listener</span><span class="sxs-lookup"><span data-stu-id="610c7-254">Custom Channels and Listeners</span></span>

<span data-ttu-id="610c7-255">Wenn der vordefinierte Satz von Kanal Bindungen nicht den Anforderungen der Anwendung entspricht, kann eine benutzerdefinierte Kanal-und Listenerimplementierung definiert werden, indem beim Erstellen des Kanals oder Listener die [**\_ benutzerdefinierte WS- \_ \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="610c7-255">If the predefined set of channel bindings do not meet the needs of the application, then a custom channel and listener implementation can be defined by specifying [**WS\_CUSTOM\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) when creating the channel or listener.</span></span> <span data-ttu-id="610c7-256">Die tatsächliche Implementierung des Kanals/Listener wird als Satz von Rückrufen über die [**\_ \_ \_ benutzerdefinierten \_ \_ channelrückrufe der WS-Channeleigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) oder die Eigenschaften der [**\_ \_ \_ benutzerdefinierten \_ listenerrückrufe \_ der WS-Listenereigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) angegeben.</span><span class="sxs-lookup"><span data-stu-id="610c7-256">The actual implementation of the channel/listener is specified as a set of callbacks via [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) or [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties.</span></span> <span data-ttu-id="610c7-257">Sobald ein benutzerdefinierter Kanal oder Listener erstellt wurde, ist das Ergebnis ein [WS- \_ Channel](ws-channel.md) -oder [WS- \_ Listenerobjekt](ws-listener.md) , das mit vorhandenen APIs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="610c7-257">Once a custom channel or listener are created, the result is a [WS\_CHANNEL](ws-channel.md) or [WS\_LISTENER](ws-listener.md) object that can be used with existing APIs.</span></span>

<span data-ttu-id="610c7-258">Ein benutzerdefinierter Kanal und ein benutzerdefinierter Listener können auch mit dem Dienst Proxy und dem [Dienst Host](service-host.md) verwendet werden, indem der **\_ benutzerdefinierte WS- \_ Kanal \_ Bindungs** Wert in der [**WS- \_ \_ channelbindungsenumeration**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) und die benutzerdefinierten channelrückrufe der WS- [**\_ \_ Channeleigenschaft \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) und [**\_ \_ \_ benutzerdefinierte \_ Listener \_ -Eigenschaften der WS-Listenereigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) bei der Erstellung des Dienst Proxys</span><span class="sxs-lookup"><span data-stu-id="610c7-258">A custom channel and listener can also be used with Service Proxy and [Service Host](service-host.md) by specifying the **WS\_CUSTOM\_CHANNEL\_BINDING** value in the [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) enumeration and the [**WS\_CHANNEL\_PROPERTY\_CUSTOM\_CHANNEL\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) and [**WS\_LISTENER\_PROPERTY\_CUSTOM\_LISTENER\_CALLBACKS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id) properties when creating the Service Proxy or Service Host.</span></span>

## <a name="security"></a><span data-ttu-id="610c7-259">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="610c7-259">Security</span></span>

<span data-ttu-id="610c7-260">Der Kanal ermöglicht das Einschränken der Menge an Arbeitsspeicher, die für verschiedene Aspekte von Vorgängen verwendet wird, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="610c7-260">The channel allows limiting the amount of memory used for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="610c7-261">[**WS \_ \_Channeleigenschaft \_ Maximale \_ \_ \_ Größe der gepufferten Nachricht**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="610c7-261">[**WS\_CHANNEL\_PROPERTY\_MAX\_BUFFERED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-262">[**WS \_ \_maximal zulässige \_ \_ \_ Nachrichten \_ Größe für Channeleigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="610c7-262">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_MESSAGE\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-263">[**WS \_ \_ \_ Maximale streamingeigenschaftsstartgröße \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="610c7-263">[**WS\_CHANNEL\_PROPERTY\_MAX\_STREAMED\_START\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-264">[**WS \_ \_ \_ Maximale Größe der \_ http \_ - \_ Anforderungs \_ Header \_ -Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="610c7-264">[**WS\_CHANNEL\_PROPERTY\_MAX\_HTTP\_REQUEST\_HEADERS\_BUFFER\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-265">[**WS \_ \_ \_ Maximale Größe der \_ Sitzungs \_ Wörterbücher \_ für die Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="610c7-265">[**WS\_CHANNEL\_PROPERTY\_MAX\_SESSION\_DICTIONARY\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="610c7-266">Diese Eigenschaften verfügen über Standardwerte, die für die meisten Szenarien konservativ und sicher sind.</span><span class="sxs-lookup"><span data-stu-id="610c7-266">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="610c7-267">Standardwerte und ggf. vorgenommenen Änderungen sollten sorgfältig gegen mögliche Angriffsvektoren ausgewertet werden, die einen Denial-of-Service-Angriff durch einen Remote Benutzer verursachen können.</span><span class="sxs-lookup"><span data-stu-id="610c7-267">Default values and any modifications to them should be carefully evaluated against potential attack vectors which may cause denial of service by a remote user.</span></span>

<span data-ttu-id="610c7-268">Der Kanal ermöglicht das Festlegen von Timeout Werten für verschiedene Aspekte von Vorgängen durch Eigenschaften wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="610c7-268">The channel allows setting timeout values for various aspects of operations through properties such as:</span></span>

-   <span data-ttu-id="610c7-269">[**WS \_ \_ \_ Verbindungs \_ Timeout für Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="610c7-269">[**WS\_CHANNEL\_PROPERTY\_CONNECT\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-270">[**WS \_ \_ \_ Sende \_ Timeout für Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="610c7-270">[**WS\_CHANNEL\_PROPERTY\_SEND\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-271">[**WS \_ \_ \_ Empfangs \_ Antwort \_ Timeout für Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="610c7-271">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_RESPONSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-272">[**WS \_ \_ \_ Empfangs \_ Timeout für Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span><span class="sxs-lookup"><span data-stu-id="610c7-272">[**WS\_CHANNEL\_PROPERTY\_RECEIVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-273">[**WS \_ Kanal \_ Eigenschaft \_ Auflösungs \_ Timeout**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)</span><span class="sxs-lookup"><span data-stu-id="610c7-273">[**WS\_CHANNEL\_PROPERTY\_RESOLVE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id),</span></span>
-   <span data-ttu-id="610c7-274">[**WS \_ Das \_ \_ Close- \_ Timeout der Kanal Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span><span class="sxs-lookup"><span data-stu-id="610c7-274">[**WS\_CHANNEL\_PROPERTY\_CLOSE\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id).</span></span>

<span data-ttu-id="610c7-275">Diese Eigenschaften verfügen über Standardwerte, die für die meisten Szenarien konservativ und sicher sind.</span><span class="sxs-lookup"><span data-stu-id="610c7-275">These properties have default values which are conservative and secure for most scenarios.</span></span> <span data-ttu-id="610c7-276">Das erhöhen von Timeout Werten erhöht die Zeitspanne, die eine Remote Partei eine lokale Ressource aufrechterhalten kann, z. b. Arbeitsspeicher, Sockets und Threads, die synchrone e/a-Vorgänge durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="610c7-276">Increasing timeout values increases the amount of time that a remote party can hold a local resource alive, such as memory, sockets, and threads doing synchronous I/O.</span></span> <span data-ttu-id="610c7-277">Eine Anwendung sollte die Standardwerte auswerten und beim erhöhen eines Timeouts Vorsicht walten lassen, da dadurch möglicherweise potenzielle Angriffsvektoren geöffnet werden, die zu einem Denial-of-Service-Angriff von einem Remote Computer führen können.</span><span class="sxs-lookup"><span data-stu-id="610c7-277">An application should evaluate the default values and use caution when increasing a timeout as it may open up potential attack vectors which may cause denial of service from a remote computer.</span></span>

<span data-ttu-id="610c7-278">Einige andere Konfigurationsoptionen und Überlegungen zum Anwendungs Entwurf, die bei der Verwendung der wwsapi-Kanal-API sorgfältig ausgewertet werden sollten:</span><span class="sxs-lookup"><span data-stu-id="610c7-278">Some of the other configuration options and application design considerations that should be carefully evaluated when using WWSAPI Channel API:</span></span>

-   <span data-ttu-id="610c7-279">Wenn die Kanal-/listenerebene verwendet wird, besteht die Anwendung darin, Kanäle auf der Serverseite zu erstellen und zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="610c7-279">When using the channel/listener layer, it is up to the application to create and accept channels on the server side.</span></span> <span data-ttu-id="610c7-280">Ebenso besteht die Anwendung darin, Kanäle auf der Clientseite zu erstellen und zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="610c7-280">Similarly, it is up to the application to create and open channels on the client side.</span></span> <span data-ttu-id="610c7-281">Eine Anwendung sollte eine Obergrenze für diese Vorgänge festlegen, da jeder Kanal Arbeitsspeicher und andere begrenzte Ressourcen wie z. b. Sockets beansprucht.</span><span class="sxs-lookup"><span data-stu-id="610c7-281">An application should put an upper bound on these operations because each channel consumes memory and other limited resources such as sockets.</span></span> <span data-ttu-id="610c7-282">Eine Anwendung sollte besonders vorsichtig sein, wenn Sie einen Kanal als Reaktion auf Aktionen erstellen, die von einer Remote Partei ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-282">An application should be especially careful when create a channel in response to any action triggered by a remote party.</span></span>
-   <span data-ttu-id="610c7-283">Die Anwendung muss die Logik zum Erstellen von Kanälen schreiben und Sie akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="610c7-283">It is up to the application to write the logic to create channels and accept them.</span></span> <span data-ttu-id="610c7-284">Jeder Kanal beansprucht begrenzte Ressourcen wie z. b. Arbeitsspeicher und Sockets.</span><span class="sxs-lookup"><span data-stu-id="610c7-284">Each channel consumes limited resources such as memory and sockets.</span></span> <span data-ttu-id="610c7-285">Eine Anwendung sollte über eine obere Grenze für die Anzahl der Kanäle verfügen, die Sie akzeptieren soll, oder eine Remote Partei könnte viele Verbindungen treffen, was zu OOM und somit zu einem Denial-of-Service führt.</span><span class="sxs-lookup"><span data-stu-id="610c7-285">An application should have an upper bound on the number of channels it is willing to accept, or a remote party could make many connections, leading to OOM and hence denial of service.</span></span> <span data-ttu-id="610c7-286">Außerdem sollte er mithilfe eines kleinen Timeouts aktiv Nachrichten von diesen Verbindungen empfangen.</span><span class="sxs-lookup"><span data-stu-id="610c7-286">It should also actively receive messages from those connections using a small timeout.</span></span> <span data-ttu-id="610c7-287">Wenn keine Nachrichten empfangen werden, tritt ein Timeout für den Vorgang auf, und die Verbindung sollte freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-287">If no messages are received, then the operation will time out and the connection should be released.</span></span>
-   <span data-ttu-id="610c7-288">Eine Anwendung kann eine Antwort oder einen Fehler senden, indem Sie die SOAP-Header "ReplyTo" oder "FaultTo" interpretiert.</span><span class="sxs-lookup"><span data-stu-id="610c7-288">It is up to an application to send a reply or fault by interpreting the ReplyTo or FaultTo SOAP headers.</span></span> <span data-ttu-id="610c7-289">Die sichere Vorgehensweise ist, nur einen ReplyTo-oder FaultTo-Header zu beachten, der "Anonym" ist, was bedeutet, dass die vorhandene Verbindung (TCP, http) oder Quell-IP (UDP) zum Senden der SOAP-Antwort verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="610c7-289">The secure practice is to only honor a ReplyTo or FaultTo header which is "anonymous", meaning that the existing connection (TCP, HTTP) or source IP (UDP) should be used to send the SOAP reply.</span></span> <span data-ttu-id="610c7-290">Anwendungen sollten bei der Erstellung von Ressourcen (z. b. einem Kanal) äußerst vorsichtig sein, um auf eine andere Adresse zu antworten, es sei denn, die Nachricht wurde von einer Partei signiert, die für die Adresse sprechen kann, an die die Antwort gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="610c7-290">Applications should exercise extreme caution when creating resources (such as a channel) in order to reply to a different address, unless the message was signed by a party that can speak for the address that the reply is being sent to.</span></span>
-   <span data-ttu-id="610c7-291">Die in der Kanal Ebene ausgeführte Validierung ist kein Ersatz für die durch die Sicherheit erzielte Datenintegrität.</span><span class="sxs-lookup"><span data-stu-id="610c7-291">The validation done in the channel layer is no replacement for data integrity achieved through security.</span></span> <span data-ttu-id="610c7-292">Eine Anwendung muss sich auf Sicherheitsfeatures der wwsapi stützen, um sicherzustellen, dass Sie mit einer vertrauenswürdigen Entität kommuniziert und auch auf der Sicherheit basieren muss, um die Datenintegrität sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="610c7-292">An application must rely on security features of the WWSAPI to ensure that it is communicating with a trusted entity, and must also rely on security to ensure data integrity.</span></span>

<span data-ttu-id="610c7-293">Ebenso gibt es Optionen für die Nachrichten Konfiguration und den Anwendungs Entwurf, die bei der Verwendung der wwsapi-Nachrichten-API sorgfältig ausgewertet werden sollten:</span><span class="sxs-lookup"><span data-stu-id="610c7-293">Similarly, there are message configuration options and application design considerations that should be carefully evaluated when using WWSAPI Message API:</span></span>

-   <span data-ttu-id="610c7-294">Die Größe des Heaps, der zum Speichern der Header einer Nachricht verwendet wird, kann mithilfe der Eigenschaft [**\_ \_ \_ Eigenschaften Heap \_ Eigenschaften von WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) -Nachrichten konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-294">The size of the heap used to store the headers of a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_HEAP\_PROPERTIES**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="610c7-295">Wenn Sie diesen Wert erhöhen, kann mehr Arbeitsspeicher von den Headern der Nachricht genutzt werden, was zu OOM führen kann.</span><span class="sxs-lookup"><span data-stu-id="610c7-295">Increasing this value allows more memory to be consumed by the headers of the message, which can lead to OOM.</span></span>
-   <span data-ttu-id="610c7-296">Der Benutzer des Message-Objekts muss erkennen, dass die Header Zugriffs-APIs in Bezug auf die Anzahl der Header in der Nachricht O (n) sind, da Sie auf Duplikate überprüfen.</span><span class="sxs-lookup"><span data-stu-id="610c7-296">The user of the message object must realize that the header access APIs are O(n) with respect to the number of headers in the message, since they check for duplicates.</span></span> <span data-ttu-id="610c7-297">Entwürfe, bei denen viele Header in einer Nachricht erforderlich sind, können zu einer übermäßigen CPU-Auslastung führen.</span><span class="sxs-lookup"><span data-stu-id="610c7-297">Designs which require many headers in a message may lead to excessive CPU usage.</span></span>
-   <span data-ttu-id="610c7-298">Die maximale Anzahl von Headern in einer Nachricht kann mithilfe der Eigenschaft [**Eigenschaft \_ \_ Max. \_ \_ verarbeitete \_ Header der WS-Nachrichten Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="610c7-298">The maximum number of headers in a message can be configured using the [**WS\_MESSAGE\_PROPERTY\_MAX\_PROCESSED\_HEADERS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) property.</span></span> <span data-ttu-id="610c7-299">Es gibt auch einen impliziten Grenzwert, der auf der Größe des Heaps der Nachricht basiert.</span><span class="sxs-lookup"><span data-stu-id="610c7-299">There is also an implicit limit based on the size of the heap of the message.</span></span> <span data-ttu-id="610c7-300">Wenn beide Werte vergrößert werden, können mehr Header vorhanden sein, wodurch die erforderliche Zeit für die Suche nach einem Header (bei Verwendung der Header Zugriffs-APIs) anwächst.</span><span class="sxs-lookup"><span data-stu-id="610c7-300">Increasing both of these values allows more headers to be present, which compounds the time necessary to find a header (when using the header access APIs).</span></span>

 

 




