---
description: In diesem Thema wird beschrieben, wie WSDAPI die wählbaren Funktionen in der Spezifikation Geräte Profil für Webdienste (DPWS) implementiert. Außerdem wird beschrieben, welche DPWS-Funktionalität in der WSDAPI-Implementierung ausgelassen wurde.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: Konformität der DPWS-Spezifikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed26e57a0f7a94069e802f96f346a3a5eca67b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349913"
---
# <a name="dpws-specification-compliance"></a>Konformität der DPWS-Spezifikation

In diesem Thema wird beschrieben, wie WSDAPI die wählbaren Funktionen in der Spezifikation [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) implementiert. Außerdem wird beschrieben, welche DPWS-Funktionalität in der WSDAPI-Implementierung ausgelassen wurde.

Die DPWS-Spezifikation bietet eine konsistente Möglichkeit zur Meldung mit Geräten. Außerdem werden bestimmte Einschränkungen und Empfehlungen hinzugefügt, die den Prozess der Unterstützung von Webdiensten auf eingebetteter Hardware vereinfachen.

Die DPWS-Spezifikation beschreibt die wählbaren Funktionen mithilfe der Bedingungen, die in einer bestimmten Implementierungs Empfehlung oder-Einschränkung auftreten können. Die ausgelassene Funktionalität kann eine Funktionalität sein, die in der von WSDAPI nicht implementierten DPWS-Spezifikation erforderlich ist, oder es kann sich um Funktionen handeln, die von WSDAPI in der in der DPWS-Spezifikation angegebenen Methode implementiert wurden.

Dieses Thema folgt dem Layout des DPWS-Abschnitts nach Abschnitt. In jedem Abschnitt wird beschrieben, wie bestimmte Einschränkungen, Anforderungen und wählende Funktionen von der WSDAPI-Implementierung behandelt werden. Dieses Thema ist am besten in Zusammenhang mit der DPWS-Spezifikation zu lesen.

## <a name="dpws-30-messaging"></a>DPWS 3,0-Messaging

### <a name="dpws-31-uri-formats"></a>DPWS 3,1-URI-Formate

Einschränkungen R0025 und R0027 schränken URIs auf \_ Oktette der maximalen URI- \_ Größe ein. WSDAPI erzwingt beide Einschränkungen wie angegeben.

### <a name="dpws-32-udp-messaging"></a>DPWS 3,2 UDP-Messaging

Empfehlung R0029 schlägt vor, dass UDP-Pakete, die größer als die maximale Übertragungseinheit (MTU) für UDP sind, nicht gesendet werden sollen. WSDAPI implementiert diese Empfehlung nicht und ermöglicht Implementierungen das Senden und empfangen von Discovery-Nachrichten, die größer als die MTU sind.

### <a name="dpws-33-http-messaging"></a>DPWS 3,3 http-Messaging

R0001 erfordert, dass Dienste eine segmentierte Übertragung unterstützen. WSDAPI nimmt in Anforderungs Nachrichten segmentierte Daten an und sendet in Anforderungs Nachrichten segmentierte Daten.

R0012 und R0013 beschreiben erforderliche Teile der SOAP-HTTP-Bindung. Für R0012 implementiert WSDAPI die SOAP-HTTP-Bindung, beginnt jedoch erst mit dem Lesen der HTTP-Antwort, wenn der WSDAPI das Senden der HTTP-Anforderung abgeschlossen hat. WSDAPI implementiert das erforderliche Nachrichtenaustausch Muster in R0013, implementiert den optionalen antwortenden SOAP-Knoten in R0014 und implementiert nicht die optionale Webmethoden Funktion in R0015. WSDAPI unterstützt auch die Anforderungen in R0030 und R0017.

### <a name="dpws-34-soap-envelope"></a>DPWS 3,4-SOAP-Umschlag

