---
title: Meldung (Windows-Webdienste)
description: Eine Nachricht ist ein Objekt, das übertragene oder empfangene Daten kapselt.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Message Web Services for Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1722cbe4a956ef16a1b7195158b695f551419ad600c64f552e92700d3e4ee57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657095"
---
# <a name="message-windows-web-services"></a>Meldung (Windows-Webdienste)

Eine Nachricht ist ein Objekt, das übertragene oder empfangene Daten kapselt. Die Struktur einer Nachricht wird durch SOAP definiert und enthält eine Reihe von Headern und einen Text. Die Header werden immer im Arbeitsspeicher gepuffert, aber der Text wird mit einer Streaming-API gelesen und geschrieben.

![Diagramm, das eine Meldung zeigt, bei der der Header gepuffert und der Text gestreamt wird.](images/messageenvelope.png)


Nachrichten verfügen über einen Satz von Eigenschaften, die verwendet werden können, um optionale Einstellungen anzugeben, die das Verhalten einer Nachricht steuern, und um eine Möglichkeit zum Abrufen zusätzlicher Informationen zu empfangenen Nachrichten (z. B. Sicherheitsinformationen) zu bieten. Eine vollständige Liste der Nachrichteneigenschaften finden Sie unter [**\_ \_ \_ EIGENSCHAFTEN-ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) der WS-NACHRICHT.

Eine Nachricht wird an eine bestimmte [Endpunktadresse adressiert.](endpoint-address.md)

Ein [**WS \_ FAULT ist**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) eine besondere Art von Nachrichteninhalt, mit dem Fehler von einem Remoteendpunkt zurückgegeben werden.

Nachrichten werden codiert, die den XML-Code vor der Übertragung in ein lineares Übertragungsformat transformieren.

Weitere Informationen zu Nachrichten finden Sie im Thema [Übersicht über die Kanalebene.](channel-layer-overview.md)

Die folgenden Beispiele veranschaulichen die Verwendung von Nachrichten in WWSAPI.

| Beispiel                                              | Beschreibung                                  |
|------------------------------------------------------|----------------------------------------------|
| [CustomHeaderExample](customheaderexample.md)       | Veranschaulicht die Verwendung benutzerdefinierter Nachrichtenheader.    |
| [MessageEncodingExample](messageencodingexample.md) | Veranschaulicht das Codieren und Decodieren einer Nachricht. |
| [ForwardMessageExample](forwardmessageexample.md)   | Veranschaulicht die Weiterleitung einer Nachricht.            |



 

Die folgenden API-Elemente werden mit Nachrichten verwendet.

| Rückruf                                                        | Beschreibung                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ MESSAGE \_ \_ DONE-RÜCKRUF**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Benachrichtigt den Aufrufer, dass die Verwendung der WS XML READER-Struktur, die für die WsReadEnvevesStart-Funktion bereitgestellt wurde, oder der WS XML WRITER-Struktur abgeschlossen wurde, die für die \_ \_ \_ \_ WsWriteEnvevesStart-Funktion bereitgestellt wurde. |



 



