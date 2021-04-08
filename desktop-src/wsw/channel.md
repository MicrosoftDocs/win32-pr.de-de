---
title: Channel (Windows-Webdienste)
description: Kanäle Kapseln einen Kommunikationskontext zwischen zwei oder mehr Parteien und werden verwendet, um Nachrichten zu senden und zu empfangen.
ms.assetid: 5a04580d-c89f-4505-a4b7-0724ffb788fd
keywords:
- Kanalweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93819057f2de4ecf82b2def9cdc4fe14dd1b0ee
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103949346"
---
# <a name="channel-windows-web-services"></a>Channel (Windows-Webdienste)

Kanäle Kapseln einen Kommunikationskontext zwischen zwei oder mehr Parteien und werden verwendet, um Nachrichten zu senden und zu empfangen.


Verwenden Sie auf dem Client [**wscreatechannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) , um einen Kanal zu erstellen. Verwenden Sie auf dem Server [**wscreatechannelforlistener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) , um einen Kanal zu erstellen, der vom Client mithilfe eines [Listener](listener.md)akzeptiert werden kann.

Wenn Sie einen Kanal erstellen, geben Sie die folgenden Informationen an, die sowohl das lokale Verhalten des Kanals als auch das zu verwendende Wire-Protokoll bestimmen.

-   Ein [**WS \_ - \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type), der das Nachrichtenaustausch Muster des Kanals bezeichnet.
-   Eine [**WS \_ - \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), die das zu verwendende Übertragungsprotokoll identifiziert.
-   Eine [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), die die für den Kanal verwendete Sicherheit angibt. Beim Erstellen von Kanälen für die Verwendung auf einem Server wird dies einmal für alle Kanäle angegeben, die für einen bestimmten Listener akzeptiert werden.
-   Eine [**\_ \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)zum Festlegen von WS-Kanälen, die zusätzliche optionale Einstellungen angeben (eine Liste dieser Einstellungen finden Sie unter den Enumerationen der [**WS- \_ \_ Channeleigenschaft- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) ).

Bevor Sie den Kanal verwenden, müssen Sie ihn öffnen, indem Sie die [**wsopenchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) -Funktion aufrufen und die Kanal-und [Endpunkt Adresse](endpoint-address.md)zusammen mit anderen optionalen Informationen angeben.

Informationen zu den Status Übergängen für einen Kanal finden Sie im Thema [**channelstates**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state) .

Weitere Informationen zu Kanälen finden Sie im Thema [Übersicht über die Kanal Schicht](channel-layer-overview.md) .

Die folgenden API-Elemente werden mit Kanälen verwendet.

| Rückruf                                                                                  | BESCHREIBUNG                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS-Abbruch \_ \_ Nachrichten \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)                     | Behandelt den [**wsabandonmessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage) -Aufrufe für einen Kanal mit benutzerdefinierter channelbindung.                                              |
| [**WS- \_ Abbruch \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)                         | Behandelt den [**wsabortchannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel) -Aufrufe für einen Kanal mit benutzerdefinierter channelbindung.                                                  |
| [**WS- \_ Schluss \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)                         | Behandelt den [**wsclosechannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) -Befehl für einen Kanal mit benutzerdefinierter channelbindung.                                                  |
| [**WS \_ Create \_ Channel- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)                       | Behandelt den [**wsclosechannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel) -Befehl für einen Kanal mit benutzerdefinierter channelbindung.                                                  |
| [**WS-Erstellungs \_ \_ Decoder- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)                       | Behandelt das Erstellen einer decoderinstanz.                                                                                                                  |
| [**WS \_ - \_ \_ codierungsrückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)                       | Behandelt das Erstellen einer encoderinstanz.                                                                                                                 |
| [**WS \_ - \_ decoderdecodierungsrückruf \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)                       | Decodiert eine Meldung.                                                                                                                                    |
| [**WS \_ - \_ decoderende- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)                             | Decodiert das Ende einer Nachricht.                                                                                                                         |
| [**WS- \_ Decoder \_ get- \_ \_ Inhaltstyp \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback) | Ruft den Inhaltstyp der Nachricht ab.                                                                                                                 |
| [**WS \_ - \_ decoderstart \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)                         | Startet das Decodieren einer Nachricht.                                                                                                                            |
| [**WS- \_ Encoder-Codierungs \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)                       | Codiert eine Nachricht.                                                                                                                                    |
| [**WS- \_ Encoder- \_ End- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)                             | Codiert das Ende einer Nachricht.                                                                                                                         |
| [**WS- \_ Encoder \_ get- \_ \_ Inhaltstyp \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback) | Ruft den Inhaltstyp der Nachricht ab.                                                                                                                 |
| [**WS- \_ Encoder- \_ Start \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)                         | Startet das Codieren einer Nachricht.                                                                                                                            |
| [**WS \_ - \_ freier \_ channelrückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)                           | Verarbeitet den [**wsfrechannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel) -Aufrufe für einen Kanal mit benutzerdefinierter channelbindung.                                                    |
| [**WS- \_ freier \_ Decoder- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)                           | Behandelt das Freigeben einer decoderinstanz.                                                                                                                   |
| [**WS \_ Free \_ Encoder- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)                           | Behandelt das Freigeben einer encoderinstanz.                                                                                                                  |
| [**Rückruf für WS- \_ get- \_ Kanal \_ Eigenschaft \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)          | Verarbeitet den [**wsgetchannelproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty) -Aufrufe für einen Kanal mit benutzerdefinierter channelbindung.                                      |
| [**WS- \_ http- \_ Umleitungs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)                         | Wird aufgerufen, wenn eine Nachricht automatisch an einen anderen Dienst umgeleitet wird, indem HTTP-Funktionen für die automatische Umleitung, wie in rfc2616 beschrieben, genutzt werden. |
| [**WS- \_ Open- \_ Channel- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)                           | Behandelt den [**wsopkanchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) -Aufrufe für einen Kanal mit benutzerdefinierter channelbindung.                                                    |
| [**WS- \_ Lese \_ Nachrichten Ende- \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)                  | Behandelt den [**wsread messageend**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) -Aufrufe für einen Kanal mit benutzerdefinierter channelbindung.                                              |
| [**WS \_ - \_ lesenachrichten- \_ Start \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)              | Behandelt den [**wsread messageend**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend) -Aufrufe für einen Kanal mit benutzerdefinierter channelbindung.                                              |
| [**WS-rücksetzungs \_ \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)                         | Behandelt den [**wsresetchannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel) -aufrufen für einen Kanal mit benutzerdefinierter channelbindung.                                                  |
| [**Rückruf für die WS- \_ Satz \_ Kanal \_ Eigenschaft \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)          | Behandelt den [**wssetchannelproperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty) -Befehl für einen Kanal mit benutzerdefinierter channelbindung.                                      |
| [**WS \_ - \_ Sitzungs \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)  | Behandelt den [**wsshutdownsessionchannel**](/windows/desktop/api/WebServices/nf-webservices-wsshutdownsessionchannel) -Befehl für einen Kanal mit benutzerdefinierter channelbindung.                              |
| [**WS- \_ Write- \_ Nachrichten Ende- \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)                | Behandelt den [**wswrite-essageend**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend) -Aufrufe für einen Kanal mit benutzerdefinierter channelbindung.                                            |
| [**WS- \_ Schreib \_ Nachrichten Start- \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)            | Behandelt den [**wswrite-essagestart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart) -Befehl für einen Kanal mit benutzerdefinierter channelbindung.                                        |



 



