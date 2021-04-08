---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ)-verbesserte Warteschlangen Behandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959958"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>Microsoft Message Queuing (MSMQ)-verbesserte Warteschlangen Behandlung

## <a name="platforms"></a>Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -niedrig  





## <a name="description"></a>BESCHREIBUNG

Der MSMQ-Dienst schränkt die Anzahl der Warteschlangen, die auf einem System erstellt werden können, nicht ein. Die Leistung des Systems ist jedoch beeinträchtigt, wenn eine große Anzahl von Warteschlangen erstellt wird. Insbesondere bei mehr als wenigen tausend Warteschlangen erhöht sich die Startzeit des MSMQ-Dienstanbieter exponentiell, was zu einer sichtbaren Auswirkung führt.

Microsoft hat den MSMQ-Dienst Start in Windows 7 optimiert, um den Suchaufwand für das Laden der Warteschlangen in den Arbeitsspeicher zu reduzieren. Diese Optimierung hat zu einer drastischen Verbesserung der Startzeit des MSMQ-Dienstanbieter geführt, auch wenn mehrere tausend Warteschlangen im System erstellt wurden.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

Diese Leistungsverbesserung wirkt sich nicht auf die Funktionalität einer vorhandenen Anwendung aus.

## <a name="leveraging-the-changed-feature"></a>Nutzen der geänderten Funktion

Anwendungsentwickler, die MSMQ unter Windows 7 verwenden, können jetzt Ihre Lösungen entwerfen, ohne die Anzahl der Warteschlangen einzuschränken. Beachten Sie, dass sich die Anzahl der Warteschlangen weiterhin auf die Gesamtleistung des MSMQ-Servers auswirkt, aber die Auswirkungen auf die Leistung auf eine lineare statt auf exponentielle Skalierung.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits-und Nutz barkeits Tests

Wenn Sie eine große Anzahl von Warteschlangen verwenden, simulieren Sie die Produktionsumgebung auf einem Testkonto, überwachen Sie die Leistung, und analysieren Sie die Startzeit und den Nachrichten Durchsatz mit einer großen Anzahl von Warteschlangen und Nachrichten, die im Testsystem vorhanden sind.

 

 



