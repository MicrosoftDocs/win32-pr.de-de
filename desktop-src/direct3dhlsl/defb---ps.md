---
title: defb – ps
description: Definiert einen booleschen konstanten Wert, der jedes Mal geladen werden soll, wenn ein Shader auf ein Gerät festgelegt wird.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ad823cd9932e98f919764e57666549189623986eb173ba6b4ef74cdade21f33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855360"
---
# <a name="defb---ps"></a>defb – ps

Definiert einen booleschen konstanten Wert, der jedes Mal geladen werden soll, wenn ein Shader auf ein Gerät festgelegt wird.

## <a name="syntax"></a>Syntax



| defb dest, booleanValue |
|-------------------------|



 

where

-   dst ist das Zielregister.
-   booleanValue ist ein einzelner boolescher Wert, entweder true oder false.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defb                  |      |      |      |      |      | x    | x     | x    | x     |



 

Die defb-Anweisung definiert eine boolesche Shaderkonstation, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt wird. Diese werden als sofortige Konstanten bezeichnet. Direktkonstanten haben Vorrang vor Konstanten, die von der API-Methode SetPixelShaderConstantB festgelegt werden.

Es gibt zwei Möglichkeiten, einen booleschen Wert in einem Shader zu setzen.

1.  Verwenden Sie defb, um die Konstante direkt in einem Shader zu definieren.
2.  Verwenden Sie die API-Methoden, um eine Konstante zu setzen.
    -   Verwenden [**Sie SetPixelShaderConstantB,**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) um eine boolesche Konstante zu setzen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[def – ps](def---ps.md)
</dt> <dt>

[defi – ps](defi---ps.md)
</dt> </dl>

 

 