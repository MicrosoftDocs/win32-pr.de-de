---
description: In diesem Thema werden allgemeine Kategorien von Problemen aufgeführt, die beim Schreiben von Direct3D-Anwendungen auftreten können, und wie Sie verhindert werden.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Problembehandlung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342741"
---
# <a name="troubleshooting-direct3d-9"></a><span data-ttu-id="4fea7-103">Problembehandlung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4fea7-103">Troubleshooting (Direct3D 9)</span></span>

<span data-ttu-id="4fea7-104">In diesem Thema werden allgemeine Kategorien von Problemen aufgeführt, die beim Schreiben von Direct3D-Anwendungen auftreten können, und wie Sie verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="4fea7-104">This topic lists common categories of problems that you might encounter when writing Direct3D applications, and how to prevent them.</span></span>

## <a name="device-creation"></a><span data-ttu-id="4fea7-105">Geräte Erstellung</span><span class="sxs-lookup"><span data-stu-id="4fea7-105">Device Creation</span></span>

<span data-ttu-id="4fea7-106">Wenn die Anwendung während der Geräte Erstellung ausfällt, überprüfen Sie, ob die folgenden allgemeinen Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="4fea7-106">If your application fails during device creation, check for the following common errors.</span></span>

-   <span data-ttu-id="4fea7-107">Stellen Sie sicher, dass Sie die Gerätefunktionen überprüfen, insbesondere die rendertiefe.</span><span class="sxs-lookup"><span data-stu-id="4fea7-107">Make sure you check the device capabilities, particularly the render depths.</span></span>
-   <span data-ttu-id="4fea7-108">Überprüfen Sie den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="4fea7-108">Examine the error code.</span></span> <span data-ttu-id="4fea7-109">D3DERR \_ outef videomemory ist immer möglich.</span><span class="sxs-lookup"><span data-stu-id="4fea7-109">D3DERR\_OUTOFVIDEOMEMORY is always possible.</span></span>
-   <span data-ttu-id="4fea7-110">Verwenden Sie die Debuggen DirectX-DLLs (Dynamic-Link Libraries), und überprüfen Sie die Ausgabemeldungen unter dem Debugger.</span><span class="sxs-lookup"><span data-stu-id="4fea7-110">Use the debug DirectX dynamic-link libraries (DLLs) and review output messages under the debugger.</span></span>

## <a name="using-lit-vertices"></a><span data-ttu-id="4fea7-111">Verwenden von beleuchteten Vertices</span><span class="sxs-lookup"><span data-stu-id="4fea7-111">Using Lit Vertices</span></span>

<span data-ttu-id="4fea7-112">Anwendungen, die beleuchtete Scheitel Punkte verwenden, sollten das Direct3D-Beleuchtungs Modul deaktivieren, indem Sie den D3DRS- \_ Beleuchtungs renderzustand auf **false** festlegen.</span><span class="sxs-lookup"><span data-stu-id="4fea7-112">Applications that use lit vertices should disable the Direct3D lighting engine by setting the D3DRS\_LIGHTING render state to **FALSE**.</span></span> <span data-ttu-id="4fea7-113">Standardmäßig legt das System bei aktivierter Beleuchtung die Farbe für alle Scheitel Punkte, die keinen normalen Vektor enthalten, auf 0 (schwarz) fest, auch wenn der Eingabe Scheitelpunkt einen Farbwert ungleich 0 (null) enthielt.</span><span class="sxs-lookup"><span data-stu-id="4fea7-113">By default, when lighting is enabled, the system sets the color for any vertex that doesn't contain a normal vector to 0 (black), even if the input vertex contained a nonzero color value.</span></span> <span data-ttu-id="4fea7-114">Da lit-Vertices nicht in ihrer Natur einen Scheitelpunkt normal enthalten, gehen alle an Direct3D über gebenden Farbinformationen beim Rendern verloren, wenn die Beleuchtungs-Engine aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4fea7-114">Because lit-vertices don't, by their nature, contain a vertex normal, any color information passed to Direct3D is lost during rendering if the lighting engine is enabled.</span></span>

<span data-ttu-id="4fea7-115">Natürlich ist die Scheitelpunkt Farbe für jede Anwendung wichtig, die ihre eigene Beleuchtung ausführt.</span><span class="sxs-lookup"><span data-stu-id="4fea7-115">Obviously, vertex color is important to any application that performs its own lighting.</span></span> <span data-ttu-id="4fea7-116">Stellen Sie sicher, dass Sie D3DRS- \_ Beleuchtung auf **false** festlegen, um zu verhindern, dass das System die Standardwerte erzwingt.</span><span class="sxs-lookup"><span data-stu-id="4fea7-116">To prevent the system from imposing the default values, make sure you set D3DRS\_LIGHTING to **FALSE**.</span></span>

<span data-ttu-id="4fea7-117">Wenn die Anwendung ausgeführt wird, aber nichts angezeigt wird, überprüfen Sie, ob die folgenden allgemeinen Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="4fea7-117">If your application runs but nothing is visible, check for the following common errors.</span></span>

