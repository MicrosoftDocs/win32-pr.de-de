---
description: Ein Shader, der aufgerufen wird, wenn Ray-Schnittmengen nicht deckend sind.
ms.assetid: ''
title: Any Hit-Shader
ms.date: 05/31/2018
ms.topic: reference
ms.localizationpriority: low
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: aad2f8b94f6ea53d500d285cac3555f5ff8b95f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346634"
---
# <a name="any-hit-shader"></a><span data-ttu-id="70e35-103">Any Hit-Shader</span><span class="sxs-lookup"><span data-stu-id="70e35-103">Any Hit Shader</span></span>

<span data-ttu-id="70e35-104">Ein Shader, der aufgerufen wird, wenn Ray-Schnittmengen nicht deckend sind.</span><span class="sxs-lookup"><span data-stu-id="70e35-104">A shader that is invoked when ray intersections are not opaque.</span></span> 

<span data-ttu-id="70e35-105">Alle Treffer-Shader müssen einen Nutz Last Parameter, gefolgt von einem Attribute-Parameter, deklarieren.</span><span class="sxs-lookup"><span data-stu-id="70e35-105">Any hit shaders must declare a payload parameter followed by an attributes parameter.</span></span> <span data-ttu-id="70e35-106">Jeder dieser Parameter muss ein benutzerdefinierter Strukturtyp sein, der mit den Typen übereinstimmt, die für [**traceray**](traceray-function.md) bzw. [**reporthit**](reporthit-function.md) verwendet werden, oder die [**Struktur der Schnittstellen Attribute**](intersection-attributes.md) bei Verwendung einer Schnittmenge mit festem Funktions Dreieck.</span><span class="sxs-lookup"><span data-stu-id="70e35-106">Each of these parameters must be a user-defined structure type matching types used for [**TraceRay**](traceray-function.md) and [**ReportHit**](reporthit-function.md) respectively, or the [**Intersection Attributes Structure**](intersection-attributes.md) when fixed function triangle intersection is used.</span></span>

<span data-ttu-id="70e35-107">Alle Treffer-Shader können die folgenden Arten von Vorgängen ausführen:</span><span class="sxs-lookup"><span data-stu-id="70e35-107">Any hit shaders may perform the following kinds of operations:</span></span>

*   <span data-ttu-id="70e35-108">Lesen und Ändern der Ray-Nutzlast: (INOUT payload_t raypayload)</span><span class="sxs-lookup"><span data-stu-id="70e35-108">Read and modify the ray payload: (inout payload_t rayPayload)</span></span>
*   <span data-ttu-id="70e35-109">Lesen der Schnittstellen Attribute: (in attr_t Attributen)</span><span class="sxs-lookup"><span data-stu-id="70e35-109">Read the intersection attributes: (in attr_t attributes)</span></span>
*   <span data-ttu-id="70e35-110">Aufrufen von " [**Accept thitandendsearch**](accepthitandendsearch-function.md)", das den aktuellen Treffer annimmt, den [beliebigen Treffer-Shader](any-hit-shader.md)beendet, den [Schnittstellen-Shader](intersection-shader.md) beendet, wenn ein solcher vorhanden ist, und führt den [nächstgelegenen Treffer-Shader](closest-hit-shader.md) am nächstgelegenen Treffer aus, wenn er aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="70e35-110">Call [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), which accepts the current hit, ends the [any hit shader](any-hit-shader.md), ends the [intersection shader](intersection-shader.md) if one is present, and executes the [closest hit shader](closest-hit-shader.md) on the closest hit so far if it is active.</span></span>
*   <span data-ttu-id="70e35-111">" [**Ignorehit**](ignorehit-function.md)" aufrufen, der den beliebigen Treffer-Shader beendet und das System anweist, die Suche nach Treffern fortzusetzen, einschließlich der Rückgabe der Steuerung an einen Schnittstellen-Shader, wenn er gerade ausgeführt wird und "false" von der [**reporthit**](reporthit-function.md)\*-Website aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="70e35-111">Call [**IgnoreHit**](ignorehit-function.md), which ends the any hit shader and tells the system to continue searching for hits, including returning control to an intersection shader, if it is currently executing, returning false from the [**ReportHit**](reporthit-function.md)\* call site.</span></span> 
*   <span data-ttu-id="70e35-112">Geben Sie zurück, ohne eine dieser systeminternen Funktionen aufzurufen, die den aktuellen Treffer akzeptiert und das System anweist, weiterhin nach Treffern zu suchen, einschließlich der Rückgabe der Steuerung an den Schnittstellen-Shader, falls vorhanden. gibt true auf der [**reporthit**](reporthit-function.md) -Aufruf Site zurück, um anzugeben, dass der Treffer akzeptiert wurde.</span><span class="sxs-lookup"><span data-stu-id="70e35-112">Return without calling either of these intrinsics, which accepts the current hit and tells the system to continue searching for hits, including returning control to the intersection shader if there is one, returning true at the [**ReportHit**](reporthit-function.md) call site to indicate that the hit was accepted.</span></span>

<span data-ttu-id="70e35-113">Selbst wenn ein beliebiger Treffer-Shader-Aufruf durch [**ignorehit**](ignorehit-function.md) oder [**Accept thitandendsearch**](accepthitandendsearch-function.md)beendet wird, müssen alle Änderungen, die an der Strahl Nutzlast bisher vorgenommen wurden, trotzdem beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="70e35-113">Even if an any hit shader invocation is ended by [**IgnoreHit**](ignorehit-function.md) or [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md), any modifications made to the ray payload so far must still be retained.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="70e35-114">Shader Type-Attribut</span><span class="sxs-lookup"><span data-stu-id="70e35-114">Shader Type attribute</span></span>

```
[shader("anyhit")]
```

## <a name="example"></a><span data-ttu-id="70e35-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="70e35-115">Example</span></span>

```
[shader("anyhit")]
void anyhit_main( inout MyPayload payload, in MyAttributes attr )
{
    float3 hitLocation = ObjectRayOrigin() + ObjectRayDirection() * RayTCurrent();
    float alpha = computeAlpha(hitLocation, attr, ...);

    // Processing shadow and only care if a hit is registered?
    if (TerminateShadowRay(alpha))
        AcceptHitAndEndSearch(); // aborts function

    // Save alpha contribution and ignoring hit?
    if (SaveAndIgnore(payload, RayTCurrent(), alpha, attr, ...))
        IgnoreHit(); // aborts function

    // do something else
    // return to accept and update closest hit
}
```
