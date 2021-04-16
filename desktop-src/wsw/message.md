---
title: Meldung (Windows-Webdienste)
description: Bei einer Nachricht handelt es sich um ein Objekt, das übertragene oder empfangene Daten kapselt.
ms.assetid: edc810d9-7d78-4b79-8cbb-e87401f6ae41
keywords:
- Nachrichtenweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704df318e10521bd56e62632af16e683b7baccfc
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104559159"
---
# <a name="message-windows-web-services"></a>Meldung (Windows-Webdienste)

Bei einer Nachricht handelt es sich um ein Objekt, das übertragene oder empfangene Daten kapselt. Die Struktur einer Nachricht wird von SOAP definiert und enthält eine Reihe von Headern und Text. Die Header werden immer im Arbeitsspeicher gepuffert, aber der Text wird mit einer Streaming-API gelesen und geschrieben.

![Das Diagramm zeigt eine Meldung mit dem gepufferten Header und dem Text, der gestreamt wird.](images/messageenvelope.png)


Nachrichten verfügen über eine Reihe von Eigenschaften, die verwendet werden können, um optionale Einstellungen anzugeben, die das Verhalten einer Nachricht steuern, und um eine Möglichkeit bereitzustellen, zusätzliche Informationen über empfangene Nachrichten (z. b. Sicherheitsinformationen) abzurufen. Eine umfassende Liste der Nachrichten Eigenschaften finden Sie unter [**WS- \_ Nachrichten eigen schafts- \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) .

Eine Nachricht wird an eine bestimmte [Endpunkt Adresse](endpoint-address.md)adressiert.

Ein [**WS- \_ Fehler**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) ist eine besondere Art von Nachrichten Inhalt, der zur Darstellung von Fehlern verwendet wird, die von einem Remote Endpunkt zurückgegeben werden.

Nachrichten werden durch eine Codierung unterzogen, die den XML-Code vor der Übertragung in ein lineares Format

Weitere Informationen zu Nachrichten finden Sie im Thema Übersicht über die [Kanal Schicht](channel-layer-overview.md) .

In den folgenden Beispielen wird die Verwendung von Nachrichten in wwsapi veranschaulicht.

| Beispiel                                              | BESCHREIBUNG                                  |
|------------------------------------------------------|----------------------------------------------|
| [Customheaderexample](customheaderexample.md)       | Veranschaulicht die Verwendung benutzerdefinierter Nachrichten Header.    |
| [MessageEncodingExample](messageencodingexample.md) | Veranschaulicht das Codieren und Decodieren einer Nachricht. |
| [Forwardmessageexample](forwardmessageexample.md)   | Veranschaulicht das Weiterleiten einer Nachricht.            |



 

Die folgenden API-Elemente werden mit Nachrichten verwendet.

| Rückruf                                                        | BESCHREIBUNG                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Rückruf für WS- \_ Nachricht \_ abgeschlossen \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback) | Benachrichtigt den Aufrufer, dass die Nachricht die Verwendung der WS-XML-readerstruktur abgeschlossen hat, die \_ \_ für die wsleenvelopestart-Funktion bereitgestellt wurde, oder der WS \_ XML Writer-Struktur, die \_ für die wsschreiteenvelopestart-Funktion bereitgestellt wurde. |



 



| Enumeration                                                      | Beschreibung                                                                                              |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**WS- \_ Adressierungs \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)         | Die Version der Spezifikation, die für die Adressierungs Header verwendet wird.                                        |
| [**WS- \_ Umschlag \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_envelope_version)             | Die Version der Spezifikation, die für die Umschlag Struktur verwendet wird.                                        |
| [**WS- \_ Header \_ Attribute**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type)           | Ein Satz von Flags, die die SOAP MustUnderstand-und relayattribute eines Headers darstellen.                    |
| [**WS \_ - \_ Headertyp**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type)                       | Der Typ des Headers.                                                                                  |
| [**WS- \_ Nachrichten \_ Initialisierung**](/windows/desktop/api/WebServices/ne-webservices-ws_message_initialization) | Gibt an, welche Header das [**wsinitializemess**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage) der Nachricht hinzufügen soll. |
| [**WS- \_ Nachrichten \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id)      | Die ID der einzelnen Nachrichten Eigenschaften.                                                                         |
| [**WS- \_ Nachrichten \_ Status**](/windows/desktop/api/WebServices/ne-webservices-ws_message_state)                   | Der Status der Nachricht.                                                                                |



 