-   <span data-ttu-id="4fea7-118">Stellen Sie sicher, dass die Dreiecke nicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fea7-118">Ensure that your triangles are not degenerate.</span></span>
-   <span data-ttu-id="4fea7-119">Stellen Sie sicher, dass Ihre Dreiecke nicht in der Hand ist.</span><span class="sxs-lookup"><span data-stu-id="4fea7-119">Ensure that your triangles are not being culled.</span></span>
-   <span data-ttu-id="4fea7-120">Stellen Sie sicher, dass ihre Transformationen intern konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="4fea7-120">Make sure that your transformations are internally consistent.</span></span>
-   <span data-ttu-id="4fea7-121">Überprüfen Sie die viewporteinstellungen, um sicherzustellen, dass Ihre Dreiecke angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4fea7-121">Check the viewport settings to be sure they allow your triangles to be seen.</span></span>

## <a name="debugging"></a><span data-ttu-id="4fea7-122">Debuggen</span><span class="sxs-lookup"><span data-stu-id="4fea7-122">Debugging</span></span>

<span data-ttu-id="4fea7-123">Das Debuggen einer Direct3D-Anwendung kann schwierig sein.</span><span class="sxs-lookup"><span data-stu-id="4fea7-123">Debugging a Direct3D application can be challenging.</span></span> <span data-ttu-id="4fea7-124">Testen Sie zusätzlich zum Überprüfen aller Rückgabewerte die folgenden Techniken: ein besonders wichtiger Ratgeber bei der Direct3D-Programmierung, der von sehr unterschiedlichen Hardware Implementierungen abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="4fea7-124">Try the following techniques, in addition to checking all the return values - a particularly important piece of advice in Direct3D programming, which is dependent on very different hardware implementations.</span></span>

-   <span data-ttu-id="4fea7-125">Wechseln Sie zu debugdlls.</span><span class="sxs-lookup"><span data-stu-id="4fea7-125">Switch to debug DLLs.</span></span>
-   <span data-ttu-id="4fea7-126">Erzwingen eines reinen Software Geräts und Ausschalten der Hardwarebeschleunigung, auch wenn diese verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4fea7-126">Force a software-only device, turning off hardware acceleration even when it is available.</span></span>
-   <span data-ttu-id="4fea7-127">Erzwingen von Oberflächen in den System Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4fea7-127">Force surfaces into system memory.</span></span>
-   <span data-ttu-id="4fea7-128">Erstellen Sie eine Option, die in einem Fenster ausgeführt werden soll, damit Sie einen integrierten Debugger verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4fea7-128">Create an option to run in a window, so that you can use an integrated debugger.</span></span>

<span data-ttu-id="4fea7-129">Mithilfe der zweiten und dritten Optionen in dieser Liste können Sie die Win16-Sperre vermeiden, die andernfalls dazu führen kann, dass der Debugger nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="4fea7-129">The second and third options in this list can help you avoid the Win16 lock which can otherwise cause your debugger to hang.</span></span>

<span data-ttu-id="4fea7-130">Fügen Sie auch die folgenden Einträge zu Win.ini hinzu.</span><span class="sxs-lookup"><span data-stu-id="4fea7-130">Also, try adding the following entries to Win.ini.</span></span>


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a><span data-ttu-id="4fea7-131">Borland-Floating-Point Initialisierung</span><span class="sxs-lookup"><span data-stu-id="4fea7-131">Borland Floating-Point Initialization</span></span>

<span data-ttu-id="4fea7-132">Compiler von Borland melden Gleit Komma Ausnahmen auf eine Weise, die mit Direct3D nicht kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="4fea7-132">Compilers from Borland report floating-point exceptions in a manner that is incompatible with Direct3D.</span></span> <span data-ttu-id="4fea7-133">Um dieses Problem zu beheben, schließen Sie einen \_ Matherr-Ausnahmehandler wie den folgenden ein:</span><span class="sxs-lookup"><span data-stu-id="4fea7-133">To solve this problem, include a \_matherr exception handler like the following:</span></span>


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a><span data-ttu-id="4fea7-134">Parameterüberprüfung</span><span class="sxs-lookup"><span data-stu-id="4fea7-134">Parameter Validation</span></span>

<span data-ttu-id="4fea7-135">Aus Leistungsgründen führt die Debugversion der Laufzeit "Direct3D immediate Mode" mehr Parameter Validierung aus als die Verkaufsversion, die gelegentlich überhaupt keine Überprüfung ausführt.</span><span class="sxs-lookup"><span data-stu-id="4fea7-135">For performance reasons, the debug version of the Direct3D Immediate Mode run time performs more parameter validation than the retail version, which sometimes performs no validation at all.</span></span> <span data-ttu-id="4fea7-136">Dadurch können Anwendungen ein stabiles Debuggen mit der langsameren Debug-Laufzeitkomponente durchführen, bevor Sie die schnellere Einzelhandelsversion für die Leistungsoptimierung und die endgültige Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fea7-136">This enables applications to perform robust debugging with the slower debug run-time component before using the faster retail version for performance tuning and final release.</span></span>

