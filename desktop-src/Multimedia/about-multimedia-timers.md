---
title: Informationen zu multimeditimern
description: Informationen zu multimeditimern
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows-Multimedia, Timer
- Multimedia, Timer
- Multimedia-Eingabe, Timer
- Multimedia-Timer, Informationen zu
- Timer, Info
- Multimedia-Timer, Planungs Ereignisse
- Timer, Zeit Planungs Ereignisse
- Planen von Zeit Geber Ereignissen
- Zeitüberschreitung bei hoher Auflösung
- Funktion "Funktion"
- Funktion "kreatewaitabletimer"
- WM_TIMER Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c36e5f19a92b6b47a3b1976bd85aadef88ab3ec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038927"
---
# <a name="about-multimedia-timers"></a>Informationen zu multimeditimern

Multimedietdienste ermöglichen es Anwendungen, Zeit Geber Ereignisse mit der größtmöglichen Auflösung (oder Genauigkeit) für die Hardwareplattform zu planen. Diese Multimedia-Timer-Dienste ermöglichen es Ihnen, Zeit Geber Ereignisse in einer höheren Auflösung als andere Zeit Geber Dienste zu planen.

Diese Timer-Dienste sind für Anwendungen nützlich, die eine Zeitüberschreitung mit hoher Auflösung erfordern. Beispielsweise erfordert ein "MIDI Sequencer" einen Zeit Geber mit hoher Auflösung, da er die Geschwindigkeit von "MIDI"-Ereignissen innerhalb einer Auflösung von 1 Millisekunden aufrechterhalten muss.

Anwendungen, die keine Zeitüberschreitung mit hoher Auflösung verwenden, sollten [die Funktion](/windows/win32/api/winuser/nf-winuser-settimer) "-Funktion" anstelle von Multimedia-Timer-Diensten verwenden. Die **von "** " bereitgestellten Timer-Dienste stellen Zeit Geber Nachrichten in einer Nachrichten Warteschlange bereit, während die Multimediatimer-Dienste eine Rückruffunktion aufzurufen. [ \_](../winmsg/wm-timer.md) Anwendungen, die einen aktivierbaren Timer benötigen, sollten die Funktion " [kreatewaitabletimer](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) " verwenden.

 

 