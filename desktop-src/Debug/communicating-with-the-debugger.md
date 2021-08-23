---
description: Die OutputDebugString-Funktion sendet eine Zeichenfolge aus dem Prozess, der gedebuggt wird, an den Debugger, indem ein Debugereignis OUTPUT DEBUG STRING EVENT generiert \_ \_ \_ wird. Ein Prozess kann erkennen, ob er gedebuggt wird, indem er die IsDebuggerPresent-Funktion aufruft.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Kommunizieren mit dem Debugger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee4d78fc2b0cef1df9f0597a816966585d00e1041711d4712d1a1fa66639e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692060"
---
# <a name="communicating-with-the-debugger"></a>Kommunizieren mit dem Debugger

Die [**OutputDebugString-Funktion**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) sendet eine Zeichenfolge aus dem Prozess, der gedebuggt wird, an den Debugger, indem ein Debugereignis OUTPUT DEBUG STRING EVENT generiert \_ \_ \_ wird. Ein Prozess kann erkennen, ob er gedebuggt wird, indem er die [**IsDebuggerPresent-Funktion aufruft.**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)

Die [**DebugBreak-Funktion**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) löst eine Breakpointausnahme im aktuellen Prozess aus. Ein Haltepunkt ist ein Speicherort in einem Programm, an dem die Ausführung beendet wird, damit der Entwickler den Code, die Variablen und die Registerwerte des Programms untersuchen und ggf. Änderungen vornehmen, die Ausführung fortsetzen oder die Ausführung beenden kann.

Die [**FatalExit-Funktion**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) beendet den aktuellen Prozess und übergibt dem Debugger die Ausführungssteuerung. Im Gegensatz zu [**Debugbreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)generiert sie jedoch keine Ausnahme. Diese Funktion sollte nur als letzte Möglichkeit verwendet werden, da sie nicht immer den Arbeitsspeicher des Prozesses frei macht oder ihre Dateien schließt.

 

 
