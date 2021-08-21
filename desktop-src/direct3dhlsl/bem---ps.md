---
title: bem - ps
description: Wenden Sie eine falsche Umgebungszuordnungstransformation an.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fdc28e6eaf71156504306b247a1a2a3797423f9a7e3bde6d4040ecb1297e09da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794821"
---
# <a name="bem---ps"></a>bem - ps

Wenden Sie eine falsche Umgebungszuordnungstransformation an.

## <a name="syntax"></a>Syntax



| bem dst.rg, src0, src1 |
|------------------------|



 

where

-   dst.rg dst ist das Zielregister. Die Schreibmaske der roten und grünen Komponente muss verwendet werden.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Bem                   |      |      |      | x    |      |      |       |      |       |



 

Diese Anweisung führt die folgende Berechnung aus.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Regeln für die Verwendung von bem:

1.  bem muss in der ersten Phase eines Shaders (d. h. vor einem Phasenmarker) angezeigt werden.
2.  bem verwendet zwei arithmetische Anweisungsslots.
3.  Pro Shader ist nur eine Verwendung dieser Anweisung zulässig.
4.  Die Ziel-Schreibmaske muss .rg /.xy sein.
5.  Diese Anweisung kann nicht gemeinsam ausgegeben werden.
6.  Abgesehen von der Einschränkung, dass die Ziel-Schreibmaske .rg ist, sind Modifizierer für die Quellmodifizierer src0, src1 und anweisungsmodifizierer uneingeschränkt.

## <a name="instruction-information"></a>Anweisungsinformationen



| Anforderung                         | Wert           |
|--------------------------|------------|
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




