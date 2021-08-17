---
title: dcl_usage ausgabe (sm1, sm2, sm3 – vs asm)
description: Die verschiedenen Arten von Ausgaberegistern wurden zu zwölf Ausgaberegistern reduziert (zwei für Farbe, acht für Textur, eines für position und eines für die Größe von 2007 Und Punkt).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee5f444cbf145957ad93db00160d812e75e4a624019ad9f578b5dc960e84f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726717"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>dcl \_ usage output (sm1, sm2, sm3 – vs asm)

Die verschiedenen Arten von Ausgaberegistern wurden zu zwölf Ausgaberegistern reduziert (zwei für Farbe, acht für Textur, eines für position und eines für die Größe von 2007 Und Punkt). Diese können für alles verwendet werden, was der Benutzer für den Pixel-Shader interpolieren möchte: Texturkoordinaten, Farben, Schnee und so weiter.

Ausgaberegister erfordern Deklarationen, die Semantik enthalten. Beispielsweise werden die alten Register für Position und Punktgröße ersetzt, indem ein Ausgaberegister mit einer Positions- oder Punktgrößensemantik deklariert wird.

Von den zwölf Ausgaberegistern verfügen alle zehn (nicht unbedingt o0 bis o9) über vier Komponenten (xyzw), ein weiteres muss als Position deklariert werden (und muss auch alle vier Komponenten enthalten), und optional kann eine weitere eine Skalarpunktgröße sein.

## <a name="syntax"></a>Syntax

Die Syntax zum Deklarieren von Ausgaberegistern ähnelt den Deklarationen für das Eingaberegister:



|                                  |
|----------------------------------|
| dcl \_ semantics o \[ .write \_ mask\] |



 

Hierbei gilt:

-   Die \_ dcl-Semantik kann denselben Semantiksatz wie für die Eingabedeklaration verwenden. Semantische Namen stammen [**aus D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (und sind mit einem Index gekoppelt, z. B. position3). Es muss immer ein Ausgaberegister mit der positiont0-Semantik geben, wenn es nicht für die Verarbeitung von Scheitelten verwendet wird. Die semantische Position 0 und die pointsize0-Semantik sind die einzigen Semantik, die eine Bedeutung haben, über das einfache Zulassen der Verknüpfung von Scheitelpunkt zu Pixel-Shadern hinaus. Bei Shadern mit Flusssteuerung wird davon ausgegangen, dass die Ausgabe im ungünstigsten Fall deklariert ist. Es gibt keine Standardwerte, wenn ein Shader nicht tatsächlich aus gibt, was er deklarieren sollte (aufgrund der Flusssteuerung).
-   o ist ein Ausgaberegister. Weitere Informationen [finden Sie \_ unter Ausgaberegister.](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)
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

 

 