WSDAPI unterstützt R0034 und erzwingt standardmäßig R0003 und R0026. Genauer gesagt wird in Übereinstimmung mit R0003 und R0026, wenn WSDAPI einen SOAP-Umschlag erhält, der größer ist als die maximale \_ Umschlag \_ Größe über HTTP, abgelehnt, und die Verbindung wird geschlossen.

### <a name="dpws-35-ws-addressing"></a>DPWS 3,5-WS-Addressing

R0004 spiegelt die empfohlene Verwendung der Geräte-API in WSDAPI wider und wird von der Client-API in WSDAPI unterstützt. Da es sich hierbei um eine Empfehlung handelt, gestattet WSDAPI, dass Clients und Geräte andere URIs als `urn:uuid` URIs für Ihre Geräte Endpunkte verwenden, um maximale Kompatibilität zu gewährleisten. Da die Geräte-API in WSDAPI den Zustand zwischen den Initialisierungen nicht beibehält, liegt es an Anwendungsentwicklern, die die Geräte-API in WSDAPI verwenden, um sicherzustellen, dass R0005 und R0006 ordnungsgemäß unterstützt werden. Die Client-API in WSDAPI geht davon aus, dass die Geräte Identitäten eindeutig und persistent sind, und die Funktionalität, die auf der Client-API in WSDAPI (z. b. PnP-X) aufbaut, erfordert dies, damit das Gerät über Geräte Neustarts hinweg richtig erkannt wird.

R0007 empfiehlt die Verwendung von Verweis Eigenschaften in Endpunkt verweisen. WSDAPI erkennt und akzeptiert weiterhin Endpunkte mit Verweis Eigenschaften, und Entwickler können diese verwenden, aber standardmäßig füllt WSDAPI Sie nicht in Endpunkten, die Sie erstellt. Analog dazu wird bei R0042 bei der Erstellung von Dienst Endpunkten durch WSDAPI eine HTTP-oder HTTPS-Transport Adresse verwendet, aber es ist nicht erforderlich, dass Geräte http-oder HTTPS-Transport Adressen in ihren Dienst Endpunkten verwenden. Das Verhalten des Clients, wenn versucht wird, mit einem Dienst zu kommunizieren, der nicht http oder HTTPS verwendet, ist nicht definiert.

Bei Fehlern schränkt R0031 den Antwort Endpunkt ein und beschreibt den Fehler, der gesendet werden soll, wenn der Fehler nicht anonym ist. WSDAPI zwingt den Antwort Endpunkt, beim Senden von Nachrichten den korrekten Wert zu verwenden, und führt zu einem Fehler, wenn WSDAPI eine Anforderungs Nachricht mit dem falschen Antwort Endpunkt empfängt. R0041 gibt Implementierungen die Option zum Löschen eines Fehlers, wenn der Antwort Endpunkt ungültig ist. Anstatt den Fehler zu verwerfen, sendet WSDAPI den Fehler an den Anforderungs Kanal zurück, der an den anonymen Endpunkt adressiert ist, um mit dem Client zu kommunizieren.

Und schließlich gibt es zwei Einschränkungen für SOAP-Header R0019 und R0040, die beide von WSDAPI für empfangene Nachrichten einhalten und erzwingen.

### <a name="dpws-36-attachments"></a>DPWS 3,6-Anlagen

WSDAPI unterstützt Anlagen und entspricht R0022. WSDAPI entspricht außerdem R0037. Beim Senden von Anlagen legt WSDAPI die Codierung der Inhalts Übertragung immer auf "Binary" für alle MIME-Teile fest. Allerdings erzwingt WSDAPI R0036 nicht. Das Verhalten von WSDAPI beim Empfangen eines MIME-Teils, bei dem eine Content Transfer Encoding nicht auf "Binary" festgelegt ist, ist nicht definiert.

DPWS definiert auch MIME-Part-Reihenfolge Klauseln. Für R0038 erzwingt WSDAPI die Reihenfolge der Teile und lehnt eine MIME-Nachricht ab, wenn der SOAP-Umschlag nicht der erste MIME-Teil ist. Für R0039 sendet WSDAPI den SOAP-Umschlag immer als ersten MIME-Teil.

