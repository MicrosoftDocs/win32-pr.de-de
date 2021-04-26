---
title: dcl_usage Ausgabe (sm1, sm2, sm3 – vs asm)
description: Die verschiedenen Arten von Ausgaberegistern wurden in zwölf Ausgaberegister reduziert (zwei für Farbe, acht für Textur, eins für die Position und eins für Dies und Punktgröße).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 314c9c9a9a9e62915e9224b3cf165bc54d09a516
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999167"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>dcl \_ usage output (sm1, sm2, sm3 - vs asm)

Die verschiedenen Arten von Ausgaberegistern wurden in zwölf Ausgaberegister reduziert (zwei für Farbe, acht für Textur, eins für die Position und eins für Dies und Punktgröße). Diese können für alles verwendet werden, was der Benutzer für den Pixelshader interpolieren möchte: Texturkoordinaten, Farben, Oberflächen usw.

Ausgaberegister erfordern Deklarationen, die Semantik enthalten. Beispielsweise werden die alten Register für Position und Punktgröße ersetzt, indem ein Ausgaberegister mit einer Position oder einer Punktgrößensemantik deklariert wird.

Von den zwölf Ausgaberegistern verfügen alle zehn (nicht unbedingt o0 bis o9) über vier Komponenten (xyzw), eine andere muss als Position deklariert werden (und muss auch alle vier Komponenten enthalten), und optional kann eine weitere Skalarpunktgröße sein.

## <a name="syntax"></a>Syntax

Die Syntax zum Deklarieren von Ausgaberegistern ähnelt den Deklarationen für das Eingaberegister:



|                                  |
|----------------------------------|
| dcl \_ semantics o \[ .write \_ mask\] |



 

Hierbei gilt:

-   Die \_ dcl-Semantik kann den gleichen Semantiksatz wie für die Eingabedeklaration verwenden. Semantische Namen stammen aus [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (und werden mit einem Index gekoppelt, z.B. position3). Es muss immer ein Ausgaberegister mit der Semantik positiont0 vorhanden sein, wenn es nicht für die Verarbeitung von Scheitelpunkten verwendet wird. Die Positiont0-Semantik und die Pointsize0-Semantik sind die einzigen, die eine Bedeutung haben, die über die einfache Verknüpfung von Scheitelpunkt- zu Pixel-Shadern hinausgeht. Bei Shadern mit Flusssteuerung wird davon ausgegangen, dass die Ausgabe im schlechtesten Fall deklariert wird. Es gibt keine Standardwerte, wenn ein Shader nicht tatsächlich ausgibt, was er deklariert (aufgrund der Flusssteuerung).
-   o ist ein Ausgaberegister. Weitere Informationen finden Sie [ \_ unter Ausgaberegister.](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)
-   Die Schreibmaske gibt dasselbe Ausgaberegister an, das mehrmals deklariert werden kann (sodass unterschiedliche Semantik auf einzelne Komponenten angewendet werden kann), jedes Mal mit einer eindeutigen \_ Schreibmaske. Die gleiche Semantik kann jedoch nicht mehrmals in einer Deklaration verwendet werden. Dies bedeutet, dass Vektoren vier Komponenten oder weniger sein müssen und nicht über Vier-Komponenten-Registergrenzen (einzelne Register) hinweg gehen können. Wenn die Semantik der Punktgröße verwendet wird, sollte sie über eine vollständige Schreibmaske verfügen, da sie als Skalar betrachtet wird. Wenn die Positionssemantik verwendet wird, sollte sie über eine vollständige Schreibmaske verfügen, da alle vier Komponenten geschrieben werden müssen.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 3 \_ 0 | 3 \_ sw |
|------------------------|------|-------|
| dcl \_ usage             | x    | x     |



 

Alle [ \_ dcl-Verwendungsanweisungen](dcl-usage-input-register---vs.md) müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="declaration-examples"></a>Deklarationsbeispiele


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