| Funktion                                                             | BESCHREIBUNG                                                                                                                                            |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wsaddressmessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage)                         | Weist einer Nachricht eine Zieladresse zu.                                                                                                            |
| [**Wscheckmustverständlicherweise-Header**](/windows/desktop/api/WebServices/nf-webservices-wscheckmustunderstandheaders) | Überprüft, ob die angegebenen Header vom Empfänger entsprechend verstanden wurden.                                                                         |
| [**Wscreatemess Age**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessage)                           | Erstellt eine Instanz eines [WS- \_ Nachrichten](ws-message.md) Objekts.                                                                                         |
| [**Wscreatemessageforchannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatemessageforchannel)       | Erstellt eine Meldung, die für die Verwendung mit einem bestimmten Kanal geeignet ist.                                                                                 |
| [**Wsfillbody**](/windows/desktop/api/WebServices/nf-webservices-wsfillbody)                                     | Stellt sicher, dass eine ausreichende Anzahl von Bytes in einer Nachricht zum Lesen verfügbar ist.                                                                |
| [**Wsflushbody**](/windows/desktop/api/WebServices/nf-webservices-wsflushbody)                                   | Leert alle gesammelten Nachrichtentext Daten, die geschrieben wurden.                                                                                       |
| [**Wsfreemess Age**](/windows/desktop/api/WebServices/nf-webservices-wsfreemessage)                               | Gibt die einer Nachricht zugeordnete Speicher Ressource frei.                                                                                                |
| [**Wsgetcustomheader**](/windows/desktop/api/WebServices/nf-webservices-wsgetcustomheader)                       | Sucht den von der Anwendung definierten Header der Nachricht und deserialisiert ihn.                                                                               |
| [**Wsgederader**](/windows/desktop/api/WebServices/nf-webservices-wsgetheader)                                   | Sucht einen bestimmten Standard Header in der Nachricht und deserialisiert ihn.                                                                                 |
| [**Wsgetheiaderattribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetheaderattributes)               | Füllt einen ULONG-Parameter mit den [**WS- \_ Header \_ Attributen**](/windows/win32/api/webservices/ne-webservices-ws_xml_text_type) aus dem Header Element auf, auf dem der Reader positioniert ist. |
| [**Wsgetmessageproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty)                 | Ruft eine angegebene Nachrichten Objekt Eigenschaft ab.                                                                                                         |
| [**Wsinitializemess**](/windows/desktop/api/WebServices/nf-webservices-wsinitializemessage)                   | Initialisiert die Header für die Nachricht zur Vorbereitung der Verarbeitung.                                                                                 |
| [**Wsmarkheaderasverstanden**](/windows/desktop/api/WebServices/nf-webservices-wsmarkheaderasunderstood)         | Markiert einen Header so, wie er von der Anwendung verstanden wird.                                                                                                       |
| [**Wsread Body**](/windows/desktop/api/WebServices/nf-webservices-wsreadbody)                                     | Deserialisiert einen Wert aus dem XML-Reader der Nachricht.                                                                                               |
| [**Wsumenvelopeend**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopeend)                       | Liest die schließenden Elemente einer Nachricht.                                                                                                               |
| [**Wsumenvelopestart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)                   | Liest die Header der Nachricht und bereitet das Lesen der Textelemente vor.                                                                               |
| [**Wsremovecustomheader**](/windows/desktop/api/WebServices/nf-webservices-wsremovecustomheader)                 | Entfernt einen benutzerdefinierten Header aus der Nachricht.                                                                                                              |
| [**Wsremoveheader**](/windows/desktop/api/WebServices/nf-webservices-wsremoveheader)                             | Entfernt das standardmäßige [**WS- \_ Header- \_ Typobjekt**](/windows/desktop/api/WebServices/ne-webservices-ws_header_type) aus einer Nachricht.                                                                 |
| [**Wsresetmessage**](/windows/desktop/api/WebServices/nf-webservices-wsresetmessage)                             | Legt den Nachrichten Zustand auf den **WS- \_ Nachrichten \_ Zustand " \_ empty**" zurück.                                                                                          |
| [**Wssetheiader**](/windows/desktop/api/WebServices/nf-webservices-wssetheader)                                   | Fügt den angegebenen Standard Header in der Nachricht hinzu oder ersetzt diesen.                                                                                         |
| [**Wsschreitebody**](/windows/desktop/api/WebServices/nf-webservices-wswritebody)                                   | Schreibt einen Wert in den Text einer Nachricht.                                                                                                               |
| [**Wsschreiteenvelopeend**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopeend)                     | Schreibt die schließenden Elemente einer Meldung.                                                                                                              |
| [**Wsschreiteenvelopestart**](/windows/desktop/api/WebServices/nf-webservices-wswriteenvelopestart)                 | Schreibt den Anfang der Nachricht einschließlich des aktuellen Satzes von Headern der Nachricht und bereitet das Schreiben der Textelemente vor.                           |



 



| Handle                        | BESCHREIBUNG                                         |
|-------------------------------|-----------------------------------------------------|
| [WS- \_ Nachricht](ws-message.md) | Der nicht transparente Typ, der zum referenzieren eines Nachrichten Objekts verwendet wird. |



 



| Struktur                                                | BESCHREIBUNG                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**WS- \_ Fehler**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)                            | Ein Fehlerwert, der in den Text einer Nachricht übertragen wird, der einen Verarbeitungsfehler angibt. |
| [**WS- \_ Fehler \_ Code**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)                 | Stellt einen Fehlercode dar.                                                             |
| [**WS- \_ Fehler \_ Ursache**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)             | Enthält eine Erläuterung des Fehlers.                                                |
| [**WS- \_ Nachrichten \_ Eigenschaften**](/windows/desktop/api/WebServices/ns-webservices-ws_message_properties) | Gibt einen Satz von [**WS- \_ Nachrichten \_ Eigenschafts**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property) Strukturen an.  |
| [**WS- \_ Nachrichten \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_message_property)     | Gibt eine Nachrichten spezifische Einstellung an.                                                |



 

 

 




