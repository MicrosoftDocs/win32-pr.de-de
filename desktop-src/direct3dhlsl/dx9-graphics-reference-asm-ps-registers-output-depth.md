---
title: Ausgabe tiefen Register
description: Das Pixel-Shader-Ausgabe tiefen Register (otiefe) ist ein Schreib geschütztes skalarregister mit dem Bereich "\ 0.. 1 \", der einen neuen tiefen Wert für einen tiefen Test gegen den tiefen Schablone-Puffer zurückgibt.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311483"
---
# <a name="output-depth-register"></a>Ausgabe tiefen Register

Das Pixel-Shader-Ausgabe tiefen Register (otiefe) ist ein Schreib geschütztes skalarregister mit dem Bereich \[ 0.. 1 \] , das einen neuen tiefen Wert für einen tiefen Test mit dem tiefen Schablone-Puffer zurückgibt.

Syntax



| otiefe |
|--------|



 

Hierbei gilt:



| Name   | BESCHREIBUNG                                                       |
|--------|-------------------------------------------------------------------|
| otiefe | Neuer tiefen Wert für einen tiefen Test mit dem tiefen Schablone-Puffer |



 

Beachten Sie, dass das Schreiben in opaces den Verlust von Hardware spezifischen tiefen Puffer Optimierungsalgorithmen (z. b. hierarchische Z) verursacht, die die Tiefe Testleistung beschleunigen.

\|Beim Schreiben in den oausführlich ist das Replizieren der Quelle (. x. y \| . z \| . w) erforderlich. Explizite Schreib Masken sind nicht zulässig.

Beim Schreiben in das otiefe-Register wird der interpoliert-tiefen Wert ersetzt (und alle tiefen Bias/slopescale-renderstates werden ignoriert). Wenn kein tiefen Puffer erstellt oder an das Gerät angefügt wurde, wird der Schreibvorgang in die otiefe ignoriert.

Wenn Sie multisamplinggrad ausführen und in den oespace schreiben, wird der tiefen Wert für alle behandelten unter Beispiel Speicherorte repliziert, da der Pixelshader nur einmal pro Pixel ausgeführt wird. Der tiefen Test erfolgt immer noch pro Stichprobe, aber Sie haben keinen pro-Stichproben-tiefen Wert, der in den Vergleich mit dem Pixelshader erfolgt, wie Sie hätten, wenn Sie keine otiefen geschrieben hätten.

Wenn für eine Anwendung ein w-Puffer als tiefen Puffer festgelegt ist, muss Sie beim Schreiben in den oausführlich berücksichtigt werden. Möglicherweise muss Sie w-Range-Informationen an den Pixelshader senden und den w-Bereich berechnen, um die in den otiefe geschriebenen w-Werte zu skalieren.

### <a name="ps_2_0-and-ps_2_x-restrictions"></a>PS \_ 2 \_ 0-und PS \_ 2 \_ x-Einschränkungen

-   otiefen können nur mit der [MOV-PS-](mov---ps.md) Anweisung geschrieben werden und können nur einmal ausgeführt werden.
-   Beim Schreiben in den otiefe ist kein quellmodifizierer zulässig.
-   Beim Schreiben in den otiefe ist kein Anweisungs Modifizierer zulässig.
-   Kein Schreiben in den otiefe-Vorgang innerhalb eines Fluss Steuerungs Konstrukts oder bei Verwendung von Prädikat.

### <a name="ps_3_0-restrictions"></a>PS \_ 3 \_ 0-Einschränkungen

-   Bei PS \_ 3 \_ 0 können die Ausgabe Register "OC #" und "od" \# beliebig oft geschrieben werden. Die Ausgabe des Pixelshaders stammt aus dem Inhalt der Ausgabe Register am Ende der Shader-Ausführung. Wenn kein Schreibzugriff auf ein Ausgabe Register erfolgt, möglicherweise aufgrund der Fluss Steuerung, oder wenn der Shader ihn eben nicht geschrieben hat, wird auch das entsprechende Renderziel nicht aktualisiert. Wenn eine Teilmenge der Kanäle in einem Ausgabe Register geschrieben wird, werden nicht definierte Werte in die restlichen Kanäle geschrieben.
-   Wenn alle möglichen Pfade in das Register schreiben, können Sie in der Fluss Steuerung oder dem Prädikat in den ofuß schreiben.
-   Sie können keine Farbverlaufs Berechnungen (oder Vorgänge, die implizit Farbverlaufs Berechnungen wie [texld-PS \_ 2 \_ 0 und up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) in Fluss Steuerungs Anweisungen ausführen, deren Verzweigungs Bedingungen auf primitiver Basis variieren (d.h. dynamische Fluss Steuerungs Anweisungen). Das Anweisungs Prädikat gilt nicht als dynamische Fluss Steuerung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




