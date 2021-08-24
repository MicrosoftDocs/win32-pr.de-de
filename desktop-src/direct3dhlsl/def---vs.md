---
title: def – vs
description: Definiert Vertex-Shaderkonstanten.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5e3d5cbeb4d60f7beffd70c30ba0775863a9782cfb365a4d40bdf5552a186f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855350"
---
# <a name="def---vs"></a>def – vs

Definiert Vertex-Shaderkonstanten.

## <a name="syntax"></a>Syntax



| def dst, float1, float2, float3, float4 |
|-----------------------------------------|



 

where

-   dst ist das Zielregister.
-   float1, float2, float3, float4 sind vier Gleitkommazahlen.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

Die def-Anweisung definiert eine Shaderkonstante, deren Wert jedes Mal geladen wird, wenn ein Shader auf ein Gerät festgelegt wird. Diese werden als sofortige Konstanten bezeichnet. Direkte Konstanten haben Vorrang vor Konstanten, die von den API-Methoden SetVertexShaderConstantF festgelegt werden.

Es gibt zwei Möglichkeiten, eine Konstante in einem Shader festzulegen.

1.  Verwenden Sie def – vs , um die Konstante direkt in einem Shader zu definieren.

    def : vs kann nur Gleitkommakonstanten definieren.

2.  Verwenden Sie die API-Methoden, um eine Konstante festzulegen.
    -   Verwenden Sie [**SetVertexShaderConstantF,**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) um eine Gleitkommakonstante festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[defi – vs](defi---vs.md)
</dt> <dt>

[defb – vs](defb---vs.md)
</dt> </dl>

 

 