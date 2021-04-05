---
title: Zeit Geber Auflösung
description: Zeit Geber Auflösung
ms.assetid: 2e5e94fe-8175-417f-8c59-9d5cf052ea89
keywords:
- Multimedia-Timer, Lösung
- Timer, Auflösung
- minimale Zeit Geber Auflösung
- maximale Zeit Geber Auflösung
- Multimedia-Timer, maximale Auflösung
- Timer, maximale Auflösung
- Multimedia-Timer, minimale Auflösung
- Timer, minimale Auflösung
- timegetdevcaps-Funktion
- TimeBeginPeriod-Funktion
- timeendperiod-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e96f1b410f2e18203af794ea124bb6b83bccce
ms.sourcegitcommit: a0b531d335bc691100149830b256d5af7e136c24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2019
ms.locfileid: "103706990"
---
# <a name="timer-resolution"></a>Zeit Geber Auflösung

Um die minimalen und maximalen Zeit Geber Auflösungen zu ermitteln, die von den Timer-Diensten unterstützt werden, verwenden Sie die Funktion [**timegetdevcaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) . Diese Funktion füllt die **Member wperiodmin** und **wperiodmax** der [**timecaps**](/windows/desktop/api/TimeAPI/ns-timeapi-timecaps) -Struktur mit der minimalen und maximalen Auflösung aus. Dieser Bereich kann sich zwischen Computern und Windows-Plattformen unterscheiden.

Nachdem Sie die minimale und die maximale Anzahl verfügbarer Zeit Geber Auflösungen festgelegt haben, müssen Sie die minimale Auflösung einrichten, die von der Anwendung verwendet werden soll. Verwenden Sie die [**TimeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) -und [**timeendperiod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod) -Funktionen, um diese Auflösung festzulegen und zu löschen. Sie müssen jeden Aufruf von **TimeBeginPeriod** mit einem Aufruf von **timeendperiod** vergleichen und dabei dieselbe minimale Auflösung in beiden Aufrufen angeben. Eine Anwendung kann mehrere **TimeBeginPeriod** -Aufrufe durchführen, solange jeder Aufruf mit einem Aufruf von **timeendperiod** übereinstimmt.

In [**TimeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) und [**timeendperiod**](/windows/desktop/api/TimeAPI/nf-timeapi-timeendperiod)gibt der *uperiod* -Parameter die minimale Zeit Geber Auflösung in Millisekunden an. Sie können einen beliebigen Zeit Geber Auflösungswert innerhalb des Bereichs angeben, der vom Timer unterstützt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu multimeditimern](about-multimedia-timers.md)
</dt> </dl>

 

 




