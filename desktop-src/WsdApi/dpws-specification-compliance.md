---
description: In diesem Thema wird beschrieben, wie WSDAPI die Wahlfunktion in der DPWS-Spezifikation (Devices Profile for Web Services) implementiert. Außerdem wird beschrieben, welche DPWS-Funktionalität in der WSDAPI-Implementierung ausgelassen wurde.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: DPWS-Spezifikationskonformität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59ba29e8e36fd5030732c0b61a2dfd164d9c887bdd9881a775c8b1ce6ec353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130826"
---
# <a name="dpws-specification-compliance"></a>DPWS-Spezifikationskonformität

In diesem Thema wird beschrieben, wie WSDAPI die Wahlfunktion in der DPWS-Spezifikation [(Devices Profile for Web Services)](https://specs.xmlsoap.org/ws/2006/02/devprof/) implementiert. Außerdem wird beschrieben, welche DPWS-Funktionalität in der WSDAPI-Implementierung ausgelassen wurde.

Die DPWS-Spezifikation bietet eine konsistente Möglichkeit, Nachrichten mit Geräten zu senden. Darüber hinaus werden spezifische Einschränkungen und Empfehlungen zur Vereinfachung der Unterstützung von Webdiensten auf eingebetteter Hardware hinzufügt.

Die DPWS-Spezifikation beschreibt die Wahlfunktion unter Verwendung der Begriffe MAY oder SHOULD in einer bestimmten Implementierungsempfehlung oder -einschränkung. Ausgelassene Funktionen können funktionen sein, die in der DPWS-Spezifikation, die nicht von WSDAPI implementiert wurde, als ERFORDERLICH beschrieben werden, oder es kann sich um Funktionen, die WSDAPI in einer anderen Methode implementiert hat, die in der DPWS-Spezifikation angegeben ist.

Dieses Thema folgt dem Layout des DPWS-Abschnitts. In jedem Abschnitt wird beschrieben, wie bestimmte Einschränkungen, Anforderungen und wahlfähige Funktionen von der WSDAPI-Implementierung behandelt werden. Dieses Thema wird am besten zusammen mit der DPWS-Spezifikation gelesen.

## <a name="dpws-30-messaging"></a>DPWS 3.0-Messaging

### <a name="dpws-31-uri-formats"></a>DPWS 3.1-URI-Formate

Einschränkungen R0025 und R0027 schränken URIs auf MAX \_ URI \_ SIZE-Oktette ein. WSDAPI erzwingt beide Einschränkungen wie angegeben.

### <a name="dpws-32-udp-messaging"></a>DPWS 3.2 UDP-Messaging

Die Empfehlung R0029 schlägt vor, dass UDP-Pakete, die größer als die maximale Übertragungseinheit (MTU) für UDP sind, nicht gesendet werden sollen. WSDAPI implementiert diese Empfehlung nicht und ermöglicht Implementierungen das Senden und Empfangen von Ermittlungsmeldungen, die größer als die MTU sind.

### <a name="dpws-33-http-messaging"></a>DPWS 3.3 HTTP messaging (DPWS 3.3-HTTP-Messaging)

R0001 erfordert, dass Dienste die blockierte Übertragung unterstützen. WSDAPI akzeptiert blockierte Daten in Anforderungsnachrichten und sendet blockierte Daten in Anforderungsnachrichten.

R0012 und R0013 beschreiben erforderliche Teile der SOAP-HTTP-Bindung. Für R0012 implementiert WSDAPI die SOAP-HTTP-Bindung, beginnt jedoch erst mit dem Lesen der HTTP-Antwort, wenn WSDAPI das Senden der HTTP-Anforderung abgeschlossen hat. WSDAPI implementiert das erforderliche Nachrichtenaustauschmuster in R0013, implementiert den optionalen antwortenden SOAP-Knoten in R0014 und implementiert nicht das optionale Webmethodesfeature in R0015. WSDAPI unterstützt auch die Anforderungen in R0030 und R0017.

### <a name="dpws-34-soap-envelope"></a>DPWS 3.4 SOAP-Umschlag

WSDAPI unterstützt R0034 und erzwingt standardmäßig R0003 und R0026. Genauer gesagt: Wenn WSDAPI in Übereinstimmung mit R0003 und R0026 einen SOAP-Umschlag empfängt, der größer als MAX ENVELOPE SIZE über HTTP ist, wird er abgelehnt und die Verbindung \_ \_ geschlossen.

### <a name="dpws-35-ws-addressing"></a>DPWS 3.5 WS-Addressing

R0004 spiegelt die empfohlene Verwendung der Geräte-API in WSDAPI wider und wird von der Client-API in WSDAPI unterstützt. Da dies eine Empfehlung ist, ermöglicht WSDAPI Clients und Geräten die Verwendung anderer URIs als URIs für ihre Geräteendpunkte, um maximale `urn:uuid` Kompatibilität sicherzustellen. Da die Geräte-API in WSDAPI den Zustand zwischen Initialisierungen nicht beibehält, liegt es an Anwendungsentwicklern, die die Geräte-API in WSDAPI verwenden, sicherzustellen, dass R0005 und R0006 ordnungsgemäß unterstützt werden. Die Client-API in WSDAPI geht davon aus, dass Geräteidentitäten eindeutig und persistent sind, und die Funktionalität, die auf der Client-API in WSDAPI (z. B. PnP-X) aufbaut, erfordert dies, um das Gerät bei Geräteneustarts ordnungsgemäß zu erkennen.

R0007 empfiehlt die Verwendung von Verweiseigenschaften in Endpunktverweisen. WSDAPI erkennt und akzeptiert weiterhin Endpunkte mit Verweiseigenschaften, und Entwickler können sie verwenden, aber standardmäßig füllt WSDAPI sie nicht in von ihr erstellten Endpunkten auf. Ähnlich wird bei R0042 beim Erstellen von Dienstendpunkten von WSDAPI eine HTTP- oder HTTPS-Transportadresse verwendet. Geräte müssen jedoch keine HTTP- oder HTTPS-Transportadressen in ihren Dienstendpunkten verwenden. Das Verhalten des Clients beim Versuch, mit einem Dienst zu kommunizieren, der http oder HTTPS nicht verwendet, ist nicht definiert.

Bei Fehlern schränkt R0031 den Antwortendpunkt ein und beschreibt den zu sendenden Fehler, wenn der Fehler nicht anonym ist. WSDAPI erzwingt, dass der Antwortendpunkt beim Senden von Nachrichten den richtigen Wert verwendet. Wenn WSDAPI eine Anforderungsnachricht mit dem falschen Antwortendpunkt empfängt, wird ein Fehler angezeigt. R0041 bietet Implementierungen die Möglichkeit, einen Fehler zu verdringen, wenn der Antwortendpunkt ungültig ist. Anstatt den Fehler zu verdringen, sendet WSDAPI den Fehler zurück im Anforderungskanal, der an den anonymen Endpunkt adressiert ist, als "bestmöglichen Aufwand" für die Kommunikation mit dem Client.

Schließlich gibt es zwei Einschränkungen für SOAP-Header, R0019 und R0040, die beide WSDAPI erfüllen und für empfangene Nachrichten erzwingen.

### <a name="dpws-36-attachments"></a>DPWS 3.6-Anlagen

WSDAPI unterstützt Anlagen und entspricht R0022. WSDAPI entspricht auch R0037. Beim Senden von Anlagen wird die Inhaltsübertragungscodierung von WSDAPI für alle MIME-Teile immer auf "binär" festgelegt. WSDAPI erzwingt jedoch nicht R0036. Das Verhalten von WSDAPI beim Empfang eines MIME-Teils mit einer Inhaltsübertragungscodierung, die nicht auf "binary" festgelegt ist, ist nicht definiert.

DPWS definiert auch KLAUSELN für die MIME-Teilebestellung. Für R0038 erzwingt WSDAPI die Reihenfolge der Teile und lehnt eine MIME-Nachricht ab, wenn der SOAP-Umschlag nicht der erste MIME-Teil ist. Für R0039 sendet WSDAPI immer den SOAP-Umschlag als ersten MIME-Teil.

## <a name="dpws-40-discovery"></a>DPWS 4.0-Ermittlung

R1013 und R1001 unterscheiden die Geräteermittlung und die Dienstermittlung. WSDAPI entspricht R1013. Die Hostingimplementierung entspricht R1001, WSDAPI erzwingt diese Empfehlung jedoch nicht auf dem Client.

DPWS bietet auch Anleitungen zu Typen und Bereichsabgleichsregeln. WSDAPI unterstützt alle in der [WS-Ermittlung](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) definierten Bereichsabgleichsregeln mit Ausnahme von LDAP. WSDAPI bietet auch ein erweiterbares Modell zum Definieren benutzerdefinierter Bereichsabgleichsregeln und damit zur Einhaltung von R1019. Die Hosting-API stellt auch immer den Typ in der Ermittlung pro R1020 bereit, aber die Client-API erfordert nicht, `wsdp:Device` dass er vorhanden ist. Für andere anwendungen, die auf WSDAPI aufgebaut sind, z. B. PnP-X, ist es schwierig, dass der Typ `wsdp:Device` bei der Ermittlung vorhanden ist.

Zur Vereinfachung der Ermittlung und Bindung unterstützt WSDAPI R1009 und R1016. Pro R1018 ignoriert WSDAPI Multicast-UDP, das nicht an die anonyme Adresse gesendet wird. R1015, R1021 und R1022 definieren eine HTTP-Bindung für die Testnachricht, die WSDAPI wie beschrieben unterstützt.

## <a name="dpws-50-description"></a>DPWS 5.0 Description

WSDAPI erzwingt R2044 auf dem Client. Auf der Hostingseite stellt WSDAPI immer nur das -Element `wsx:Metadata` im SOAP-Umschlagkörper zur Verfügung. R2045 ermöglicht Geräten die Unterstützung einer Teilmenge der [WS-Transfer-Funktionalität.](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) Die Hosting-API generiert immer den `wsa:ActionNotSupported` Fehler.

### <a name="dpws-51-characteristics"></a>DPWS 5.1-Merkmale

DPWS beschreibt grundlegende Merkmale für das Gerät. Zusätzlich zu den in diesem Thema beschriebenen Einschränkungen werden Längenlimits für bestimmte Zeichenfolgen und URIs definiert. WSDAPI erzwingt die Längengrenzwerte in diesem DPWS-Abschnitt 5.1, entweder vor dem Senden der Nachricht oder nach der Analyse ihres Inhalts.

DPWS beschreibt auch die erforderlichen Metadatenabschnitte und das Durchfahren der Metadatenversion. Die Clientimplementierung erzwingt das Vorhandensein von ThisModel- und ThisDevice-Metadaten. Die Hostingimplementierung verwaltet auch ordnungsgemäß die Metadatenversion und stellt immer diese Abschnitte bereit, die R2038, R2012, R2001, R2039, R2014 und R2002 erfüllen.

### <a name="dpws-52-hosting"></a>DPWS 5.2-Hosting

In diesem Abschnitt wird die Hierarchie von Diensten und Beziehungsmetadaten beschrieben. WSDAPI erzwingt weder auf client- noch geräteseitiger Seite die Eindeutigkeit der ServiceId, wie in diesem Abschnitt beschrieben.

WSDAPI hält R2040 ein, und die Hostingimplementierung kann eine Metadatenantwort ohne Beziehungsabschnitt senden, wenn keine gehosteten Dienste enthalten sind. Die Clientimplementierung akzeptiert die Metadatenantwort ordnungsgemäß.

R2029 ermöglicht mehrere Beziehungsabschnitte in einer Metadatenantwort, die WSDAPI ordnungsgemäß akzeptiert. R2030 und R2042 beschreiben die Verwaltung der Metadatenversion, die in der Hosting-API ordnungsgemäß implementiert ist.

### <a name="dpws-53-wsdl"></a>DPWS 5.3 WSDL

Wenn ein Dienst Web Services Description Language (WSDL) daten, können Clientimplementierungen die Dienstdefinition erhalten und den Dienst direkt bearbeiten. Dies wird von spät gebundenen Clients verwendet. Die WSDAPI-Clientimplementierung akzeptiert die von einem Dienst bereitgestellte WSDL, aber der Client überprüft sie nicht, und der Client stellt kein spät gebundenes Programmiermodell zur Verfügung. Die Hostingimplementierung kann verwendet werden, um WSDL zur Verfügung zu stellen, aber der Host ist dazu nicht erforderlich, da die Metadaten auf Dienstebene nicht vom Host selbst verwaltet werden.

### <a name="dpws-54-ws-policy"></a>DPWS 5.4 WS-Policy

DPWS beschreibt Richtlinien-Assertionen, die für Geräte verwendet werden sollen. Da WSDAPI WSDL nicht zur Verfügung stellt und nicht interpretiert, kann die in WSDL-Daten eingebettete Richtlinie nicht erkannt und erzwungen werden.

## <a name="dpws-60-eventing"></a>DPWS 6.0-Ereignis

### <a name="dpws-61-subscription"></a>DPWS 6.1-Abonnement

DPWS erfordert Unterstützung für die Pushbereitstellung. WSDAPI implementiert die Pushbereitstellung auf Dienstseite und ist daher mit R3009 und R3010 konform und akzeptiert nur den Pushbereitstellungsmodus auf clientseitiger Seite. R3017 und R3018 erfordern bestimmte Fehler vom Dienst, wenn er die Adressen oder `NotifyTo` nicht `EndTo` erkennt. WSDAPI überprüft diese Adressen nicht im Voraus und generiert diese Fehler nicht. Die Clientimplementierung erkennt diese Fehler jedoch ordnungsgemäß. Entsprechend ist R3019 optional, und WSDAPI implementiert diese Empfehlung nicht, aber die Clientimplementierung erkennt die Nachricht ordnungsgemäß und benachrichtigt die Anwendung über einen `SubscriptionEnd` Übermittlungsfehler.

### <a name="dpws-611-filtering"></a>DPWS 6.1.1-Filterung

WSDAPI entspricht R3008 und implementiert den `Action` Filter. In Übereinstimmung mit R3011 und R3012 generiert WSDAPI die Fehler in den angegebenen Bedingungen nicht. WSDAPI implementiert auch den fehler beschriebenen R3020, wenn die Aktionen, nach denen gefiltert werden soll, nicht erkannt werden.

### <a name="dpws-62-subscription-duration-and-renewal"></a>DPWS 6.2 Abonnementdauer und -verlängerung

WSDAPI entspricht R3005, R3006 und R3016. WSDAPI verwendet immer , akzeptiert jedoch, falls angegeben, und gibt daher den optionalen Fehler `xs:duration` `xs:dateTime` in R3013 nicht aus. WSDAPI unterstützt `GetStatus` und gibt den Fehler nicht pro `wsa:ActionNotSupported` R3015 aus. WSDAPI akzeptiert den `wsa:ActionNotSupported` Fehler, wenn ein Dienst damit auf `GetStatus` eine Anforderung antwortet.

## <a name="dpws-70-security"></a>DPWS 7.0-Sicherheit

DPWS beschreibt ein empfohlenes Sicherheitsmodell für Geräte. WSDAPI implementiert diese Empfehlungen nicht wie beschrieben und erzwingt die Einschränkungen in diesem Abschnitt nicht wie beschrieben.

## <a name="dpws-appendix-i"></a>DPWS Anhang I

DPWS passt globale Konstanten von anderen Spezifikationen an Geräte an. WSDAPI verwendet die Konstanten aus diesem Abschnitt und überschreibt die Standardkonst constants in der [WS-Discovery-Implementierung](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) mit diesen Konstanten. Anwendungen, die WSDAPI für WS-Discovery, werden an die in DPWS definierten Konstanten gebunden, nicht an die konstanten, die in [WS-Discovery definiert sind.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

 

 



