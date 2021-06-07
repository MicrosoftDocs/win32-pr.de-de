---
title: Präprozessordirektiven (HLSL)
description: Präprozessordirektiven wie \define und \ifdef werden in der Regel verwendet, um Quellprogramme einfach zu ändern und in verschiedenen Ausführungsumgebungen einfach zu kompilieren.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386829"
---
# <a name="preprocessor-directives-hlsl"></a>Präprozessordirektiven (HLSL)

Präprozessordirektiven wie [ \# define](dx-graphics-hlsl-appendix-pre-define.md) und [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)werden in der Regel verwendet, um Quellprogramme einfach zu ändern und in verschiedenen Ausführungsumgebungen einfach zu kompilieren. Anweisungen in der Quelldatei weisen den Präprozessor an, bestimmte Aktionen auszuführen. Beispielsweise kann der Präprozessor Token im Text ersetzen, den Inhalt von anderen Dateien in die Quelldatei einfügen oder die Kompilierung eines Teils der Datei unterdrücken, indem er Textabschnitte entfernt. Präprozessorzeilen werden vor der Makroerweiterung erkannt und ausgeführt. Wenn also die Erweiterung eines Makros aussieht wie ein Präprozessorbefehl, wird dieser Befehl nicht vom Präprozessor erkannt.

Präprozessoranweisungen verwenden den gleichen Zeichensatz wie Quelldateianweisungen, mit der Ausnahme, dass Escapesequenzen nicht unterstützt werden. Der Zeichensatz, der in Präprozessoranweisungen verwendet wird, ist mit dem Ausführungszeichensatz identisch. Der Präprozessor erkennt auch negative Zeichenwerte.

Der HLSL-Präprozessor erkennt die folgenden Anweisungen:

-   [\#Definieren](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#Fehler](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#Wenn](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#Ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#include](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#line](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#Pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

Das Nummernzeichen ( ) muss das erste Nicht-Leerzeichen in der Zeile sein, die die -Direktive enthält. Leerzeichen können zwischen dem Nummernzeichen und dem ersten Buchstaben der -Direktive \# angezeigt werden. Manche Anweisungen enthalten Argumente oder Werte. Jedem Text, der auf eine -Anweisung folgt (mit Ausnahme eines Arguments oder Werts, das Teil der -Direktive ist), muss das einzeilenbasierte Kommentartrennzeichen (/) voranstehen oder in Kommentartrennzeichen (/ /) eingeschlossen \* \* werden. Zeilen, die Präprozessordirektiven enthalten, können fortgesetzt werden, indem dem Zeilenendemarker unmittelbar ein zurücker schräger Schrägstrich ( ) vorangegangen \\ wird.

Präprozessoranweisungen können an beliebiger Stelle in einer Quelldatei auftreten, aber sie gelten nur für den Rest der Quelldatei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anhang (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




