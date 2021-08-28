---
title: Kanal (Windows Webdienste)
description: Kanäle kapseln einen Kommunikationskontext zwischen zwei oder mehr Parteien und werden zum Senden und Empfangen von Nachrichten verwendet.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Kanalwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff11601f372416527f1d521f8fb9880c98821f9421b633f9eed059cc5b4f672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026648"
---
# <a name="channel-windows-web-services"></a>Kanal (Windows Webdienste)

Kanäle kapseln einen Kommunikationskontext zwischen zwei oder mehr Parteien und werden zum Senden und Empfangen von Nachrichten verwendet.


Verwenden Sie auf dem Client [**WsCreateChannel,**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) um einen Kanal zu erstellen. Verwenden Sie auf dem Server [**WsCreateChannelForListener,**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) um einen Kanal zu erstellen, der vom Client mithilfe eines [Listeners](listener.md)akzeptiert werden kann.

Wenn Sie einen Kanal erstellen, geben Sie die folgenden Informationen an, die sowohl das lokale Verhalten des Kanals als auch das zu verwendende Wire Protocol bestimmen.

-   Ein [**\_ WS-KANALTYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type), der das Nachrichtenaustauschmuster des Kanals identifiziert.
-   Eine [**\_ WS-KANALBINDUNG, \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)die das zu verwendende Übertragungsprotokoll identifiziert.
-   Eine [**\_ WS-SICHERHEITSBESCHREIBUNG, \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)die die für den Kanal verwendete Sicherheit angibt. Beim Erstellen von Kanälen für die Verwendung auf einem Server wird dies einmal für alle Kanäle angegeben, die für einen bestimmten Listener akzeptiert werden.
-   Eine Gruppe von [**WS \_ CHANNEL \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, die zusätzliche optionale Einstellungen angeben (eine Liste dieser Einstellungen finden Sie in den [**WS \_ CHANNEL PROPERTY \_ \_ ID-Enumerationen).**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)

Bevor Sie den Kanal verwenden, müssen Sie ihn öffnen, indem Sie die [**WsOpenChannel-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) aufrufen und den Kanal und die [Endpunktadresse](endpoint-address.md)sowie andere optionale Informationen angeben.

Informationen zu den Statusübergängen für einen Kanal finden Sie im Thema [**Kanalzustände.**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)

Weitere Informationen zu Kanälen finden Sie im Thema Übersicht über die [Kanalebene.](channel-layer-overview.md)

Die folgenden API-Elemente werden mit Kanälen verwendet.

| Rückruf                                                                                  | Beschreibung                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ ABANDON \_ MESSAGE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Verarbeitet den [**WsAbtaxinMessage-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) für einen Kanal mit benutzerdefinierter Kanalbindung.                                              |
| [**WS \_ ABORT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Verarbeitet den [**WsAbortChannel-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) für einen Kanal mit benutzerdefinierter Kanalbindung.                                                  |
| [**WS \_ CLOSE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Verarbeitet den [**WsCloseChannel-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) für einen Kanal mit benutzerdefinierter Kanalbindung.                                                  |
| [**WS \_ CREATE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Verarbeitet den [**WsCloseChannel-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) für einen Kanal mit benutzerdefinierter Kanalbindung.                                                  |
| [**WS \_ CREATE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Behandelt das Erstellen einer Decoderinstanz.                                                                                                                  |
| [**WS \_ CREATE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Behandelt das Erstellen einer Encoderinstanz.                                                                                                                 |
| [**\_ \_ WS-DECODERDECODIERUNGSRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Decodiert eine Nachricht.                                                                                                                                    |
| [**ENDRÜCKRUF DES \_ WS-DECODERS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Decodiert das Ende einer Nachricht.                                                                                                                         |
| [**WS-DECODER \_ \_ RUFT DEN \_ \_ \_ INHALTSTYPRÜCKRUF AB**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Ruft den Inhaltstyp der Nachricht ab.                                                                                                                 |
| [**STARTRÜCKRUF DES \_ WS-DECODERS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Beginnt mit der Decodierung einer Nachricht.                                                                                                                            |
| [**WS \_ \_ ENCODER-CODIERUNGSRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Codiert eine Nachricht.                                                                                                                                    |
| [**WS \_ ENCODER \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Codiert das Ende einer Nachricht.                                                                                                                         |
| [**WS \_ ENCODER \_ GET \_ CONTENT \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Ruft den Inhaltstyp der Nachricht ab.                                                                                                                 |
| [**WS \_ ENCODER \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Startet die Codierung einer Nachricht.                                                                                                                            |
| [**WS \_ FREE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Verarbeitet den [**WsFreeChannel-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) für einen Kanal mit benutzerdefinierter Kanalbindung.                                                    |
| [**RÜCKRUF DES \_ KOSTENLOSEN WS-DECODERS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Behandelt das Freigeben einer Decoderinstanz.                                                                                                                   |
| [**WS \_ FREE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Behandelt das Freigeben einer Encoderinstanz.                                                                                                                  |
| [**WS \_ GET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Verarbeitet den [**WsGetChannelProperty-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) für einen Kanal mit benutzerdefinierter Kanalbindung.                                      |
| [**\_ \_ WS-HTTP-UMLEITUNGSRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Wird aufgerufen, wenn eine Nachricht automatisch an einen anderen Dienst umgeleitet werden soll, indem die automatische HTTP-Umleitungsfunktion verwendet wird, wie in RFC2616 beschrieben. |
| [**WS \_ OPEN \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Verarbeitet den [**WsOpenChannel-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) für einen Kanal mit benutzerdefinierter Kanalbindung.                                                    |
| [**WS \_ READ \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Verarbeitet den [**WsReadMessageEnd-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) für einen Kanal mit benutzerdefinierter Kanalbindung.                                              |
| [**WS \_ READ \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Verarbeitet den [**WsReadMessageEnd-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) für einen Kanal mit benutzerdefinierter Kanalbindung.                                              |
| [**RÜCKRUF DES \_ WS-ZURÜCKSETZUNGSKANALS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Verarbeitet den [**WsResetChannel-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) für einen Kanal mit benutzerdefinierter Kanalbindung.                                                  |
| [**WS \_ SET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Verarbeitet den [**WsSetChannelProperty-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) für einen Kanal mit benutzerdefinierter Kanalbindung.                                      |
| [**WS \_ SHUTDOWN \_ SESSION \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Verarbeitet den [**WsShutdownSessionChannel-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) für einen Kanal mit benutzerdefinierter Kanalbindung.                              |
| [**WS \_ WRITE \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Verarbeitet den [**WsWriteMessageEnd-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) für einen Kanal mit benutzerdefinierter Kanalbindung.                                            |
| [**WS \_ WRITE \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Verarbeitet den [**WsWriteMessageStart-Aufruf**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) für einen Kanal mit benutzerdefinierter Kanalbindung.                                        |



 



| Enumeration                                                 | Beschreibung                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_WS-KANALBINDUNG \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Gibt den Protokollstapel an, der für den Kanal verwendet werden soll.                                                                                      |
| [**\_ \_ WS-KANALEIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Identifiziert jede Kanaleigenschaft durch eine ID.                                                                                                |
| [**\_WS-KANALSTATUS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | Der Zustand des Kanals.                                                                                                                 |
| [**\_WS-KANALTYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Gibt die grundlegenden Merkmale des Kanals an, z. B. ob er sitzungsvoll ist und welche Kommunikationsrichtungen unterstützt werden. |
| [**\_WS-CODIERUNG**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | Die verschiedenen Codierungen (Nachrichtenformate).                                                                                                |
| [**\_WS-EMPFANGSOPTION \_**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Gibt an, ob eine Nachricht erforderlich ist, wenn sie von einem Kanal empfangen wird.                                                                    |
| [**\_WS-ÜBERTRAGUNGSMODUS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Gibt an, ob gesendete oder empfangene Nachrichten gestreamt oder gepuffert werden.                                                            |



 



| Funktion                                                         | Beschreibung                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**WsAbtaxinMessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Überspringt den Rest einer Nachricht für einen Kanal.                                                              |
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Bricht alle ausstehenden E/A-Sätze in einem angegebenen Kanal ab und legt den Kanalzustand auf **WS \_ CHANNEL STATE \_ \_ FAULTED fest.** |
| [**WsCloseChannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Schließt einen Kanal, wenn er nicht mehr benötigt wird.                                                                |
| [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Erstellt einen Kanal.                                                                                           |
| [**WsCreateChannelForListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Erstellt einen Kanal für einen Listener.                                                                            |
| [**WsFreeChannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Gibt die einem Kanal zugeordneten Arbeitsspeicherressourcen frei.                                                     |
| [**WsGetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Ruft eine Eigenschaft des Kanals ab, auf den vom Channelparameter verwiesen wird.                                     |
| [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Öffnet einen Kanal zu einem Endpunkt.                                                                              |
| [**WsReadMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Liest die schließenden Elemente einer Nachricht aus einem Kanal.                                                      |
| [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Liest die Header der nächsten Nachricht aus dem Kanal und bereitet das Lesen der Textelemente vor.               |
| [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Empfängt eine Nachricht und deserialisiert den Nachrichtentext als Wert.                                      |
| [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Sendet eine Anforderungsnachricht und empfängt eine korrelierte Antwortnachricht.                                             |
| [**WsResetChannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Setzen Sie einen Kanal zurück, damit er wiederverwendet werden kann.                                                                         |
| [**WsSendMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Sendet eine Nachricht in einem Kanal mithilfe der Serialisierung, um das Textelement zu schreiben.                                  |
| [**WsSendReplyMessage**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Sendet eine Nachricht, die eine Antwort auf eine empfangene Nachricht ist.                                                       |
| [**WsSetChannelProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Legt eine Eigenschaft eines Kanals fest.                                                                                |
| [**WsSetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Legt eine Eigenschaft einer Nachricht fest.                                                                                |
| [**WsWriteMessageEnd**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Schreibt die schließenden Elemente einer Nachricht in den Kanal.                                                     |
| [**WsWriteMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Schreiben Sie die Header einer Nachricht in den Kanal, und bereiten Sie das Schreiben der Textelemente vor.                   |



 



| Handle                        | Beschreibung                                 |
|-------------------------------|---------------------------------------------|
| [\_WS-KANAL](ws-channel.md) | Ein nicht transparenter Typ, der verwendet wird, um auf einen Kanal zu verweisen. |



 



| Struktur                                                                          | Beschreibung                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_WS-KANALDECODER \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Eine Reihe von Rückrufen, die den Inhaltstyp und codierte Bytes einer empfangenen Nachricht transformieren.                                                                                                      |
| [**\_ \_ WS-KANALENCODER**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Eine Reihe von Rückrufen, die den Inhaltstyp und codierte Bytes einer gesendeten Nachricht transformieren können.                                                                                                      |
| [**\_WS-KANALEIGENSCHAFTEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Eine Reihe von [**WS \_ CHANNEL \_ PROPERTY-Strukturen.**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                                                                                                                        |
| [**\_WS-KANALEIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Eine kanalspezifische Einstellung.                                                                                                                                                                      |
| [**\_BENUTZERDEFINIERTE \_ WS-KANALRÜCKRUFE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Eine Reihe von Rückrufen, die die Implementierung eines benutzerdefinierten Kanals bilden.                                                                                                                             |
| [**\_BENUTZERDEFINIERTER \_ WS-HTTP-PROXY \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | wird verwendet, um den benutzerdefinierten Proxy für den Kanal mithilfe des **\_ \_ \_ BENUTZERDEFINIERTEN \_ HTTP-PROXYwerts** \_ der [**WS \_ CHANNEL PROPERTY \_ \_ ID-Enumeration**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) anzugeben. |
| [**\_WS-HTTP-HEADERZUORDNUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Stellt einen einzelnen Header dar, der als Teil der [**\_ WS-HTTP-NACHRICHTENZUORDNUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)zugeordnet wird.                                                                         |
| [**\_WS-HTTP-NACHRICHTENZUORDNUNG \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Informationen dazu, wie eine HTTP-Anforderung oder -Antwort in einem Nachrichtenobjekt dargestellt werden soll.                                                                                                     |
| [**\_ \_ WS-HTTP-UMLEITUNGSRÜCKRUFKONTEXT \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Gibt die Rückruffunktion und den Zustand zum Steuern des Verhaltens der automatischen HTTP-Umleitung an.                                                                                               |
| [**\_WS-NACHRICHTENBESCHREIBUNG \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | Das Schema für die Eingabe und Ausgabe von [WS \_ MESSAGE](ws-message.md) für eine bestimmte Vorgangsbeschreibung.                                                                                             |



 

 

 




