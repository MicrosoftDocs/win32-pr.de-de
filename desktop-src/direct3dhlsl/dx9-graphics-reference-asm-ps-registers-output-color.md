---
title: Ausgabefarbregister
description: Die Pixel-Shader-Farbausgaberegister (oC\) sind schreibgeschützte Register, die Ergebnisse an mehrere Renderziele ausgeben.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 038446bb7d588222e04028727a447b6a47c941ab6a18a3ba4216f46e93440961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119704"
---
# <a name="output-color-register"></a>Ausgabefarbregister

Die Pixel-Shader-Farbausgaberegister (oC#) sind schreibgeschützte Register, die Ergebnisse an mehrere Renderziele ausgeben.

Syntax



| Oc # |
|------|



 

Hierbei gilt:



| Name | Beschreibung       |
|------|-------------------|
| oC0  | Renderziel \# 0 |
| oC1  | Renderziel \# 1 |
| oC2  | Renderziel \# 2 |
| oC3  | Renderziel \# 3 |



 

## <a name="remarks"></a>Hinweise

-   Wenn oCn geschrieben wird, aber kein entsprechendes Renderziel vorhanden ist, wird dieser Schreibvorgang in oCn ignoriert.
-   Die Renderzustände D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 und D3DRS \_ COLORWRITEENABLE3 bestimmen, welche oCn-Komponenten letztendlich in das Renderziel geschrieben werden (nach blend, falls zutreffend). Wenn der Shader einige, aber nicht alle komponenten schreibt, die von den D3DRS \_ COLORWRITEENABLE-Renderzuständen \* für ein bestimmtes oCn-Register definiert werden, erzeugen die nicht geschriebenen Kanäle im entsprechenden Renderziel nicht definierte Werte. Wenn keine der Komponenten eines oCn geschrieben wird, darf das entsprechende Renderziel nicht aktualisiert werden (wie oben erwähnt), sodass die D3DRS \_ COLORWRITEENABLE-Renderzustände \* nicht gelten.

### <a name="shader-model-2-restrictions"></a>Shadermodell 2 – Einschränkungen

-   oCn kann nur mit der Anweisung [mov - ps](mov---ps.md) geschrieben werden.
-   oC0 muss immer im Shader geschrieben werden.
-   Beim Schreiben in einen beliebigen oCn ist kein Quellwizzle (mit Ausnahme von .xyzw = Standard-Swizzle) oder Quellmodifizierer zulässig.
-   Beim Schreiben in oCn ist keine Zielschreibmaske (mit Ausnahme von .xyzw = Standardmaske) oder Anweisungsmodifizierer zulässig.
-   Wenn oCn geschrieben wird, muss auch oC0 - oCn-1 geschrieben werden. Um beispielsweise in oC2 zu schreiben, müssen Sie auch in oC0 und oC1 schreiben.
-   Es ist höchstens ein Schreibvorgang in beliebige oC#-Dateien pro Shader zulässig.
-   Für ps \_ 2 \_ x und ps \_ 3 \_ 0 können Sie nicht in oC#- und oD-Register \# innerhalb der dynamischen Flusssteuerung oder Prädikation schreiben (Schreibvorgänge in oC# innerhalb der statischen Flusssteuerung sind in Ordnung).

### <a name="shader-model-3-restrictions"></a>Einschränkungen für Shadermodell 3

-   Für ps \_ 3 \_ 0 können ausgaberegister oC# und oD \# beliebig oft geschrieben werden. Die Ausgabe des Pixelshader stammt aus dem Inhalt der Ausgaberegister am Ende der Shaderausführung. Wenn kein Schreibvorgang in ein Ausgaberegister erfolgt, z. B. aufgrund der Flusssteuerung, oder wenn der Shader es einfach nicht geschrieben hat, wird auch das entsprechende Renderziel nicht aktualisiert. Wenn eine Teilmenge der Kanäle in einem Ausgaberegister geschrieben wird, werden nicht definierte Werte in die verbleibenden Kanäle geschrieben.
-   Für ps \_ 3 \_ 0 können die oC#-Register mit beliebigen Schreibmasken geschrieben werden.
-   Für ps \_ 2 \_ x und ps \_ 3 \_ 0 können Sie nicht in oC#- und oD-Register \# innerhalb der dynamischen Flusssteuerung oder Prädikation schreiben (Schreibvorgänge in oC# innerhalb der statischen Flusssteuerung sind in Ordnung).
-   Sie dürfen keine Farbverlaufsberechnungen (oder Vorgänge, die implizit Farbverlaufsberechnungen wie [texld - ps \_ 2 \_ 0 und up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) innerhalb von Flusssteuerungsanweisungen aufrufen, deren Verzweigungsbedingungen pro Primitive variieren (d. h. dynamische Ablaufsteuerungsanweisungen). Anweisungsprädikation wird nicht als dynamische Flusssteuerung betrachtet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Mehrere Renderziele (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 