---
title: def – ps
description: Definiert Pixel-Shader-Gleitkommakonstierungen.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce5f842f44e915d3f3240618261b501f2240c3636227f930538e1bbcbe0d9367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726560"
---
# <a name="def---ps"></a>def – ps

Definiert Pixel-Shader-Gleitkommakonstierungen.

## <a name="syntax"></a>Syntax



| def dst, fVvalue1, fValue2, fValue3, fValue4 |
|----------------------------------------------|



 

Hierbei gilt:

-   dst ist das Zielregister.
-   fValue1 bis fValue4 sind Gleitkommawerte.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| def                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Es gibt zwei Möglichkeiten, eine Gleitkommakonstance in einem Pixel-Shader zu setzen.

1.  Verwenden Sie def, um die Konstante direkt in einem Shader zu definieren.
2.  Verwenden Sie die API, um eine Konstante mit [**SetPixelShaderConstantF festlegen.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

def definiert eine Shaderkonstation, deren Wert jedes Mal geladen wird, wenn ein Shader auf ein Gerät festgelegt wird. Diese werden als sofortige Konstanten bezeichnet. Direkte Konstanten haben Vorrang vor Konstanten, die von der API-Methode festgelegt werden.

-   Muss vor der ersten Arithmetik- oder Adressierungsanweisung im Shader angezeigt werden.
-   Kann mit [dcl- (sm2, sm3 - ps asm)-Anweisungen](dcl---ps.md) (dies sind die anderen Anweisungstypen, die sich am Anfang eines Shaders befinden) miteinander vermiert werden.
-   dst register muss ein [konstantes Register sein.](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
-   Die Schreibmaske muss voll sein (Standard).
-   Wenn ein [konstantes](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) Register mehrmals in einem Shader definiert wird, wird das letzte beibehalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 