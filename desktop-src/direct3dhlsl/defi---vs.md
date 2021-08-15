---
title: defi – vs
description: Definiert einen ganzzahligen konstanten Wert, der immer dann geladen werden sollte, wenn ein Shader auf ein Gerät festgelegt wird.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5568a9d1db49dadb9e0e6497cfd4e5af357054f930c35ec6a7e05d59d5f60965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726680"
---
# <a name="defi---vs"></a>defi – vs

Definiert einen ganzzahligen konstanten Wert, der immer dann geladen werden sollte, wenn ein Shader auf ein Gerät festgelegt wird.

## <a name="syntax"></a>Syntax



| defi dst, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   dst ist das Zielregister.
-   integerValue \# ist ein konstanter ganzzahliger Wert.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Defi                   |      | x    | x    | x     | x    | x     |



 

Die Defi-Anweisung definiert eine Ganzzahl-Shaderkonstance, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt wird. Diese werden als direkt konstante Konstanten bezeichnet. Direktkonstanten haben Vorrang vor Konstanten, die von der API-Methode SetVertexShaderConstantI festgelegt werden.

Es gibt zwei Möglichkeiten, eine ganzzahlige Konstante in einem Shader zu setzen.

1.  Verwenden Sie defi, um den ganzzahligen konstanten Vektor direkt in einem Shader zu definieren.
2.  Verwenden Sie die API-Methoden, um eine Konstante zu setzen.
    -   Verwenden [**Sie SetVertexShaderConstantI,**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) um eine ganzzahlige Konstante zu setzen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def – vs](def---vs.md)
</dt> <dt>

[defb – vs](defb---vs.md)
</dt> </dl>

 

 