| Enumeration                                                 | Beschreibung                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS- \_ Kanal \_ Bindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)          | Gibt den Protokollstapel an, der für den Kanal verwendet werden soll.                                                                                      |
| [**ID der WS- \_ Kanal \_ Eigenschaft \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) | Identifiziert jede Kanal Eigenschaft durch eine ID.                                                                                                |
| [**Status des WS- \_ Kanals \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_state)              | Der Status des Kanals.                                                                                                                 |
| [**WS \_ - \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)                | Gibt die grundlegenden Eigenschaften des Kanals an, z. b. ob er Sitzungs basiert ist und welche Kommunikations Richtungen unterstützt werden. |
| [**WS- \_ Codierung**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding)                         | Die verschiedenen Codierungen (Nachrichtenformate).                                                                                                |
| [**WS \_ Receive- \_ Option**](/windows/desktop/api/WebServices/ne-webservices-ws_receive_option)            | Gibt an, ob beim Empfang von einem Kanal eine Meldung erforderlich ist.                                                                    |
| [**WS- \_ Übertragungs \_ Modus**](/windows/desktop/api/WebServices/ne-webservices-ws_transfer_mode)              | Gibt an, ob gesendete oder empfangene Nachrichten gestreamt oder gepuffert werden.                                                            |



 



