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
# <a name="offline-compiling"></a><span data-ttu-id="c60a8-104">Offline Kompilierung</span><span class="sxs-lookup"><span data-stu-id="c60a8-104">Offline compiling</span></span>

<span data-ttu-id="c60a8-105">Das Effekt-Compilertool (fxc.exe) ist für die Offline Kompilierung von HLSL-Shadern konzipiert.</span><span class="sxs-lookup"><span data-stu-id="c60a8-105">The effect-compiler tool (fxc.exe) is designed for offline compilation of HLSL shaders.</span></span>

## <a name="compiling-with-the-current-compiler"></a><span data-ttu-id="c60a8-106">Kompilieren mit dem aktuellen Compiler</span><span class="sxs-lookup"><span data-stu-id="c60a8-106">Compiling with the current compiler</span></span>

<span data-ttu-id="c60a8-107">Die vom aktuellen Compiler unterstützten shadermodelle werden als [profile](dx-graphics-tools-fxc-syntax.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c60a8-107">The shader models supported by the current compiler are shown in [Profiles](dx-graphics-tools-fxc-syntax.md).</span></span> <span data-ttu-id="c60a8-108">In diesem Beispiel wird ein Pixelshader für das Shader-Modell 5,1-Ziel kompiliert.</span><span class="sxs-lookup"><span data-stu-id="c60a8-108">This example compiles a pixel shader for the shader model 5.1 target.</span></span>

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="c60a8-109">In diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c60a8-109">In this example:</span></span>

-   <span data-ttu-id="c60a8-110">PS \_ 5 \_ 1 ist das Ziel Profil.</span><span class="sxs-lookup"><span data-stu-id="c60a8-110">ps\_5\_1 is the target profile.</span></span>
-   <span data-ttu-id="c60a8-111">PixelShader1. FXC ist die Ausgabe Objektdatei, die den kompilierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="c60a8-111">PixelShader1.fxc is the output object file containing the compiled shader.</span></span>
-   <span data-ttu-id="c60a8-112">PixelShader1. HLSL ist die Quelle.</span><span class="sxs-lookup"><span data-stu-id="c60a8-112">PixelShader1.hlsl is the source.</span></span>

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="c60a8-113">Die Debugoptionen enthalten zusätzliche Optionen zum Deaktivieren von Compileroptimierungen (od) und zum Aktivieren von Debuginformationen (Zi) wie Zeilennummern und Symbolen.</span><span class="sxs-lookup"><span data-stu-id="c60a8-113">The debug options include additional options to disable compiler optimizations (Od) and enable debug information (Zi) like line numbers and symbols.</span></span>

<span data-ttu-id="c60a8-114">Eine vollständige Liste der Befehlszeilenoptionen finden Sie auf der Seite [Syntax](dx-graphics-tools-fxc-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="c60a8-114">For a full listing of the command-line options, see the [Syntax](dx-graphics-tools-fxc-syntax.md) page.</span></span>

## <a name="compiling-with-the-legacy-compiler"></a><span data-ttu-id="c60a8-115">Kompilieren mit dem Legacy Compiler</span><span class="sxs-lookup"><span data-stu-id="c60a8-115">Compiling with the legacy compiler</span></span>

<span data-ttu-id="c60a8-116">Ab Direct3D 10 werden einige shadermodelle nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c60a8-116">Beginning with Direct3D 10, some shader models are no longer supported.</span></span> <span data-ttu-id="c60a8-117">Hierzu zählen Pixel-shadermodelle: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 und PS \_ 1 \_ 4, die sehr begrenzte Ressourcen unterstützen und von der Hardware abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="c60a8-117">These include pixel shader models: ps\_1\_1, ps\_1\_2, ps\_1\_3, and ps\_1\_4 which support very limited resources and are dependent on hardware.</span></span> <span data-ttu-id="c60a8-118">Der Compiler wurde mit dem Shader-Modell 2 (oder höher) neu gestaltet, das eine größere Effizienz mit der Kompilierung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c60a8-118">The compiler has been redesigned with shader model 2 (or greater) which allows for greater efficiencies with compilation.</span></span> <span data-ttu-id="c60a8-119">Dies erfordert natürlich, dass Sie auf Hardware ausgeführt werden, die Shader-Modelle 2 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c60a8-119">This of course will require that you are running on hardware that supports shader models 2 and greater.</span></span>

<span data-ttu-id="c60a8-120">Beachten Sie außerdem, dass Sie sich die SDK-Versions Hinweise zu Ihrer Version des FXC-Compilers für das vom/GEC-Switch betroffene Verhalten ansehen sollten.</span><span class="sxs-lookup"><span data-stu-id="c60a8-120">Also note that you should consult the SDK release notes associated with your version of the FXC compiler for behavior affected by the /Gec switch.</span></span>

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a><span data-ttu-id="c60a8-121">Verwenden des Effekts-Compiler-Tools in einem Teilprozess</span><span class="sxs-lookup"><span data-stu-id="c60a8-121">Using the effect-compiler tool in a subprocess</span></span>

<span data-ttu-id="c60a8-122">Wenn fxc.exe von einer Anwendung als Teilprozess erzeugt wird, muss sichergestellt werden, dass die Anwendung alle Daten in der Ausgabe oder an Fehler Pipes überprüft und liest, die an die Funktion "deateprocess" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c60a8-122">If fxc.exe is spawned as a subprocess by an application it is important to ensure that the application checks for and reads any data in output or error pipes passed to the CreateProcess function.</span></span> <span data-ttu-id="c60a8-123">Wenn die Anwendung nur darauf wartet, dass der Teilprozess abgeschlossen wird und einer der Pipes voll ist, wird der Teilprozess nie beendet.</span><span class="sxs-lookup"><span data-stu-id="c60a8-123">If the application only waits for the subprocess to finish and one of the pipes becomes full the subprocess will never finish.</span></span>

<span data-ttu-id="c60a8-124">Der folgende Beispielcode veranschaulicht das warten auf einen Teilprozess und das Lesen der Ausgabe-und Fehler Pipes, die an den Teilprozess angefügt sind.</span><span class="sxs-lookup"><span data-stu-id="c60a8-124">The following example code illustrates waiting on a subprocess and reading the output and error pipes attached to the subprocess.</span></span> <span data-ttu-id="c60a8-125">Der Inhalt des `WaitHandles` Arrays entspricht Handles für den unter Prozess, der Pipe für "stdout" und der Pipe für "stderr".</span><span class="sxs-lookup"><span data-stu-id="c60a8-125">The contents of the `WaitHandles` array correspond to handles for the subprocess, the pipe for stdout and the pipe for stderr.</span></span>

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

<span data-ttu-id="c60a8-126">Weitere Informationen zum Erzeugen eines Prozesses finden Sie auf der Referenzseite für " [**kreateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)".</span><span class="sxs-lookup"><span data-stu-id="c60a8-126">For additional information on spawning a process see the reference page for [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c60a8-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c60a8-127">Related topics</span></span>

* [<span data-ttu-id="c60a8-128">Effekt-Compilertool</span><span class="sxs-lookup"><span data-stu-id="c60a8-128">Effect-Compiler Tool</span></span>](fxc.md)