## <a name="dpws-40-discovery"></a>DPWS 4,0-Ermittlung

R1013 und R1001 unterscheiden Geräte Ermittlung und Dienst Ermittlung. WSDAPI entspricht R1013. Die hostingimplementierung entspricht R1001, aber WSDAPI erzwingt diese Empfehlung nicht auf dem Client.

DPWS bietet auch Anleitungen für Typen und Bereichs Übereinstimmungs Regeln. WSDAPI unterstützt alle in [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) mit Ausnahme von LDAP definierten Regeln für den Bereichs Abgleich. WSDAPI bietet auch ein erweiterbares Modell zum Definieren von benutzerdefinierten Regeln zum Abgleich von Bereichen und entspricht somit R1019. Die Hosting-API liefert auch immer den `wsdp:Device` Typ in der Ermittlung pro R1020, aber die Client-API erfordert nicht, dass Sie vorhanden ist. Andere Anwendungen, die auf WSDAPI basieren, wie z. b. PnP-X, haben eine feste Anforderung, dass der `wsdp:Device` Typ in der Ermittlung vorhanden sein muss.

Um die Ermittlung und Bindung zu vereinfachen, unterstützt WSDAPI R1009 und R1016. Per R1018 ignoriert WSDAPI Multicast-UDP, die nicht an die anonyme Adresse gesendet werden. R1015, R1021 und R1022 definieren eine HTTP-Bindung für die Testnachricht, die von WSDAPI wie beschrieben unterstützt wird.

## <a name="dpws-50-description"></a>DPWS 5,0-Beschreibung

WSDAPI erzwingt R2044 auf dem Client. Auf der Hostingseite stellt WSDAPI das Element immer nur `wsx:Metadata` im SOAP-Umschlagtext bereit. R2045 ermöglicht es Geräten, eine Teilmenge der [WS-Transfer-](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) Funktionalität zu unterstützen. Die Hosting-API generiert immer den `wsa:ActionNotSupported` Fehler.

### <a name="dpws-51-characteristics"></a>DPWS 5,1-Merkmale

DPWS beschreibt grundlegende Merkmale für das Gerät. Zusätzlich zu den in diesem Thema beschriebenen Einschränkungen werden Längen Limits für bestimmte Zeichen folgen und URIs definiert. WSDAPI erzwingt die Längen Limits in diesem DPWS-Abschnitt 5,1, entweder vor dem Senden der Nachricht oder nach der Inhalts Verarbeitung.

DPWS beschreibt außerdem die erforderlichen Metadatenabschnitte und den Vorgang zum Durchlaufen der Metadatenversion. Die Client Implementierung erzwingt das vorhanden sein der Metadaten thismodel und thisdevice. Die hostingimplementierung verwaltet auch die Metadatenversion ordnungsgemäß und stellt immer diese Abschnitte bereit, die R2038, R2012, R2001, R2039, R2014 und R2002 einhalten.

### <a name="dpws-52-hosting"></a>DPWS 5,2-Hosting

In diesem Abschnitt wird die Hierarchie der Dienste und Beziehungs Metadaten beschrieben. WSDAPI erzwingt nicht die Eindeutigkeit der serviceid, wie in diesem Abschnitt auf der Client-oder der Geräteseite beschrieben.

WSDAPI entspricht R2040, und es ist möglich, dass die Hosting-Implementierung eine metadatenantwort ohne einen Beziehungs Abschnitt sendet, wenn keine gehosteten Dienste vorhanden sind. Die Client Implementierung akzeptiert die metadatenantwort ordnungsgemäß.

R2029 ermöglicht mehrere Beziehungs Abschnitte in einer metadatenantwort, die von WSDAPI ordnungsgemäß akzeptiert werden. R2030 und R2042 beschreiben die Verwaltung der Metadatenversion, die in der Hosting-API ordnungsgemäß implementiert ist.

### <a name="dpws-53-wsdl"></a>DPWS 5,3 WSDL

