---
title: DEF-PS
description: Definiert Pixel-Shader-Gleit Komma Konstanten.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039548"
---
# <a name="def---ps"></a>DEF-PS

Definiert Pixel-Shader-Gleit Komma Konstanten.

## <a name="syntax"></a>Syntax



| DEF DST, fVvalue1, fValue2, fValue3, fValue4 |
|----------------------------------------------|



 

Hierbei gilt:

-   DST ist das Ziel Register.
-   fValue1 to fValue4 sind Gleit Komma Werte.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Es gibt zwei Möglichkeiten, eine Gleit Komma Konstante in einem Pixelshader festzulegen.

1.  Verwenden Sie def, um die Konstante direkt in einem Shader zu definieren.
2.  Verwenden Sie die-API, um eine Konstante mit [**setpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)festzulegen.

DEF definiert eine shaderkonstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist. Diese werden als unmittelbare Konstanten bezeichnet. Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode festgelegt werden.

-   Muss vor der ersten arithmetischen oder Adressierungs Anweisung im Shader angezeigt werden.
-   Kann mit [DCL-(SM2, SM3-PS ASM)-](dcl---ps.md) Anweisungen gemischt werden (bei denen es sich um den anderen Typ der Anweisung handelt, die sich am Anfang eines Shaders befindet).
-   das DST-Register muss ein [konstantes Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)sein.
-   Die Schreib Maske muss voll (Standard) sein.
-   Wenn ein [konstantes Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) mehrmals in einem Shader definiert ist, wird das letzte beibehalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 