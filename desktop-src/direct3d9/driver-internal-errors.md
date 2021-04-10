---
description: In Direct3D 9 ermöglicht Direct3D dem Treiber das Zurückgeben von Fehlercodes, wie z \_ . b. "E outo fmemory", "D3DERR \_ outo fvideomemory" und "D3DERR \_ unsupportedcolorarg", damit eine Anwendung darauf reagieren kann.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Interne Treiber Fehler (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124760"
---
# <a name="driver-internal-errors-direct3d-9"></a><span data-ttu-id="e5f97-103">Interne Treiber Fehler (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e5f97-103">Driver Internal Errors (Direct3D 9)</span></span>

<span data-ttu-id="e5f97-104">In Direct3D 9 ermöglicht Direct3D dem Treiber das Zurückgeben von Fehlercodes, wie z \_ . b. "E outo fmemory", "D3DERR \_ outo fvideomemory" und "D3DERR \_ unsupportedcolorarg", damit eine Anwendung darauf reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="e5f97-104">In Direct3D 9, Direct3D will allow the driver to return error codes such as E\_OUTOFMEMORY, D3DERR\_OUTOFVIDEOMEMORY, and D3DERR\_UNSUPPORTEDCOLORARG so that an application would be able to respond to them.</span></span> <span data-ttu-id="e5f97-105">Manchmal werden jedoch die API-Aufrufe, die diese Rückgabe Typen generiert haben, in einen Befehls Puffer geladen und in einem Batch zusammengefasst, um Sie an die GPU zu senden (Weitere Informationen finden Sie unter [Steuern von Lauf Zeit-und Treiber Optimierungen](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="e5f97-105">However, sometimes the API calls that generated these return types get loaded into a command buffer and are batched up to be sent to the GPU (see [Controlling Runtime and Driver Optimizations](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="e5f97-106">In diesem Fall können die Fehler nicht an die Anwendung weitergeleitet werden, wenn eine Aktion ausgeführt werden muss, sodass der Fehlercode von der Laufzeit genutzt wird und für das Geräte Objekt, auf dem dies aufgetreten ist, ein Hinweis ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e5f97-106">In this case, the errors cannot be relayed to the application when action needs to be taken, so the error code is consumed by the runtime and a note is made on the device object that this happened.</span></span> <span data-ttu-id="e5f97-107">Wenn die Anwendung zu einem späteren Zeitpunkt " [**:P IDirect3DDevice9**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)" aufruft, wird " **IDirect3DDevice9::P Resent** " D3DERR \_ driverinternalerror zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5f97-107">Later when the application invokes [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::Present** will return D3DERR\_DRIVERINTERNALERROR.</span></span> <span data-ttu-id="e5f97-108">Aus diesem Grund ist der beste Ansatz für eine Anwendung beim Empfang eines D3DERR \_ driverinternalerror von **IDirect3DDevice9::P** erneutes Senden besteht darin, das Gerät zu zerstören und neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e5f97-108">This is why the best approach for an application to take when receiving a D3DERR\_DRIVERINTERNALERROR from **IDirect3DDevice9::Present** is to destroy and recreate the device.</span></span>

<span data-ttu-id="e5f97-109">Wenn Sie versuchen möchten, das Debugging weiter zu versuchen, finden Sie hier einige Vorschläge, um herauszufinden, welcher API-Befehl den Fehler erzeugt:</span><span class="sxs-lookup"><span data-stu-id="e5f97-109">If you want to try to debug further, here are a couple of suggestions for trying to figure out which API call is generating the error:</span></span>

-   <span data-ttu-id="e5f97-110">Da die Liste der möglichen Rückgabewerte nicht erfüllt ist, können Sie versuchen, den Fehler zu ermitteln, indem Sie die einzelnen API-Aufrufe wie folgt umschließen:</span><span class="sxs-lookup"><span data-stu-id="e5f97-110">Because the list of possible return values is not complete, you can try to find which call is failing by surrounding each API call like this:</span></span>

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    <span data-ttu-id="e5f97-111">Der ausgabedebugstream sollte dann den-Befehl anzeigen, der das Problem verursacht.</span><span class="sxs-lookup"><span data-stu-id="e5f97-111">The output debug stream should then show the call that is causing the problem.</span></span>

-   <span data-ttu-id="e5f97-112">Versuchen Sie zusätzlich zu Debuggingzwecken, [**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) direkt vor jedem [**IDirect3DDevice9::D rawprimiprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) zu aufrufen, um zu ermitteln, ob ein zusätzliches Problem mit dem Gerätetreiber vorliegt (nicht unterstützter Vorgang, nicht verwendbare Kombination von Textur Formaten usw.).</span><span class="sxs-lookup"><span data-stu-id="e5f97-112">Additionally, for debugging purposes, try calling [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediately before each [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to see if there is an additional problem with the device driver (unsupported operation, unusable combination of texture formats, etc).</span></span>

    > [!Note]  
    > <span data-ttu-id="e5f97-113">[**IDirect3DDevice9:: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) sollte aufgrund der Menge an Validierungsarbeiten, die der Treiber ausführen muss, um eine Antwort zurückzugeben, sorgfältig und sparsam verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e5f97-113">[**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) should be used carefully and sparingly because of the amount of validation work the driver needs to perform to return an answer.</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="e5f97-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5f97-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5f97-115">Programmiertipps</span><span class="sxs-lookup"><span data-stu-id="e5f97-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