Wenn ein Dienst Web Services Description Language-Daten (WSDL) bereitstellt, können Client Implementierungen die Dienst Definition erhalten und den Dienst dynamisch bearbeiten. Diese wird von spät gebundenen Clients verwendet. Die WSDAPI-Client Implementierung akzeptiert WSDL, das von einem Dienst bereitgestellt wird, der Client überprüft Sie jedoch nicht, und der Client stellt kein spät gebundenes Programmiermodell bereit. Die Hosting-Implementierung kann verwendet werden, um WSDL bereitzustellen, aber der Host ist nicht erforderlich, da die Service Level-Metadaten nicht vom Host selbst verwaltet werden.

### <a name="dpws-54-ws-policy"></a>DPWS 5,4-WS-Policy

DPWS beschreibt Richtlinien Assertionen, die für Geräte verwendet werden sollen. Da WSDAPI WSDL nicht bereitstellt und nicht interpretiert, kann es keine Richtlinie erkennen und erzwingen, die in WSDL-Daten eingebettet ist.

## <a name="dpws-60-eventing"></a>DPWS 6,0 Eventing

### <a name="dpws-61-subscription"></a>DPWS 6,1-Abonnement

DPWS erfordert Unterstützung für die pushübermittlung. WSDAPI implementiert die pushübermittlung auf der Dienst Seite und entspricht somit R3009 und R3010 und akzeptiert nur den pushübermittlungs Modus auf der Clientseite. R3017 und R3018 erfordern bestimmte Fehler vom Dienst, wenn die Adressen oder nicht erkannt `NotifyTo` werden `EndTo` . WSDAPI überprüft diese Adressen nicht vorab und generiert diese Fehler nicht. Die Client Implementierung erkennt diese Fehler jedoch ordnungsgemäß. Ebenso ist R3019 optional, und WSDAPI implementiert diese Empfehlung nicht, aber die Client Implementierung erkennt die Nachricht ordnungsgemäß `SubscriptionEnd` und benachrichtigt die Anwendung über einen Übermittlungs Fehler.

### <a name="dpws-611-filtering"></a>DPWS 6.1.1 Filtern

WSDAPI entspricht R3008 und implementiert den `Action` Filter. In Übereinstimmung mit R3011 und R3012 generiert WSDAPI die Fehler nicht in den angegebenen Bedingungen. WSDAPI implementiert auch den beschriebenen Fehler R3020, wenn er nicht erkennt, welche Aktionen er filtern soll.

### <a name="dpws-62-subscription-duration-and-renewal"></a>Dauer und Erneuerung des DPWS 6,2-Abonnements

WSDAPI entspricht R3005, R3006 und R3016. Der WSDAPI verwendet immer `xs:duration` `xs:dateTime` , wenn er bereitgestellt wird, und führt daher nicht den optionalen Fehler in R3013 aus. WSDAPI unterstützt `GetStatus` und führt den `wsa:ActionNotSupported` Fehler nicht pro R3015 aus. WSDAPI akzeptiert den `wsa:ActionNotSupported` Fehler, wenn ein Dienst auf eine `GetStatus` Anforderung antwortet.

## <a name="dpws-70-security"></a>DPWS 7,0-Sicherheit

In DPWS wird ein empfohlenes Sicherheitsmodell für Geräte beschrieben. WSDAPI implementiert diese Empfehlungen nicht wie beschrieben und erzwingt die Einschränkungen in diesem Abschnitt nicht wie beschrieben.

## <a name="dpws-appendix-i"></a>DPWS-Anhang I

DPWS Amend globale Konstanten von anderen Spezifikationen an Geräte. WSDAPI verwendet die Konstanten aus diesem Abschnitt und überschreibt die Standard Konstanten in der [WS-Discovery-](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) Implementierung mit diesen Konstanten. Anwendungen, die WSDAPI für WS-Discovery verwenden, werden an die in DPWS definierten Konstanten gebunden, nicht an die in [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)definierten Konstanten.

 

 



