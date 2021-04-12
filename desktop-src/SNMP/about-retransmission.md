---
title: Informationen zur erneuten Übertragung
description: Eine WinSNMP-Anwendung kann SNMP-Vorgangs Anforderungen auf verschiedene Weise ausführen.
ms.assetid: 71150a66-74a3-4957-bc70-3dd25c3b9c71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a26ba632cec096300927911c2277cbcf5911e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309599"
---
# <a name="about-retransmission"></a>Informationen zur erneuten Übertragung

Eine WinSNMP-Anwendung kann SNMP-Vorgangs Anforderungen auf verschiedene Weise ausführen. Die Anwendung kann mehrere Anforderungen an einen SNMP-Agent ausgeben, ohne auf eine Antwort zu warten, oder es kann eine einzelne Anforderung ausgeben und auf die Antwort warten. Da SNMP in mehreren Transportprotokollen implementiert werden kann, können Übermittlungs Mechanismen und Zuverlässigkeits Merkmale variieren.

Wenn Sie die WinSNMP-Anwendung programmieren, müssen Sie den Grad der Zuverlässigkeit ermitteln, den Sie für Kommunikations Vorgänge benötigen, basierend auf der Art und Weise, in der die Anwendung Vorgangs Anforderungen ausgibt. Anschließend müssen Sie eine Neuübertragungs Strategie auswählen und eine Richtlinie für die erneute Übertragung implementieren.

Eine Richtlinie für Neuübertragungen umfasst einen Timeout Zeitraum und eine Wiederholungs Anzahl. Ein Timeout Zeitraum ist die verstrichene Zeit (in Hundertstel Sekunden) zwischen der Ausgabe einer [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) -Anforderung einer Anwendung und dem Empfang der entsprechenden Nachricht. Die Anwendung empfängt die Nachricht als Ergebnis eines Aufrufes der [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion. Der Timeout Wert ist die Zeitspanne, die die Microsoft WinSNMP-Implementierung darauf wartet, dass eine Entität auf eine Kommunikations Anforderung antwortet. Wenn innerhalb des Timeout Zeitraums keine Antwort vorhanden ist, wird die Anforderung von der Implementierung entweder erneut übermittelt, wenn der Wert für die Wiederholungs Anzahl Neuübertragungs Versuche angibt, oder der Aufruf von [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)schlägt fehl. Eine Wiederholungs Anzahl ist die maximale Anzahl von Neuübertragungs versuchen, die die Implementierung durchführt, wenn eine SNMP-Übertragungs Anforderung fehlschlägt.

Die-Implementierung speichert Timeout Werte und die Anzahl der Wiederholungs Versuche in der Datenbank für die Anwendung. Die-Implementierung speichert einzelne Werte für jede Ziel Entität.

Anwendungen müssen eigene Abruf Frequenzen einrichten und Zeit Geber Variablen verwalten. Weitere Informationen finden Sie unter [Verwalten der Richtlinie für Neuübertragungen](managing-the-retransmission-policy.md).

 

 




