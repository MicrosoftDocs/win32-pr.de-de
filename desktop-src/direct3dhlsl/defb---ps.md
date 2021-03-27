---
title: DEFB-PS
description: Definiert einen booleschen Konstanten Wert, der jedes Mal geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729176"
---
# <a name="defb---ps"></a>DEFB-PS

Definiert einen booleschen Konstanten Wert, der jedes Mal geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.

## <a name="syntax"></a>Syntax



| DEFB dest, BooleanValue |
|-------------------------|



 

where

-   DST ist das Ziel Register.
-   BooleanValue ist ein einzelner boolescher Wert, entweder true oder false.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DEFB                  |      |      |      |      |      | x    | x     | x    | x     |



 

Die DEFB-Anweisung definiert eine boolesche Shader-Konstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist. Diese werden als unmittelbare Konstanten bezeichnet. Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode setpixelshaderconstantb festgelegt werden.

Es gibt zwei Möglichkeiten, eine BooleanConstant in einem Shader festzulegen.

1.  Verwenden Sie DEFB, um die Konstante direkt in einem Shader zu definieren.
2.  Verwenden Sie die API-Methoden, um eine Konstante festzulegen.
    -   Verwenden Sie [**setpixelshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) , um eine boolesche Konstante festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[DEF-PS](def---ps.md)
</dt> <dt>

[Defi-PS](defi---ps.md)
</dt> </dl>

 

 