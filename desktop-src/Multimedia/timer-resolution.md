---
title: Timerauflösung
description: Timerauflösung
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- Multimediatimer, Auflösung
- Timer, Auflösung
- Minimale Timerauflösung
- Maximale Timerauflösung
- Multimediatimer, maximale Auflösung
- Timer, maximale Auflösung
- Multimediatimer, Mindestauflösung
- Timer, Mindestauflösung
- timeGetDevCaps-Funktion
- timeBeginPeriod-Funktion
- timeEndPeriod-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948e81228acec27e41d43d41de7393ad64345acce25a450e91c815b1bbbf5164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781830"
---
# <a name="timer-resolution"></a>Timerauflösung

Verwenden Sie die [**timeGetDevCaps-Funktion,**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) um die minimalen und maximalen Timerauflösungen zu bestimmen, die von den Timerdiensten unterstützt werden. Diese Funktion füllt die **wPeriodMin-** und **wPeriodMax-Member** der [**TIMECAPS-Struktur**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) mit der minimalen und maximalen Auflösung. Dieser Bereich kann computer- und Windows Plattformen variieren.

Nachdem Sie die minimalen und maximalen verfügbaren Timerauflösungen ermittelt haben, müssen Sie die Mindestauflösung festlegen, die ihre Anwendung verwenden soll. Verwenden Sie die Funktionen [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) und [**timeEndPeriod,**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) um diese Auflösung festzulegen und zu löschen. Sie müssen jeden Aufruf von **timeBeginPeriod** mit einem Aufruf von **timeEndPeriod** abgleichen und dabei die gleiche Mindestauflösung in beiden Aufrufen angeben. Eine Anwendung kann mehrere **timeBeginPeriod-Aufrufe** ausführen, solange jeder Aufruf mit einem Aufruf von **timeEndPeriod** übereinstimmt.

Sowohl in [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) als auch [**in timeEndPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)gibt der *uPeriod-Parameter* die minimale Timerauflösung in Millisekunden an. Sie können einen beliebigen Timerauflösungswert innerhalb des vom Timer unterstützten Bereichs angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Multimediatimern](about-multimedia-timers.md)
</dt> </dl>

 

 




