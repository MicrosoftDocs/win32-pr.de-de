---
description: Ein Shader, der aufgerufen wird, wenn Die Schnittpunkte des Strahls nicht deckend sind.
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
ms.openlocfilehash: 127c12c6d87ca76ddac5b5c5e013414c96651e56ee762156e7435811ff275a05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124385"
---
# <a name="any-hit-shader"></a>Any Hit-Shader

Ein Shader, der aufgerufen wird, wenn Die Schnittpunkte des Strahls nicht deckend sind. 

Alle Treffer-Shader müssen einen Nutzlastparameter gefolgt von einem attributes-Parameter deklarieren. Jeder dieser Parameter muss ein benutzerdefinierter Strukturtyp sein, der mit Typen abgleicht, die für [**TraceRay**](traceray-function.md) bzw. [**ReportHit**](reporthit-function.md) verwendet werden, oder die [**Schnittmengenattribute-Struktur,**](intersection-attributes.md) wenn eine feste Funktionsdreieck-Schnittmenge verwendet wird.

Alle Treffer-Shader können die folgenden Arten von Vorgängen ausführen:

*   Lesen und Ändern der Raynutzlast: (inout payload_t rayPayload)
*   Lesen der Schnittmengenattribute: (in attr_t Attributen)
*   Rufen Sie [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md)auf, das den aktuellen Treffer akzeptiert, den beliebigen Treffer-Shader beendet, den Schnittpunkt-Shader beendet, sofern vorhanden, und führt den nächstgelegenen Treffer-Shader für den nächstgelegenen Treffer aus, sofern er aktiv ist. [](any-hit-shader.md) [](intersection-shader.md) [](closest-hit-shader.md)
*   Rufen [**Sie IgnoreHit**](ignorehit-function.md)auf, wodurch der beliebige Treffer-Shader beendet wird, und weist das System an, weiterhin nach Treffern zu suchen, einschließlich der Rückgabe der Steuerung an einen Schnittpunkt-Shader, sofern er gerade ausgeführt wird, und gibt false von der [**ReportHit**](reporthit-function.md)*-Aufrufsite zurück. 
*   Kehren Sie zurück, ohne eine dieser systeminternen Systeminternen zu aufrufen. Diese akzeptiert den aktuellen Treffer und weist das System an, weiterhin nach Treffern zu suchen, einschließlich der Rückgabe der Steuerung an den Schnittpunkt-Shader, sofern eine solche ist, und die Rückgabe von TRUE an der [**ReportHit-Aufrufsite,**](reporthit-function.md) um anzugeben, dass der Treffer akzeptiert wurde.

Auch wenn ein Treffer-Shaderaufruf durch [**IgnoreHit**](ignorehit-function.md) oder [**AcceptHitAndEndSearch**](accepthitandendsearch-function.md)beendet wird, müssen alle änderungen, die bisher an der Raynutzlast vorgenommen wurden, weiterhin beibehalten werden.

## <a name="shader-type-attribute"></a>Shadertypattribut

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
