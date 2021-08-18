---
title: Quellregister swizzling (HLSL VS-Referenz)
description: Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quellregister in ein temporäres Register kopiert. Swizzling bezieht sich auf die Möglichkeit, jede Quellregisterkomponente in eine beliebige temporäre Registerkomponente zu kopieren. Swizzling wirkt sich nicht auf die Quellregisterdaten aus.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03dd2d9051c185d1be1ccb6fce18549bf5aa3414975c9a600bb8f8c47f78d4c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854550"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Quellregister swizzling (HLSL VS-Referenz)

Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quellregister in ein temporäres Register kopiert. Swizzling bezieht sich auf die Möglichkeit, jede Quellregisterkomponente in eine beliebige temporäre Registerkomponente zu kopieren. Swizzling wirkt sich nicht auf die Quellregisterdaten aus.

## <a name="component-swizzling"></a>Component Swizzling

Wie in der folgenden Tabelle gezeigt, kann Swizzling auf die einzelnen Komponenten der Quellregisterdaten angewendet werden (wobei eines der gültigen Vertex-Shadereingaberegister ist – im Vergleich [ \_ zu 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).



| Komponentenmodifizierer                 | Beschreibung    |
|------------------------------------|----------------|
| r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw xyzw\] | Quell-Swizzle |



 

-   Alle vier Komponenten werden immer kopiert. Wenn weniger als vier Komponenten angegeben werden, wird die letzte Komponente wiederholt (xy bedeutet .xyyy). Wenn keine Komponenten angegeben werden, wird x wiederholt (.xxxx).
-   Die Komponenten können in beliebiger Reihenfolge angezeigt werden. v0.ywx führt zu v0.ywxx.
-   Die rgba-Komponenten können jeweils für xyzw verwendet werden (r für x, g für b usw.).
-   Diese Anweisungen implementieren swizzles für die Quellregister-Einzelkomponente: exp, expp, log, logp, pow, rcp, rsq. Das Ergebnis dieser Anweisungen wird in alle vier Zielregisterkomponenten kopiert.

Swizzling kann nicht auf [m3x2](m3x2---vs.md)im Vergleich zu , [m3x3 im](m3x3---vs.md)Vergleich zu , [m4x3 – vs](m4x3---vs.md)und [m4x4 –](m4x4---vs.md) im Vergleich zu Anweisungen verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Registermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




