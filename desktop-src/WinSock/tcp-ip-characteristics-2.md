---
description: TCP/IP verfügt über Eigenschaften, mit denen das Protokoll gemäß den Anforderungen der standardisierten Implementierung funktionieren kann.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: TCP/IP-Merkmale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865960"
---
# <a name="tcpip-characteristics"></a>TCP/IP-Merkmale

TCP/IP verfügt über Eigenschaften, mit denen das Protokoll gemäß den Anforderungen der standardisierten Implementierung funktionieren kann. Diese Merkmale können mit Entwicklungsoptionen kombiniert werden, die zu einer schlechten Leistung führen. Welche Auswirkung diese TCP/IP-Merkmale auf eine Anwendung haben, hängt davon ab, ob die Anwendung transaktional oder Streaming ist.

Transaktionale Anwendungen sind von dem Aufwand betroffen, der zum Einrichten und Beenden der Verbindung erforderlich ist. Wenn z. b. eine Verbindung in einem Ethernet-Netzwerk hergestellt wird, müssen jeweils drei Pakete mit ungefähr 60 Byte gesendet werden, und für den Austausch ist ungefähr eine RTT erforderlich. Wenn eine Verbindung beendet wird, werden vier Pakete ausgetauscht. Dies gilt für jede Verbindung. eine Anwendung, die Verbindungen öffnet und schließt, verursacht häufig den Aufwand für jedes Vorkommen.

Ein anderer Aspekt von TCP/IP ist ein *langsamer Start*, der immer dann stattfindet, wenn eine Verbindung hergestellt wird. Der langsame Start ist ein künstlicher Grenzwert für die Anzahl der Daten Segmente, die gesendet werden können, bevor die Bestätigung dieser Segmente empfangen wird. Der langsame Start ist so konzipiert, dass die Überlastung des Netzwerks eingeschränkt wird. Wenn eine Verbindung über Ethernet hergestellt wird, kann unabhängig von der Fenstergröße des Empfängers eine Übertragung von 4 KB bis zu 3-4 RTT dauern, da langsam begonnen wird.

Eine TCP/IP-Optimierung, die als Nagle-Algorithmus bezeichnet wird, kann auch die Datenübertragungsgeschwindigkeit bei einer Verbindung einschränken. Der Nagle-Algorithmus ist so konzipiert, dass der Protokoll Mehraufwand für Anwendungen reduziert wird, die kleine Datenmengen senden, wie z. b. Telnet, die jeweils jeweils ein einzelnes Zeichen senden. Anstatt direkt ein Paket mit vielen Header-und kleinen Daten zu senden, wartet der Stapel auf weitere Daten von der Anwendung oder einer Bestätigung, bevor der Vorgang fortgesetzt wird.

Verzögerte Bestätigungen, die häufig als *verzögerte* Bestätigung bezeichnet werden, werden auch in TCP/IP integriert, um eine effizientere piggyunterstützung von Bestätigungen zu ermöglichen, wenn Rückgabe Daten von der empfangenden Anwendung empfangen werden. Wenn diese Daten nicht in Kürze vorhanden sind und die Sendeseite auf eine Bestätigung wartet, können Verzögerungen von ungefähr 200 Millisekunden pro Sendevorgang auftreten.

Wenn eine TCP-Verbindung geschlossen wird, werden Verbindungs Ressourcen an dem Knoten, der die Schließung initiiert hat, in einen Wartezustand versetzt, der als Zeit Wartezeit bezeichnet wird, um Schutz vor Daten Beschädigungen zu erhalten, wenn doppelte Pakete im Netzwerk gelinger werden. Dadurch wird sichergestellt, dass beide Enden mit der Verbindung abgeschlossen sind. Dies kann zu einem Mangel an Ressourcen, die pro Verbindung erforderlich sind, führen, z. b. RAM und Ports, wenn Anwendungen häufig Verbindungen öffnen und schließen.

Neben der Auswirkung von verzögertem ACK und anderen Überlastungs Vermeidungs Schemas können Streaminganwendungen auch durch eine zu geringe standardmäßige Empfangs Fenstergröße auf dem empfangenden Ende beeinträchtigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsverhalten](application-behavior-2.md)
</dt> <dt>

[Hochleistungsfähige Windows Sockets-Anwendungen](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Nagle-Algorithmus](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



