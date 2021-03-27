---
title: Ausgabe Farb Register
description: Die Pixel-Shader-Farbausgabe Register (OC \) sind schreibgeschützt, die Ergebnisse an mehrere Renderziele ausgeben.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390812"
---
# <a name="output-color-register"></a>Ausgabe Farb Register

Die Pixel-Shader-Farbausgabe Register (OC #) sind schreibgeschützte Registrierungen, die Ergebnisse an mehrere Renderziele ausgeben.

Syntax



| d # |
|------|



 

Hierbei gilt:



| Name | BESCHREIBUNG       |
|------|-------------------|
| oC0  | Renderziel \# 0 |
| oC1  | Renderziel \# 1 |
| oC2  | Renderziel \# 2 |
| oC3  | Renderziel \# 3 |



 

## <a name="remarks"></a>Bemerkungen

-   Wenn OCN geschrieben ist, aber kein entsprechendes Renderziel vorhanden ist, wird dieser Schreibvorgang in OCN ignoriert.
-   Die renderzustände D3DRS \_ colorschreiteenable, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 und D3DRS \_ COLORWRITEENABLE3 bestimmen, welche Komponenten von OCN letztendlich in das Renderziel geschrieben werden (sofern zutreffend). Wenn der Shader einige, jedoch nicht alle Komponenten schreibt, die von den D3DRS \_ ColorWriteEnable- \* renderzuständen für ein bestimmtes OCN-Register definiert werden, erzeugen die nicht geschriebenen Kanäle nicht definierte Werte im entsprechenden Renderziel. Wenn keine der Komponenten eines OCN geschrieben wird, darf das entsprechende Renderziel überhaupt nicht aktualisiert werden (wie oben beschrieben), sodass die \_ renderzustände von D3DRS colorschreiteenable \* nicht zutreffen.

### <a name="shader-model-2-restrictions"></a>Einschränkungen für Shader Model 2

-   OCN kann nur mit der [MOV-PS-](mov---ps.md) Anweisung geschrieben werden.
-   oC0 muss immer im Shader geschrieben werden.
-   Beim Schreiben in einen beliebigen OCN ist kein quellswidwert (mit Ausnahme von. xyzw = default Swizzle) oder der quellmodifizierer zulässig.
-   Beim Schreiben in einen beliebigen OCN ist keine Ziel Schreib Maske (mit Ausnahme von. xyzw = default Mask) oder ein Anweisungs Modifizierer zulässig.
-   Wenn OCN geschrieben ist, muss auch oC0-OCN-1 geschrieben werden. Wenn Sie z. b. in oC2 schreiben möchten, müssen Sie auch in oC0 und oC1 schreiben.
-   Höchstens ein Schreibvorgang in einen oC # pro Shader ist zulässig.
-   Für PS \_ 2 \_ x und PS \_ 3 \_ 0 können Sie nicht in oC #-und od- \# Register in der dynamischen Fluss Steuerung oder im Prädikat schreiben (Schreibvorgänge in OC # innerhalb der statischen Fluss Steuerung ist in Ordnung).

### <a name="shader-model-3-restrictions"></a>Shader Model 3-Einschränkungen

-   Bei PS \_ 3 \_ 0 können die Ausgabe Register "OC #" und "od" \# beliebig oft geschrieben werden. Die Ausgabe des Pixelshaders stammt aus dem Inhalt der Ausgabe Register am Ende der Shader-Ausführung. Wenn kein Schreibzugriff auf ein Ausgabe Register erfolgt, möglicherweise aufgrund der Fluss Steuerung, oder wenn der Shader ihn eben nicht geschrieben hat, wird auch das zugehörige renderTarget-Element nicht aktualisiert. Wenn eine Teilmenge der Kanäle in einem Ausgabe Register geschrieben wird, werden nicht definierte Werte in die restlichen Kanäle geschrieben.
-   Für PS \_ 3 \_ 0 können die OC #-Register mit allen Schreib Vorwörtern geschrieben werden.
-   Für PS \_ 2 \_ x und PS \_ 3 \_ 0 können Sie nicht in oC #-und od- \# Register in der dynamischen Fluss Steuerung oder im Prädikat schreiben (Schreibvorgänge in OC # innerhalb der statischen Fluss Steuerung ist in Ordnung).
-   Sie können keine Farbverlaufs Berechnungen (oder Vorgänge, die implizit Farbverlaufs Berechnungen wie [texld-PS \_ 2 \_ 0 und up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) in Fluss Steuerungs Anweisungen ausführen, deren Verzweigungs Bedingungen auf primitiver Basis variieren (d.h. dynamische Fluss Steuerungs Anweisungen). Das Anweisungs Prädikat gilt nicht als dynamische Fluss Steuerung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Mehrere Renderziele (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 