<span data-ttu-id="4fea7-137">Obwohl mehrere Direct3D-Methoden für den unmittelbaren Modus Grenzwerte für die zu akzeptierenden Werte vorsehen, werden diese Grenzwerte häufig nur von der Debugversion der Laufzeit des Direct3D unmittelbaren Modus geprüft und erzwungen.</span><span class="sxs-lookup"><span data-stu-id="4fea7-137">Although several Direct3D Immediate Mode methods impose limits on the values that they can accept, these limits are often only checked and enforced by the debug version of the Direct3D Immediate Mode run time.</span></span> <span data-ttu-id="4fea7-138">Anwendungen müssen diesen Grenzwerten entsprechen, oder es können unvorhersehbare und unerwünschte Ergebnisse auftreten, wenn Sie in der Verkaufsversion von Direct3D ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4fea7-138">Applications must conform to these limits, or unpredictable and undesirable results can occur when running on the retail version of Direct3D.</span></span> <span data-ttu-id="4fea7-139">Beispielsweise akzeptiert die [**IDirect3DDevice9::D rawprimiprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Methode einen Parameter (primitivecount), der die Anzahl der primitiven angibt, die von der Methode gerrentet werden.</span><span class="sxs-lookup"><span data-stu-id="4fea7-139">For example, the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method accepts a parameter (PrimitiveCount) that indicates the number of primitives that the method will render.</span></span> <span data-ttu-id="4fea7-140">Die-Methode kann nur Werte zwischen 0 und D3DMAXNUMPRIMITIVES akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="4fea7-140">The method can only accept values between 0 and D3DMAXNUMPRIMITIVES.</span></span> <span data-ttu-id="4fea7-141">Wenn Sie in der Debugversion von Direct3D mehr als D3DMAXNUMPRIMITIVES primitive übergeben, schlägt die Methode ordnungsgemäß fehl, druckt eine Fehlermeldung in das Fehlerprotokoll und gibt einen Fehlerwert an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="4fea7-141">In the debug version of Direct3D, if you pass more than D3DMAXNUMPRIMITIVES primitives, the method fails gracefully, printing an error message to the error log, and returning an error value to your application.</span></span> <span data-ttu-id="4fea7-142">Wenn die Anwendung dagegen denselben Fehler ausführt, wenn Sie mit der Verkaufsversion der Laufzeit ausgeführt wird, ist das Verhalten nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="4fea7-142">Conversely, if your application makes the same error when it is running with the retail version of the run time, behavior is undefined.</span></span> <span data-ttu-id="4fea7-143">Aus Leistungsgründen überprüft die-Methode die Parameter nicht, was zu unvorhersehbarem und vollständig veränderbarem Verhalten führt, wenn Sie nicht gültig sind.</span><span class="sxs-lookup"><span data-stu-id="4fea7-143">For performance reasons, the method does not validate the parameters, resulting in unpredictable and completely situational behavior when they are not valid.</span></span> <span data-ttu-id="4fea7-144">In einigen Fällen kann der-Befehl funktionieren, und in anderen Fällen kann er in Direct3D zu einem Speicherfehler führen.</span><span class="sxs-lookup"><span data-stu-id="4fea7-144">In some cases the call might work, and in other cases it might cause a memory fault in Direct3D.</span></span> <span data-ttu-id="4fea7-145">Wenn ein ungültiger-Rückruf konstant mit einer bestimmten Hardwarekonfiguration und DirectX-Version funktioniert, gibt es keine Garantie dafür, dass er weiterhin auf anderer Hardware oder mit späteren Versionen von DirectX funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4fea7-145">If an invalid call consistently works with a particular hardware configuration and DirectX version, there is no guarantee that it will continue to function on other hardware or with later releases of DirectX.</span></span>

<span data-ttu-id="4fea7-146">Wenn in Ihrer Anwendung bei der Ausführung mit der Direct3D-Lauf Zeit Datei für den Einzelhandel unerklärliche Fehler auftreten, testen Sie die Debugversion, und suchen Sie nach Fällen, in denen Ihre Anwendung ungültige Parameter übergibt.</span><span class="sxs-lookup"><span data-stu-id="4fea7-146">If your application encounters unexplained failures when running with the retail Direct3D run-time file, test against the debug version and look closely for cases where your application passes invalid parameters.</span></span> <span data-ttu-id="4fea7-147">Verwenden Sie das DirectX-System Steuerungs Applet, wechseln Sie ggf. zur Debug-Laufzeit, und aktivieren Sie die Option "unterbrechen bei D3DError".</span><span class="sxs-lookup"><span data-stu-id="4fea7-147">Use the DirectX control panel applet, switch to the debug runtime if necessary, and check the "Break on D3DError" option.</span></span> <span data-ttu-id="4fea7-148">Mit dieser Option wird die Laufzeit gezwungen, die Windows DebugBreak-Methode zu verwenden, um zu erzwingen, dass die Anwendung beendet wird, wenn ein Anwendungsfehler erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="4fea7-148">This option will force the runtime to use the Windows DebugBreak method in order to force the application to stop when an application bug is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fea7-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4fea7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fea7-150">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="4fea7-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
