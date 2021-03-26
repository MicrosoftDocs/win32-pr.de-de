---
title: DEF-vs
description: Definiert Scheitelpunkt-Shader-Konstanten.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209344"
---
# <a name="def---vs"></a>DEF-vs

Definiert Scheitelpunkt-Shader-Konstanten.

## <a name="syntax"></a>Syntax



| DEF DST, float1, float2, float3, float4 |
|-----------------------------------------|



 

where

-   DST ist das Ziel Register.
-   float1, float2, float3, float4 sind vier Gleit Komma Zahlen.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

Die DEF-Anweisung definiert eine shaderkonstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist. Diese werden als unmittelbare Konstanten bezeichnet. Unmittelbare Konstanten haben Vorrang vor Konstanten, die von den API-Methoden setvertexshaderconstantf festgelegt werden.

Es gibt zwei Möglichkeiten, eine Konstante in einem Shader festzulegen.

1.  Verwenden Sie DEF-vs, um die Konstante direkt in einem Shader zu definieren.

    DEF-vs können nur Gleit Komma Konstanten definieren.

2.  Verwenden Sie die API-Methoden, um eine Konstante festzulegen.
    -   Verwenden Sie [**setvertexshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) , um eine Gleit Komma Konstante festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[Defi-vs](defi---vs.md)
</dt> <dt>

[DEFB-vs](defb---vs.md)
</dt> </dl>

 

 