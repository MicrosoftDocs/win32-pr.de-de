---
title: Offline Kompilierung
description: Das Effekt-Compilertool (fxc.exe) ist für die Offline Kompilierung von HLSL-Shadern konzipiert.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- FXC, Offline Kompilierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729912"
---
# <a name="offline-compiling"></a>Offline Kompilierung

Das Effekt-Compilertool (fxc.exe) ist für die Offline Kompilierung von HLSL-Shadern konzipiert.

## <a name="compiling-with-the-current-compiler"></a>Kompilieren mit dem aktuellen Compiler

Die vom aktuellen Compiler unterstützten shadermodelle werden als [profile](dx-graphics-tools-fxc-syntax.md)angezeigt. In diesem Beispiel wird ein Pixelshader für das Shader-Modell 5,1-Ziel kompiliert.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

In diesem Beispiel:

-   PS \_ 5 \_ 1 ist das Ziel Profil.
-   PixelShader1. FXC ist die Ausgabe Objektdatei, die den kompilierten Shader enthält.
-   PixelShader1. HLSL ist die Quelle.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Die Debugoptionen enthalten zusätzliche Optionen zum Deaktivieren von Compileroptimierungen (od) und zum Aktivieren von Debuginformationen (Zi) wie Zeilennummern und Symbolen.

Eine vollständige Liste der Befehlszeilenoptionen finden Sie auf der Seite [Syntax](dx-graphics-tools-fxc-syntax.md) .

## <a name="compiling-with-the-legacy-compiler"></a>Kompilieren mit dem Legacy Compiler

Ab Direct3D 10 werden einige shadermodelle nicht mehr unterstützt. Hierzu zählen Pixel-shadermodelle: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 und PS \_ 1 \_ 4, die sehr begrenzte Ressourcen unterstützen und von der Hardware abhängig sind. Der Compiler wurde mit dem Shader-Modell 2 (oder höher) neu gestaltet, das eine größere Effizienz mit der Kompilierung ermöglicht. Dies erfordert natürlich, dass Sie auf Hardware ausgeführt werden, die Shader-Modelle 2 und höher unterstützt.

Beachten Sie außerdem, dass Sie sich die SDK-Versions Hinweise zu Ihrer Version des FXC-Compilers für das vom/GEC-Switch betroffene Verhalten ansehen sollten.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Verwenden des Effekts-Compiler-Tools in einem Teilprozess

Wenn fxc.exe von einer Anwendung als Teilprozess erzeugt wird, muss sichergestellt werden, dass die Anwendung alle Daten in der Ausgabe oder an Fehler Pipes überprüft und liest, die an die Funktion "deateprocess" übergeben werden. Wenn die Anwendung nur darauf wartet, dass der Teilprozess abgeschlossen wird und einer der Pipes voll ist, wird der Teilprozess nie beendet.

Der folgende Beispielcode veranschaulicht das warten auf einen Teilprozess und das Lesen der Ausgabe-und Fehler Pipes, die an den Teilprozess angefügt sind. Der Inhalt des `WaitHandles` Arrays entspricht Handles für den unter Prozess, der Pipe für "stdout" und der Pipe für "stderr".

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

Weitere Informationen zum Erzeugen eines Prozesses finden Sie auf der Referenzseite für " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)".

## <a name="related-topics"></a>Zugehörige Themen

* [Effekt-Compilertool](fxc.md)