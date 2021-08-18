---
title: Informationen zur Neuübertragung
description: Eine WinSNMP-Anwendung kann SNMP-Vorgangsanforderungen auf verschiedene Weise senden.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade0b2d58f371de87be5da855f26686a18518454c787c6a09e9701afbb731757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009958"
---
# <a name="about-retransmission"></a>Informationen zur Neuübertragung

Eine WinSNMP-Anwendung kann SNMP-Vorgangsanforderungen auf verschiedene Weise senden. Die Anwendung kann mehrere Anforderungen an einen SNMP-Agent senden, ohne auf eine Antwort zu warten, oder sie kann eine einzelne Anforderung senden und auf die Antwort warten. Da SNMP für mehrere Transportprotokolle implementiert werden kann, können Übermittlungsmechanismen und Zuverlässigkeitsmerkmale variieren.

Wenn Sie die WinSNMP-Anwendung codieren, müssen Sie den Zuverlässigkeitsgrad bestimmen, den Sie für Kommunikationsvorgänge benötigen, basierend auf der Art und Weise, wie die Anwendung Vorgangsanforderungen aus stellt. Anschließend müssen Sie eine Neuübertragungsstrategie auswählen und eine Neuübertragungsrichtlinie implementieren.

Eine Neuübertragungsrichtlinie enthält einen Time out-Zeitraum und eine Wiederholungsanzahl. Ein Time out-Zeitraum ist die verstrichene Zeit in 1/100 Sekunden zwischen der Ausstellung einer [**SnmpSendMsg-Anforderung**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) durch eine Anwendung und dem Empfang der entsprechenden Nachricht. Die Anwendung empfängt die Nachricht als Ergebnis eines Aufrufs der [**SnmpRecvMsg-Funktion.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) Der Time out-Wert ist der Zeitraum, in dem die Microsoft WinSNMP-Implementierung wartet, bis eine Entität auf eine Kommunikationsanforderung antwortet. Wenn innerhalb des Time outzeitraums keine Antwort auftritt, überträgt die Implementierung die Anforderung entweder erneut, wenn der Wert der Wiederholungsanzahl Neuübertragungsversuche angibt, oder der Aufruf von [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)schlägt fehl. Eine Wiederholungsanzahl ist die maximale Anzahl von Neuübertragungsversuchen, die die Implementierung vorschlägt, wenn eine SNMP-Übertragungsanforderung fehlschlägt.

Die Implementierung speichert Time out-Werte und Wiederholungsanzahlen in ihrer Datenbank für die Anwendung. Die Implementierung speichert einzelne Werte für jede Zielentität.

Anwendungen müssen eigene Abrufhäufigkeiten einrichten und Timervariablen verwalten. Weitere Informationen finden Sie unter [Verwalten der Neuübertragungsrichtlinie.](managing-the-retransmission-policy.md)

 

 




