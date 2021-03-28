---
title: dcl_usage Ausgabe (SM1, SM2, SM3-vs ASM)
description: Die verschiedenen Typen von Ausgabe Registern wurden in zwölf Ausgabe Register reduziert (zwei für Farbe, acht für die Textur, eine für die Position und eine für den Nebel und die Punktgröße).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993526"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>DCL- \_ Verwendungs Ausgabe (SM1, SM2, SM3-vs ASM)

Die verschiedenen Typen von Ausgabe Registern wurden in zwölf Ausgabe Register reduziert (zwei für Farbe, acht für die Textur, eine für die Position und eine für den Nebel und die Punktgröße). Diese können für alle Elemente verwendet werden, die der Benutzer für den Pixelshader interpolieren möchte: Texturkoordinaten, Farben, Nebel usw.

Ausgabe Register erfordern Deklarationen, die Semantik einschließen. Beispielsweise werden die alten Positions-und Punktgrößen Register durch Deklarieren eines Ausgabe Registers mit einer Position oder einer Semantik für die Punktgröße ersetzt.

Von den zwölf Ausgabe Registern verfügen alle zehn (nicht notwendigerweise o0 bis O9) über vier Komponenten (xyzw), eine andere muss als Position deklariert werden (und müssen auch alle vier Komponenten enthalten), und optional kann auch eine skalare Punktgröße sein.

## <a name="syntax"></a>Syntax

Die Syntax zum Deklarieren von Ausgabe Registern ähnelt den Deklarationen für das Eingabe Register:



|                                  |
|----------------------------------|
| DCL- \_ Semantik o \[ . Schreib \_ Maske\] |



 

Hierbei gilt:

-   die DCL- \_ Semantik kann denselben Satz von Semantik wie für die Eingabe Deklaration verwenden. Semantik Namen stammen aus [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (und sind mit einem Index gekoppelt, z. b. Position3). Es muss immer ein Ausgabe Register mit der positiont0 Semantic vorhanden sein, wenn es nicht für die Verarbeitung von Scheitel Punkten verwendet wird. Die Semantik positiont0 Semantic und pointsize0 sind die einzigen, die die Bedeutung haben, die über die einfache Verknüpfung von Scheitel Punkten zu Pixel-Shadern hinausgehen. Für Shader mit Fluss Steuerung wird angenommen, dass die schlechteste Fall Ausgabe deklariert wird. Es gibt keine Standardwerte, wenn ein Shader nicht tatsächlich angibt, was er deklariert (aufgrund der Fluss Steuerung).
-   o ist ein Ausgabe Register. Siehe [Ausgabe \_ Register](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).
-   \_die Schreib Maske gibt das gleiche Ausgabe Register an, das mehrmals deklariert werden kann (damit unterschiedliche Semantik auf einzelne Komponenten angewendet werden kann), und zwar jedes Mal mit einer eindeutigen Schreib Maske. Die gleiche Semantik kann jedoch nicht mehrmals in einer Deklaration verwendet werden. Dies bedeutet, dass Vektoren vier Komponenten oder weniger sein müssen und nicht über vier Komponenten Register Grenzen (einzelne Register) hinausgehen können. Wenn die Semantik für die Punktgröße verwendet wird, sollte Sie über eine vollständige Schreib Maske verfügen, da Sie als Skalar angesehen wird. Wenn die Positions Semantik verwendet wird, sollte Sie über eine vollständige Schreib Maske verfügen, da alle vier Komponenten geschrieben werden müssen.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 3 \_ 0 | 3 \_ SW |
|------------------------|------|-------|
| DCL- \_ Verwendung             | x    | x     |



 

Alle [DCL- \_ Verwendungs](dcl-usage-input-register---vs.md) Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="declaration-examples"></a>Deklarations Beispiele


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

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 