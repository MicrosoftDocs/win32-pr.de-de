---
description: 'Microsoft Message Queuing (MSMQ): Verbesserte Warteschlangenbehandlung'
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: 'Microsoft Message Queuing (MSMQ): Verbesserte Warteschlangenbehandlung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4de125062dfdd705165e83e8a34d2bc0ef595eb08b6152d37aed5520e9ed39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053058"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a>Microsoft Message Queuing (MSMQ): Verbesserte Warteschlangenbehandlung

## <a name="platforms"></a>Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Niedrig  
**Häufigkeit** : Niedrig  





## <a name="description"></a>Beschreibung

Der MSMQ-Dienst legt keine harte Grenze für die Anzahl der Warteschlangen fest, die auf einem System erstellt werden können. Die Leistung des Systems wird jedoch beeinträchtigt, wenn eine große Anzahl von Warteschlangen erstellt wird. Insbesondere wenn mehr als ein paar Tausend Warteschlangen vorhanden sind, erhöht sich die Startzeit des MSMQ-Diensts exponentiell, was zu sichtbaren Auswirkungen führt.

Microsoft hat das Starten des MSMQ-Diensts in Windows 7 optimiert, um den Suchaufwand für das Laden der Warteschlangen in den Arbeitsspeicher zu reduzieren. Diese Optimierung hat zu einer erheblichen Verbesserung der Startzeit des MSMQ-Diensts geführt, auch wenn mehrere Tausend Warteschlangen im System erstellt werden.

## <a name="manifestation-of-impact"></a>Auswirkungen

Diese Leistungsverbesserung wirkt sich nicht auf die Funktionalität einer vorhandenen Anwendung aus.

## <a name="leveraging-the-changed-feature"></a>Nutzen der geänderten Funktion

Anwendungsentwickler, die MSMQ auf Windows 7 verwenden, können jetzt ihre Lösungen entwerfen, ohne die Anzahl der Warteschlangen einzuschränken. Beachten Sie, dass sich die Anzahl der Warteschlangen weiterhin auf die Gesamtleistung des MSMQ-Servers auswirkt, die Leistungsbeeinträchtigung jedoch jetzt linear und nicht exponentiell ist.

## <a name="compatibility-performance-reliability-and-usability-tests"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

Wenn Sie eine große Anzahl von Warteschlangen verwenden, simulieren Sie die Produktionsumgebung auf einem Testbett, überwachen Sie die Leistung, und analysieren Sie die Startzeit des Diensts und den Nachrichtendurchsatz mit einer großen Anzahl von Warteschlangen und Nachrichten, die im Testsystem vorhanden sind.

 

 



