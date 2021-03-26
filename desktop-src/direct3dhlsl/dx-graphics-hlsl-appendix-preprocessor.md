---
title: Präprozessordirektiven (HLSL)
description: Präprozessordirektiven, wie z. b. \ define und \ ifdef, werden normalerweise verwendet, um das ändern und Kompilieren von Quell Programmen in verschiedenen Ausführungs Umgebungen zu vereinfachen.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739232"
---
# <a name="preprocessor-directives-hlsl"></a>Präprozessordirektiven (HLSL)

Präprozessordirektiven, wie z. b. [ \# define](dx-graphics-hlsl-appendix-pre-define.md) und [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), werden normalerweise verwendet, um das ändern und Kompilieren von Quell Programmen in verschiedenen Ausführungs Umgebungen zu vereinfachen. Anweisungen in der Quelldatei weisen den Präprozessor an, bestimmte Aktionen auszuführen. Beispielsweise kann der Präprozessor Token im Text ersetzen, den Inhalt von anderen Dateien in die Quelldatei einfügen oder die Kompilierung eines Teils der Datei unterdrücken, indem er Textabschnitte entfernt. Präprozessorzeilen werden vor der Makroerweiterung erkannt und ausgeführt. Wenn also die Erweiterung eines Makros aussieht wie ein Präprozessorbefehl, wird dieser Befehl nicht vom Präprozessor erkannt.

Präprozessoranweisungen verwenden den gleichen Zeichensatz wie Quelldateianweisungen, mit der Ausnahme, dass Escapesequenzen nicht unterstützt werden. Der Zeichensatz, der in Präprozessoranweisungen verwendet wird, ist mit dem Ausführungszeichensatz identisch. Der Präprozessor erkennt auch negative Zeichenwerte.

Der HLSL-Präprozessor erkennt die folgenden Direktiven:

-   [\#define](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#Zeit](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#if](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#darunter](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#Stimmen](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

Das Nummern Zeichen ( \# ) muss das erste nicht-Leerzeichen in der Zeile sein, die die Direktive enthält. Leerzeichen können zwischen dem Nummern Zeichen und dem ersten Buchstaben der Direktive angezeigt werden. Manche Anweisungen enthalten Argumente oder Werte. Jedem Text, der auf eine Direktive folgt (außer einem Argument oder einem Wert, der Teil der Direktive ist), muss das einzeilige Kommentar Trennzeichen (//) vorangestellt sein, oder es muss in Kommentar Trennzeichen (/ \* \* /) eingeschlossen werden. Zeilen, die Präprozessordirektiven enthalten, können fortgesetzt werden, indem unmittelbar vor dem Zeilenende Marker mit einem umgekehrten Schrägstrich ( \) .

Präprozessoranweisungen können an beliebiger Stelle in einer Quelldatei auftreten, aber sie gelten nur für den Rest der Quelldatei.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anhang (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




