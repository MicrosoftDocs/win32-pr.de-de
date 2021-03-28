---
title: DEFB-vs
description: Definiert einen booleschen Konstanten Wert, der immer dann geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948766"
---
# <a name="defb---vs"></a>DEFB-vs

Definiert einen booleschen Konstanten Wert, der immer dann geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.

## <a name="syntax"></a>Syntax



| DEFB dest, BooleanValue |
|-------------------------|



 

where

-   DST ist das Ziel Register.
-   BooleanValue ist ein boolescher Wert, entweder true oder false.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| DEFB                   |      | x    | x    | x     | x    | x     |



 

Die DEFB-vs-Anweisung definiert eine boolesche Shader-Konstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist. Diese werden als unmittelbare Konstanten bezeichnet. Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode setvertexshaderconstantb festgelegt werden.

Es gibt zwei Möglichkeiten, eine boolesche Konstante in einem Shader festzulegen.

1.  Verwenden Sie DEFB-vs, um die Konstante direkt in einem Shader zu definieren.
2.  Verwenden Sie die API-Methoden, um eine Konstante festzulegen.
    -   Verwenden Sie [**setvertexshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) , um eine boolesche Konstante festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[DEF-vs](def---vs.md)
</dt> <dt>

[Defi-vs](defi---vs.md)
</dt> </dl>

 

 