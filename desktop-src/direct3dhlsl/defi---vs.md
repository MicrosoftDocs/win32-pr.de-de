---
title: Defi-vs
description: Definiert einen ganzzahligen Konstanten Wert, der immer dann geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517006"
---
# <a name="defi---vs"></a>Defi-vs

Definiert einen ganzzahligen Konstanten Wert, der immer dann geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.

## <a name="syntax"></a>Syntax



| Defi DST, integerValue0, integerValue1, integerValue2, integerValue3 |
|----------------------------------------------------------------------|



 

-   DST ist das Ziel Register.
-   integerValue \# ist ein konstanter ganzzahliger Wert.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| verteidigen                   |      | x    | x    | x     | x    | x     |



 

Die defi-Anweisung definiert eine ganzzahlige Shader-Konstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist. Diese werden als unmittelbare Konstanten bezeichnet. Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode setvertexshaderconstanti festgelegt werden.

Es gibt zwei Möglichkeiten, eine ganzzahlige Konstante in einem Shader festzulegen.

1.  Verwenden Sie defi, um den ganzzahligen Konstanten Vektor direkt in einem Shader zu definieren.
2.  Verwenden Sie die API-Methoden, um eine Konstante festzulegen.
    -   Verwenden Sie [**setvertexshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) , um eine ganzzahlige Konstante festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[DEF-vs](def---vs.md)
</dt> <dt>

[DEFB-vs](defb---vs.md)
</dt> </dl>

 

 