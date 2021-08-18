---
title: defb – vs
description: Definiert einen booleschen konstanten Wert, der jedes Mal geladen werden soll, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e5ace74e275ae63a62306d47d50924e9c4e9a9771027e75659ef72345f69906d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792672"
---
# <a name="defb---vs"></a>defb – vs

Definiert einen booleschen konstanten Wert, der jedes Mal geladen werden soll, wenn ein Shader auf ein Gerät festgelegt ist.

## <a name="syntax"></a>Syntax



| defb dest, booleanValue |
|-------------------------|



 

where

-   dst ist das Zielregister.
-   booleanValue ist ein boolescher Wert, entweder True oder False.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| defb                   |      | x    | x    | x     | x    | x     |



 

Die Anweisung defb – vs definiert eine boolesche Shaderkonstante, deren Wert jedes Mal geladen wird, wenn ein Shader auf ein Gerät festgelegt wird. Diese werden als sofortige Konstanten bezeichnet. Direkte Konstanten haben Vorrang vor Konstanten, die von der API-Methode SetVertexShaderConstantB festgelegt werden.

Es gibt zwei Möglichkeiten, eine boolesche Konstante in einem Shader festzulegen.

1.  Verwenden Sie defb – vs , um die Konstante direkt in einem Shader zu definieren.
2.  Verwenden Sie die API-Methoden, um eine Konstante festzulegen.
    -   Verwenden Sie [**SetVertexShaderConstantB,**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) um eine boolesche Konstante festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def – vs](def---vs.md)
</dt> <dt>

[defi – vs](defi---vs.md)
</dt> </dl>

 

 