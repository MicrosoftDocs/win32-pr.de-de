---
description: Die OutputDebugString-Funktion sendet eine Zeichenfolge vom debuggten Prozess an den Debugger, indem ein Debug-Ereignis für das Debugger-Ereignis erzeugt wird \_ \_ \_ . Ein Prozess kann erkennen, ob er durch Aufrufen der isdebuggerpresent-Funktion gedebuggt wird.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Kommunikation mit dem Debugger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860582"
---
# <a name="communicating-with-the-debugger"></a>Kommunikation mit dem Debugger

Die [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) -Funktion sendet eine Zeichenfolge vom \_ debuggten Prozess an den Debugger, indem ein Debug-Ereignis für das Debugger-Ereignis erzeugt wird \_ \_ . Ein Prozess kann erkennen, ob er durch Aufrufen der [**isdebuggerpresent-Funktion gedebuggt**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) wird.

Die [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) -Funktion verursacht eine breakpointausnahme im aktuellen Prozess. Ein Haltepunkt ist eine Position in einem Programm, an der die Ausführung angehalten wird, damit der Entwickler den Code, die Variablen und die Registerwerte des Programms untersuchen und ggf. Änderungen vornehmen, die Ausführung fortsetzen oder die Ausführung beenden kann.

Die Funktion [**fatalexit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) beendet den aktuellen Prozess und übergibt die Ausführungs Steuerung an den Debugger, aber im Gegensatz zu [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)wird keine Ausnahme generiert. Diese Funktion sollte nur als letztes Mittel verwendet werden, da Sie nicht immer den Arbeitsspeicher des Prozesses freigibt oder die Dateien schließt.

 

 
