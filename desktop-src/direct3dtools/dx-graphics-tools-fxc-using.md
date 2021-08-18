---
title: Offline kompilieren
description: Das Effektcompilertool (fxc.exe) ist für die Offlinekompilierung von HLSL-Shadern konzipiert.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc, offline kompilieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a15d3a71dbfb79541a75bd38cb28140d832b45e75a88a52b2d0c8988865f12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406330"
---
# <a name="offline-compiling"></a>Offline kompilieren

Das Effektcompilertool (fxc.exe) ist für die Offlinekompilierung von HLSL-Shadern konzipiert.

## <a name="compiling-with-the-current-compiler"></a>Kompilieren mit dem aktuellen Compiler

Die vom aktuellen Compiler unterstützten Shadermodelle werden unter Profile [angezeigt.](dx-graphics-tools-fxc-syntax.md) In diesem Beispiel wird ein Pixel-Shader für das Shadermodell 5.1-Ziel kompiliert.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

In diesem Beispiel:

-   ps \_ 5 \_ 1 ist das Zielprofil.
-   PixelShader1.fxc ist die Ausgabeobjektdatei, die den kompilierten Shader enthält.
-   PixelShader1.hlsl ist die Quelle.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Die Debugoptionen enthalten zusätzliche Optionen, um Compileroptimierungen (Od) zu deaktivieren und Debuginformationen (Zi) wie Zeilennummern und Symbole zu aktivieren.

Eine vollständige Liste der Befehlszeilenoptionen finden Sie auf der [Seite Syntax.](dx-graphics-tools-fxc-syntax.md)

## <a name="compiling-with-the-legacy-compiler"></a>Kompilieren mit dem Legacycompiler

Ab Direct3D 10 werden einige Shadermodelle nicht mehr unterstützt. Dazu gehören Pixel-Shadermodelle: ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 3 und ps \_ \_ 1 \_ 4, die sehr eingeschränkte Ressourcen unterstützen und von Hardware abhängig sind. Der Compiler wurde mit Shadermodell 2 (oder höher) umgestaltet, was eine höhere Effizienz bei der Kompilierung ermöglicht. Dies erfordert natürlich, dass Sie auf Hardware ausführen, die Shadermodelle ab 2 unterstützt.

Beachten Sie auch, dass Sie die SDK-Versionshinweise, die Ihrer Version des FXC-Compilers zugeordnet sind, für das Verhalten lesen sollten, das vom Schalter /Gec betroffen ist.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Verwenden des Effektcompilertools in einem Unterprozess

Wenn fxc.exe anwendung als Unterprozess erstellt wird, ist es wichtig sicherzustellen, dass die Anwendung alle Daten in Ausgabe- oder Fehlerpipes überprüft und liest, die an die CreateProcess-Funktion übergeben werden. Wenn die Anwendung nur auf den Abschluss des Unterprozesses wartet und einer der Pipes voll ist, wird der Unterprozess nie beendet.

Der folgende Beispielcode veranschaulicht das Warten auf einen Unterprozess und das Lesen der Ausgabe- und Fehlerpipes, die an den Unterprozess angefügt sind. Der Inhalt des Arrays entspricht Handles für den Unterprozess, der Pipe für `WaitHandles` stdout und der Pipe für stderr.

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

Weitere Informationen zum Erzeugen eines Prozesses finden Sie auf der Referenzseite für [**CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

## <a name="related-topics"></a>Zugehörige Themen

* [Effect-Compiler-Tool](fxc.md)