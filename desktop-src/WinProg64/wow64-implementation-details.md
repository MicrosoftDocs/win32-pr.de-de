---
title: WOW64-Implementierungs Details
description: Der WOW64-Emulator wird im Benutzermodus ausgeführt.
ms.assetid: 93daf9d0-dfdb-42c3-8c3d-397b21991e83
keywords:
- WOW64 64-Bit-Windows-Programmierung, Umgebungsvariablen
- WOW64 64-Bit-Windows-Programmierung, Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7d095369b883171e39bffd4dc629b7f80a7f39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101827"
---
# <a name="wow64-implementation-details"></a>WOW64-Implementierungs Details

Der WOW64-Emulator wird im Benutzermodus ausgeführt. Sie stellt eine Schnittstelle zwischen der 32-Bit-Version von Ntdll.dll und dem Kernel des Prozessors bereit und fängt Kernel Aufrufe ab. Der WOW64-Emulator besteht aus den folgenden DLLs:

-   Wow64.dll stellt die Kern Emulations Infrastruktur und die thunge für die Ntoskrnl.exe-Einstiegspunkt Funktionen bereit.
-   Wow64Win.dll stellt thunas für die Win32k.sys-Einstiegspunkt Funktionen bereit.
-   (nur x64) Wow64Cpu.dll bietet Unterstützung für die Ausführung von x86-Programmen auf x64.
-   (Nur Intel Itanium) IA32Exec. bin enthält den x86-Software Emulator.
-   (Nur Intel Itanium) Wowia32x.dll die Schnittstelle zwischen IA32Exec. bin und WOW64 bereitstellt.
-   (Nur ARM64) xtajit.dll enthält den x86-Software Emulator.
-   (Nur ARM64) wowarmw.dll bietet Unterstützung für die Ausführung von ARM32-Programmen auf ARM64.

Diese DLLs sind zusammen mit der 64-Bit-Version von Ntdll.dll die einzigen 64-Bit-Binärdateien, die in einen 32-Bit-Prozess geladen werden können. Unter Windows 10 auf ARM können auch CHPE-Binärdateien (kompilierte hybride portable ausführbare Dateien) in einen x86 32-Bit-Prozess geladen werden.

Beim Start lädt Wow64.dll die x86-Version von Ntdll.dll (oder die CHPE-Version, sofern aktiviert) und führt den Initialisierungs Code aus, der alle erforderlichen 32-Bit-DLLs lädt. Fast alle 32-Bit-DLLs sind nicht geänderte Kopien 32 von 32-Bit-Windows-Binärdateien, obwohl einige aus Leistungsgründen als CHPE geladen werden. Einige dieser DLLs unterscheiden sich auf WOW64 anders als bei 32-Bit-Fenstern, in der Regel, weil Sie Arbeitsspeicher mit 64-Bit-Systemkomponenten gemeinsam nutzen. Der gesamte Benutzermodus-Adressraum über dem 32-Bit-Limit ist vom System reserviert. Weitere Informationen finden Sie [unterleistung und Arbeitsspeicher Nutzung unter WOW64](performance-and-memory-consumption.md).

Anstatt die x86-Systemdienst-Aufruf Sequenz zu verwenden, werden 32-Bit-Binärdateien, die Systemaufrufe ausführen, neu erstellt, um eine benutzerdefinierte Aufruf Sequenz zu verwenden. Diese Aufruf Sequenz ist preiswert, damit WOW64 abgefangen wird, da Sie vollständig im Benutzermodus bleibt. Wenn die benutzerdefinierte Aufruf Sequenz erkannt wird, wechselt die WOW64-CPU zurück in den nativen 64-Bit-Modus und ruft Wow64.dll auf. Thunking wird im Benutzermodus durchgeführt, um die Auswirkung auf den 64-Bit-Kernel zu verringern und das Risiko eines Fehlers im Thunk zu verringern, der einen Absturz des Kernelmodus, eine Beschädigung von Daten oder eine Sicherheitslücke verursachen kann. Die thungs extrahieren Argumente aus dem 32-Bit-Stapel, erweitern Sie auf 64 Bits und führen dann den systemeigenen System Rückruf aus.

## <a name="environment-variables"></a>Umgebungsvariablen

Wenn ein 32-Bit-Prozess von einem 64-Bit-Prozess erstellt wird oder ein 64-Bit-Prozess von einem 32-Bit-Prozess erstellt wird, legt WOW64 die Umgebungsvariablen für den erstellten Prozess fest, wie in der folgenden Tabelle gezeigt.



| Prozess                   | Umgebungsvariablen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 64-Bit-Prozess<br/> | Prozessor \_ Architektur = amd64 oder Prozessor \_ Architektur = ia64 oder Prozessor \_ Architektur = ARM64<br/> Program Files =% Program Files%<br/> ProgramW6432 =% Program Files%<br/> COMMONPROGRAM files =% COMMONPROGRAMFILES%<br/> CommonProgramW6432 =% COMMONPROGRAMFILES%<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Die Umgebungsvariablen ProgramW6432 und CommonProgramW6432 wurden ab Windows 7 und Windows Server 2008 R2 hinzugefügt. <br/> |
| 32-Bit-Prozess<br/> | Prozessor \_ Architektur = x86<br/> Prozessor \_ ARCHITEW6432 =% Prozessor \_ Architektur%<br/> Program Files =% Program Files (x86)%<br/> ProgramW6432 =% Program Files%<br/> COMMONPROGRAM files =% COMMONPROGRAMFILES (x86)%<br/> CommonProgramW6432 =% COMMONPROGRAMFILES%<br/>                                                                                                                                                                                                                  |



 

## <a name="global-hooks"></a>Globale Hooks

Die Funktion " [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) " kann verwendet werden, um eine DLL in einen anderen Prozess einzufügen, wenn die folgenden Bedingungen erfüllt sind:

-   Eine 32-Bit-DLL kann nur in einen 32-Bit-Prozess eingefügt werden, und eine 64-Bit-DLL kann nur in einen 64-Bit-Prozess eingefügt werden. Es ist nicht möglich, eine 32-Bit-DLL in einen 64-Bit-Prozess einzufügen oder umgekehrt.
-   Die 32-Bit-und 64-Bit-DLLs müssen unterschiedliche Namen aufweisen.
-   Die Architekturen der dll und der Prozess müssen mit identisch sein. Beispielsweise können Sie eine 32-Bit-x86-dll nicht in einen 32-Bit-ARM-Prozess einfügen.

Weitere Informationen finden Sie unter [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).

Beachten Sie, dass die " **WH \_ Mouse**", " **WH \_ Keyboard**", " **WH \_ Journal \***", " **WH \_ Shell**" und "Low-Level Hooks" für den Thread aufgerufen werden können, der den Hook installiert hat, anstatt den Thread, der den Hook Für diese Hooks ist es möglich, dass sowohl die 32-Bit-als auch die 64-Bit-Hooks aufgerufen werden, wenn ein 32-Bit-Hook vor einem 64-Bit-Hook in der Hook-Kette liegt. Weitere Informationen finden Sie unter [Verwenden von Hooks](../winmsg/using-hooks.md).

 