| Funktion                                                         | BESCHREIBUNG                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Wsabandonmessage**](/windows/desktop/api/WebServices/nf-webservices-wsabandonmessage)                     | Überspringt den Rest einer Nachricht für einen Kanal.                                                              |
| [**Wsabortchannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)                         | Bricht alle ausstehenden e/a-Vorgänge auf einem angegebenen Kanal ab und legt den Kanalstatus auf den **WS- \_ Kanal \_ Status \_** Fehler fest. |
| [**Wsclosechannel**](/windows/desktop/api/WebServices/nf-webservices-wsclosechannel)                         | Schließt einen Kanal, wenn er nicht mehr benötigt wird.                                                                |
| [**Wscreatechannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel)                       | Erstellt einen Kanal.                                                                                           |
| [**Wscreatechannelforlistener**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannelforlistener) | Erstellt einen Kanal für einen Listener.                                                                            |
| [**Wsfrechannel**](/windows/desktop/api/WebServices/nf-webservices-wsfreechannel)                           | Gibt die einem Kanal zugeordneten Speicherressourcen frei.                                                     |
| [**Wsgetchannelproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetchannelproperty)             | Ruft eine Eigenschaft des Kanals ab, auf den vom Channel-Parameter verwiesen wird.                                     |
| [**Wsopumchannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)                           | Öffnet einen Kanal zu einem Endpunkt.                                                                              |
| [**Wslesmessageend**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessageend)                     | Liest die schließenden Elemente einer Nachricht aus einem Kanal.                                                      |
| [**Wsummessagestart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart)                 | Liest die Header der nächsten Nachricht aus dem Kanal und bereitet das Lesen der Textelemente vor.               |
| [**Wsreceivemess**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage)                     | Empfängt eine Nachricht und deserialisiert den Text der Nachricht als-Wert.                                      |
| [**Wsrequestreply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply)                         | Sendet eine Anforderungs Nachricht und empfängt eine korrelierte Antwortnachricht.                                             |
| [**Wsresetchannel**](/windows/desktop/api/WebServices/nf-webservices-wsresetchannel)                         | Setzen Sie einen Kanal zurück, damit er wieder verwendet werden kann.                                                                         |
| [**Wssendmessage**](/windows/desktop/api/WebServices/nf-webservices-wssendmessage)                           | Sendet eine Nachricht über einen Kanal mithilfe der Serialisierung, um das Body-Element zu schreiben.                                  |
| [**Wssendreplymess**](/windows/desktop/api/WebServices/nf-webservices-wssendreplymessage)                 | Sendet eine Nachricht, bei der es sich um eine Antwort auf eine empfangene Nachricht handelt.                                                       |
| [**Wssetchannelproperty**](/windows/desktop/api/WebServices/nf-webservices-wssetchannelproperty)             | Legt eine Eigenschaft eines Kanals fest.                                                                                |
| [**Wssetmessageproperty**](/windows/desktop/api/WebServices/nf-webservices-wssetmessageproperty)             | Legt eine Eigenschaft einer Nachricht fest.                                                                                |
| [**Wsschreitemessageend**](/windows/desktop/api/WebServices/nf-webservices-wswritemessageend)                   | Schreibt die schließenden Elemente einer Nachricht in den Kanal.                                                     |
| [**Wsschreitemessagestart**](/windows/desktop/api/WebServices/nf-webservices-wswritemessagestart)               | Schreiben Sie die Header einer Nachricht in den Kanal, und bereiten Sie das Schreiben der Textelemente vor.                   |



 



| Handle                        | BESCHREIBUNG                                 |
|-------------------------------|---------------------------------------------|
| [WS- \_ Kanal](ws-channel.md) | Ein nicht transparenter Typ, der zum Verweisen auf einen Kanal verwendet wird. |



 



| Struktur                                                                          | BESCHREIBUNG                                                                                                                                                                                      |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS- \_ Kanal- \_ Decoder**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_decoder)                                 | Ein Satz von Rückrufen, die den Inhaltstyp und codierte Bytes einer empfangenen Nachricht transformieren.                                                                                                      |
| [**WS- \_ Kanal \_ Encoder**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_encoder)                                 | Ein Satz von Rückrufen, die den Inhaltstyp und codierte Bytes einer gesendeten Nachricht transformieren können.                                                                                                      |
| [**Eigenschaften des WS- \_ Kanals \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_properties)                           | Eine Reihe von [**WS- \_ Kanal \_ Eigenschafts**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) Strukturen.                                                                                                                        |
| [**WS \_ - \_ Channeleigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)                               | Eine Kanal spezifische Einstellung.                                                                                                                                                                      |
| [**\_benutzerdefinierte WS-channelrückrufe \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_channel_callbacks)              | Ein Satz von Rückrufen, die die Implementierung eines benutzerdefinierten Kanals bilden.                                                                                                                             |
| [**\_benutzerdefinierter WS- \_ http- \_ Proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_http_proxy)                            | wird zum Angeben des benutzerdefinierten Proxys für den Kanal mithilfe des **\_ \_ \_ benutzerdefinierten \_ http**-Proxy Werts der WS-Kanal Eigenschaft \_ der WS- [**\_ \_ Channeleigenschaft- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id) -Enumeration verwendet. |
| [**WS- \_ http- \_ Header \_ Zuordnung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_mapping)                        | Stellt einen einzelnen Header dar, der als Teil der [**WS- \_ http- \_ Nachrichten \_ Zuordnung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)zugeordnet ist.                                                                         |
| [**WS- \_ http- \_ Nachrichten \_ Zuordnung**](/windows/desktop/api/WebServices/ns-webservices-ws_http_message_mapping)                      | Informationen dazu, wie eine HTTP-Anforderung oder-Antwort in einem Nachrichten Objekt dargestellt werden soll.                                                                                                     |
| [**WS- \_ http- \_ Umleitungs \_ Rückruf \_ Kontext**](/windows/desktop/api/WebServices/ns-webservices-ws_http_redirect_callback_context) | Gibt die Rückruffunktion und den Zustand zum Steuern des automatischen http-Umleitungs Verhaltens an.                                                                                               |
| [**Beschreibung der WS- \_ Nachricht \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_description)                         | Das Schema für die Eingabe-und Ausgabe- [WS- \_ Nachricht](ws-message.md) für eine angegebene Vorgangs Beschreibung.                                                                                             |



 

 

 