| Enumeration                                                      | Beschreibung                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**\_WS-ADRESSIERUNGSVERSION \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | Die Version der Spezifikation, die für die Adressierungsheader verwendet wird.                                        |
| [**\_WS-UMSCHLAGVERSION \_**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | Die Version der Spezifikation, die für die Umschlagstruktur verwendet wird.                                        |
| [**\_WS-HEADERATTRIBUTE \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Ein Satz von Flags, die die SOAP-Attribute "understand" und "relay" eines Headers darstellen.                    |
| [**\_WS-HEADERTYP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | Der Typ des Headers.                                                                                  |
| [**\_WS-NACHRICHTENIN \_ INITIALISIERUNG**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Gibt an, welche Header [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) der Nachricht hinzufügen soll. |
| [**\_ \_ WS-NACHRICHTENEIGENSCHAFTS-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | Die ID jeder Nachrichteneigenschaft.                                                                         |
| [**\_WS-NACHRICHTENSTATUS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | Der Status der Nachricht.                                                                                |



 



| Funktion                                                             | Beschreibung                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Weist einer Nachricht eine Zieladresse zu.                                                                                                            |
| [**WsCheckMustUnderstandHeaders**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Überprüft, ob der Empfänger die angegebenen Header richtig verstanden hat.                                                                         |
| [**WsCreateMessage**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Erstellt eine Instanz eines [WS \_ MESSAGE-Objekts.](ws-message.md)                                                                                         |
| [**WsCreateMessageForChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Erstellt eine Meldung, die für die Verwendung mit einem bestimmten Kanal geeignet ist.                                                                                 |
| [**WsFillBody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Stellt sicher, dass in einer Nachricht eine ausreichende Anzahl von Bytes zum Lesen verfügbar ist.                                                                |
| [**WsFlushBody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Leert alle akkumulierten Nachrichtentextdaten, die geschrieben wurden.                                                                                       |
| [**WsFreeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Gibt die einer Nachricht zugeordnete Speicherressource frei.                                                                                                |
| [**WsGetCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Sucht den anwendungsdefinierten Header der Nachricht und deserialisiert ihn.                                                                               |
| [**WsGetHeader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Sucht einen bestimmten Standardheader in der Nachricht und deserialisiert ihn.                                                                                 |
| [**WsGetHeaderAttributes**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Füllt einen ULONG-Parameter mit [**den WS \_ HEADER \_ ATTRIBUTES aus**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) dem Headerelement auf, auf dem der Reader positioniert ist. |
| [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Ruft eine angegebene Message-Objekteigenschaft ab.                                                                                                         |
| [**WsInitializeMessage**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Initialisiert die Header für die Nachricht als Vorbereitung für die Verarbeitung.                                                                                 |
| [**WsMarkHeaderAsUnderstood**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Markiert einen Header als von der Anwendung verstanden.                                                                                                       |
| [**WsReadBody**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Deserialisiert einen Wert aus dem XML-Reader der Nachricht.                                                                                               |
| [**WsReadEnvevesEnd**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Liest die schließenden Elemente einer Nachricht.                                                                                                               |
| [**WsReadEnvevesStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Liest die Header der Nachricht und bereitet das Lesen der Textelemente vor.                                                                               |
| [**WsRemoveCustomHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Entfernt einen benutzerdefinierten Header aus der Nachricht.                                                                                                              |
| [**WsRemoveHeader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Entfernt das [**WS \_ HEADER \_ TYPE-Standardobjekt**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) aus einer Nachricht.                                                                 |
| [**WsResetMessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Legt den Nachrichtenzustand wieder auf **WS \_ MESSAGE STATE \_ EMPTY \_ fest.**                                                                                          |
| [**WsSetHeader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Fügt den angegebenen Standardheader in der Nachricht hinzu oder ersetzt ihn.                                                                                         |
| [**WsWriteBody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Schreibt einen Wert in den Text einer Nachricht.                                                                                                               |
| [**WsWriteEnvevesEnd**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Schreibt die schließenden Elemente einer Nachricht.                                                                                                              |
| [**WsWriteEnvevesStart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Schreibt den Anfang der Nachricht einschließlich des aktuellen Sets von Headern der Nachricht und bereitet das Schreiben der Textelemente vor.                           |



 



| Handle                        | Beschreibung                                         |
|-------------------------------|-----------------------------------------------------|
| [\_WS-NACHRICHT](ws-message.md) | Der nicht transparente Typ, der verwendet wird, um auf ein Nachrichtenobjekt zu verweisen. |



 



| Struktur                                                | Beschreibung                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_WS-FEHLER**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Ein Fehlerwert, der im Text einer Nachricht enthalten ist und auf einen Verarbeitungsfehler hinweist. |
| [**\_WS-FEHLERCODE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Stellt einen Fehlercode dar.                                                             |
| [**\_WS-FEHLERURSACHE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Enthält eine Erläuterung des Fehlers.                                                |
| [**\_WS-NACHRICHTENEIGENSCHAFTEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Gibt einen Satz von [**WS \_ MESSAGE \_ PROPERTY-Strukturen**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property) an.  |
| [**WS \_ \_ MESSAGE-EIGENSCHAFT**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Gibt eine nachrichtenspezifische Einstellung an.                                                |



 

 

 




