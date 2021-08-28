---
description: TCP/IP verfügt über Merkmale, die es dem Protokoll ermöglichen, wie es die standardisierten Implementierungsanforderungen vorschreiben.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: TCP/IP-Merkmale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f720dac1157149fe34da1b6bcbc08928654f268c7ac3e32b2e22599ae43cb701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733420"
---
# <a name="tcpip-characteristics"></a>TCP/IP-Merkmale

TCP/IP verfügt über Merkmale, die es dem Protokoll ermöglichen, wie es die standardisierten Implementierungsanforderungen vorschreiben. Diese Merkmale können mit Entwicklungsoptionen kombiniert werden, die zu einer schlechten Leistung führen. Die Auswirkungen dieser TCP/IP-Merkmale auf eine Anwendung hängen davon ab, ob es sich um eine Transaktion oder ein Streaming handelt.

Transaktionsanwendungen sind von dem Aufwand betroffen, der für die Verbindungseinrichtung und -beendigung erforderlich ist. Jedes Mal, wenn eine Verbindung in einem Ethernet-Netzwerk hergestellt wird, müssen beispielsweise drei Pakete mit jeweils ca. 60 Bytes gesendet werden, und für den Austausch ist ungefähr eine RTT erforderlich. Beim Beenden einer Verbindung werden vier Pakete ausgetauscht. Dies gilt für jede Verbindung. Eine Anwendung, die Verbindungen öffnet und schließt, verursacht häufig diesen Mehraufwand bei jedem Vorkommen.

Ein weiterer Aspekt von TCP/IP ist *der langsame Start,* der immer dann erfolgt, wenn eine Verbindung hergestellt wird. Der langsame Start ist ein künstlicher Grenzwert für die Anzahl der Datensegmente, die gesendet werden können, bevor eine Bestätigung dieser Segmente empfangen wird. Der langsame Start wurde entwickelt, um die Netzwerküberlastung zu begrenzen. Wenn unabhängig von der Fenstergröße des Empfängers eine Verbindung über Ethernet hergestellt wird, kann eine Übertragung mit 4 KB aufgrund eines langsamen Startes bis zu 3 bis 4 RTT dauern.

Eine TCP/IP-Optimierung namens Nagle-Algorithmus kann auch die Datenübertragungsgeschwindigkeit für eine Verbindung einschränken. Der Nagle-Algorithmus wurde entwickelt, um den Protokollaufwand für Anwendungen zu reduzieren, die kleine Datenmengen senden, z. B. Telnet, das gleichzeitig ein einzelnes Zeichen sendet. Anstatt sofort ein Paket mit vielen Headern und wenig Daten zu senden, wartet der Stapel auf weitere Daten aus der Anwendung oder eine Bestätigung, bevor der Vorgang fortfahren kann.

Verzögerte Bestätigungen, die häufig als verzögerte *ACK* bezeichnet werden, sind auch für TCP/IP konzipiert, um ein effizienteres Piggybacking von Bestätigungen zu ermöglichen, wenn Rückgabedaten von der empfangenden Anwendung anstehender werden. Wenn diese Daten nicht in Kürze angezeigt werden und die sendende Seite auf eine Bestätigung wartet, kann es zu Verzögerungen von ca. 200 Millisekunden pro Sendedaten kommen.

Wenn eine TCP-Verbindung geschlossen wird, werden Verbindungsressourcen auf dem Knoten, der das Schließen initiiert hat, in den Wartezustand TIME-WAIT aufgenommen, um datenverfälschungsgeschützt zu werden, wenn doppelte Pakete im Netzwerk vorhanden sind. Dadurch wird sichergestellt, dass beide Enden mit der Verbindung beendet werden. Dies kann zu einer Verknappung der pro Verbindung erforderlichen Ressourcen führen, z. B. RAM und Ports, wenn Anwendungen häufig Verbindungen öffnen und schließen.

Streaminganwendungen sind nicht nur von verzögerter ACK und anderen Überlastungsvermeidungsschemas betroffen, sondern können auch von einer zu kleinen Standardgröße des Empfangsfensters auf der Empfangende betroffen sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsverhalten](application-behavior-2.md)
</dt> <dt>

[Hochleistungsanwendungen Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Nagle-Algorithmus](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



