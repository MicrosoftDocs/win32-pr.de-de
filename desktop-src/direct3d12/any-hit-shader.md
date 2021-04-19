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
# <a name="any-hit-shader"></a>Any Hit-Shader

Ein Shader, der aufgerufen wird, wenn Ray-Schnittmengen nicht deckend sind. 

Alle Treffer-Shader müssen einen Nutz Last Parameter, gefolgt von einem Attribute-Parameter, deklarieren. Jeder dieser Parameter muss ein benutzerdefinierter Strukturtyp sein, der mit den Typen übereinstimmt, die für [**traceray**](traceray-function.md) bzw. [**reporthit**](reporthit-function.md) verwendet werden, oder die [**Struktur der Schnittstellen Attribute**](intersection-attributes.md) bei Verwendung einer Schnittmenge mit festem Funktions Dreieck.

Alle Treffer-Shader können die folgenden Arten von Vorgängen ausführen:

*   Lesen und Ändern der Ray-Nutzlast: (INOUT payload_t raypayload)
*   Lesen der Schnittstellen Attribute: (in attr_t Attributen)
*   Aufrufen von " [**Accept thitandendsearch**](accepthitandendsearch-function.md)", das den aktuellen Treffer annimmt, den [beliebigen Treffer-Shader](any-hit-shader.md)beendet, den [Schnittstellen-Shader](intersection-shader.md) beendet, wenn ein solcher vorhanden ist, und führt den [nächstgelegenen Treffer-Shader](closest-hit-shader.md) am nächstgelegenen Treffer aus, wenn er aktiv ist.
*   " [**Ignorehit**](ignorehit-function.md)" aufrufen, der den beliebigen Treffer-Shader beendet und das System anweist, die Suche nach Treffern fortzusetzen, einschließlich der Rückgabe der Steuerung an einen Schnittstellen-Shader, wenn er gerade ausgeführt wird und "false" von der [**reporthit**](reporthit-function.md)*-Website aufgerufen wird. 
*   Geben Sie zurück, ohne eine dieser systeminternen Funktionen aufzurufen, die den aktuellen Treffer akzeptiert und das System anweist, weiterhin nach Treffern zu suchen, einschließlich der Rückgabe der Steuerung an den Schnittstellen-Shader, falls vorhanden. gibt true auf der [**reporthit**](reporthit-function.md) -Aufruf Site zurück, um anzugeben, dass der Treffer akzeptiert wurde.

Selbst wenn ein beliebiger Treffer-Shader-Aufruf durch [**ignorehit**](ignorehit-function.md) oder [**Accept thitandendsearch**](accepthitandendsearch-function.md)beendet wird, müssen alle Änderungen, die an der Strahl Nutzlast bisher vorgenommen wurden, trotzdem beibehalten werden.

## <a name="shader-type-attribute"></a>Shader Type-Attribut

```
[shader("anyhit")]
```

## <a name="example"></a>Beispiel

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
