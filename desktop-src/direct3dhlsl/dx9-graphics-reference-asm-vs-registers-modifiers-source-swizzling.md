---
title: Quellen Register (swizzling) (HLSL vs-Referenz)
description: Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quell Register in ein temporäres Register kopiert. Swizzling bezieht sich auf die Möglichkeit, beliebige Quell Registrierungs Komponenten in beliebige temporäre Register Komponenten zu kopieren. Das Schwenken wirkt sich nicht auf die Quell Registrierungsdaten aus.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104389620"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a>Quellen Register (swizzling) (HLSL vs-Referenz)

Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quell Register in ein temporäres Register kopiert. Swizzling bezieht sich auf die Möglichkeit, beliebige Quell Registrierungs Komponenten in beliebige temporäre Register Komponenten zu kopieren. Das Schwenken wirkt sich nicht auf die Quell Registrierungsdaten aus.

## <a name="component-swizzling"></a>Komponenten schwenken

Wie in der folgenden Tabelle gezeigt, kann das Schwenken auf die einzelnen Komponenten der Quell Registrierungsdaten angewendet werden (wobei es sich bei um einen der gültigen Vertex-Shader [-Eingabe Register-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)handelt).



| Komponentenmodifizierer                 | BESCHREIBUNG    |
|------------------------------------|----------------|
| r. \[ xyzw xyzw xyzw xyzw \] \[ \] \[ \] \[\] | Quellen-wischen |



 

-   Alle vier Komponenten werden immer kopiert. Wenn weniger als vier Komponenten angegeben werden, wird die letzte Komponente wiederholt (XY means. XYYY). Wenn keine Komponenten angegeben werden, wird x wiederholt (. xxxx).
-   Die Komponenten können in beliebiger Reihenfolge angezeigt werden. "v0. ywx" ergibt "v0. ywxx".
-   Die RGBA-Komponenten können für xyzw verwendet werden (r für x, g für b usw.).
-   Diese Anweisungen implementieren Quellen Register für einzelne Komponenten: Exp, EXPP, Log, LogP, Pow, rcp, RSQ. Das Ergebnis dieser Anweisungen wird in alle vier Ziel Register Komponenten kopiert.

"Swizzling" kann nicht in den Anweisungen [m3x2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)und [M4x4-vs](m4x4---vs.md) verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




