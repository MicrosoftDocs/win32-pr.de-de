---
title: Ausgabetiefenregister
description: Das Pixel-Shader-Ausgabetiefenregister (oDepth) ist ein Skalarregister mit Schreibzugriff mit dem Bereich \0..1\, das einen neuen Tiefenwert für einen Tiefentest für den Tiefenschablonenpuffer zurückgibt.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 041ffccb3301831c91554ef3cda835d3f2e79204730e838b25f26660e76d9a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119724"
---
# <a name="output-depth-register"></a>Ausgabetiefenregister

Das Pixel-Shader-Ausgabetiefenregister (oDepth) ist ein Skalarregister mit Schreibzugriff mit dem Bereich \[ 0..1, das einen neuen Tiefenwert für einen Tiefentest für den Tiefenschablonenpuffer \] zurückgibt.

Syntax



| oDepth |
|--------|



 

Hierbei gilt:



| Name   | Beschreibung                                                       |
|--------|-------------------------------------------------------------------|
| oDepth | Neuer Tiefenwert für einen Tiefentest für den Tiefen-Schablonenpuffer |



 

Es ist wichtig zu beachten, dass das Schreiben in oDepth den Verlust von hardwarespezifischen Algorithmen zur Tiefenpufferoptimierung (d. h. hierarchische z) verursacht, die die Leistung von Tiefentests beschleunigen.

Beim Schreiben in oDepth ist eine Replikation der Quell-Swizzle (.x \| \| .y .z \| .w) erforderlich. Explizite Schreibmasken sind nicht zulässig.

Das Schreiben in das oDepth-Register ersetzt den interpolierten Tiefenwert (und ignoriert alle Renderstate für Tiefen- bzw. Steigungsskala). Wenn kein Tiefenpuffer erstellt oder an das Gerät angefügt wurde, wird der Schreibzugriff auf oDepth ignoriert.

Wenn Sie multisampling und in oDepth schreiben, da der Pixel-Shader nur einmal pro Pixel ausgeführt wird, wird Ihr Tiefenwert für alle abgedeckten Unterbeispielpositionen repliziert. Der Tiefentest erfolgt weiterhin pro Stichprobe, aber Sie haben keinen Tiefenwert pro Stichproben, der vom Pixel-Shader in den Vergleich einfädt, wie sie es wäre, wenn Sie oDepth nicht geschrieben hätten.

Wenn eine Anwendung einen W-Puffer als Tiefenpuffer festgelegt hat, muss sie dies beim Schreiben in oDepth berücksichtigen. Möglicherweise müssen w-Bereichsinformationen an den Pixel-Shader gesendet und der w-Bereich berechnet werden, um die w-Werte zu skalieren, die auf oDepth geschrieben wurden.

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>ps \_ 2 \_ 0 und ps \_ 2 \_ x Einschränkungen

-   oDepth kann nur mit der [mov - ps-Anweisung](mov---ps.md) geschrieben werden und kann nur einmal durchgeführt werden.
-   Beim Schreiben in oDepth ist kein Quellmodifizierer zulässig.
-   Beim Schreiben in oDepth ist kein Anweisungsmodifizierer zulässig.
-   Kein Schreiben in oDepth innerhalb eines Flusssteuerungskonstrukts oder bei Verwendung von Prädication.

### <a name="ps_3_0-restrictions"></a>PS \_ 3 \_ 0 Einschränkungen

-   Für ps 3 0 können die Ausgaberegister oC# und oD so oft \_ \_ wie möglich geschrieben \# werden. Die Ausgabe des Pixelschattens stammt aus dem Inhalt der Ausgaberegister am Ende der Shaderausführung. Wenn kein Schreibzugriff in ein Ausgaberegister geschieht, z. B. aufgrund der Flusssteuerung oder wenn der Shader es einfach nicht geschrieben hat, wird auch das entsprechende Renderziel nicht aktualisiert. Wenn eine Teilmenge der Kanäle in einem Ausgaberegister geschrieben wird, werden nicht definierte Werte in die verbleibenden Kanäle geschrieben.
-   Sie können in oDepth innerhalb der Flusssteuerung oder Prädication schreiben, solange alle möglichen Pfade schließlich in das Register geschrieben werden.
-   Sie dürfen keine Farbverlaufsberechnungen (oder Vorgänge, die implizit Farbverlaufsberechnungen aufrufen, z. B. [texld – ps \_ 2 \_ 0](texld---ps-2-0.md)und up , [texldb – ps](texldb---ps.md), [texldp – ps](texldp---ps.md)) innerhalb von Flusssteuerungsanweisungen ausführen, deren Verzweigungsbedingungen je nach Primitiven variieren (d.h. dynamische Flusssteuerungsanweisungen). Anweisungsvordication wird nicht als dynamische Flusssteuerung betrachtet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




