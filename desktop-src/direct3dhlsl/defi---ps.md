---
title: Defi-PS
description: Definiert einen ganzzahligen Konstanten Wert, der jedes Mal geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102078"
---
# <a name="defi---ps"></a>Defi-PS

Definiert einen ganzzahligen Konstanten Wert, der jedes Mal geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.

## <a name="syntax"></a>Syntax



| Defi DST, integerValue |
|------------------------|



 

-   DST ist das Ziel Register.
-   integerValue ist ein konstanter ganzzahliger Wert.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| verteidigen                  |      |      |      |      |      | x    | x     | x    | x     |



 

Die defi-Anweisung definiert eine shaderkonstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist. Diese werden als unmittelbare Konstanten bezeichnet. Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode setpixelshaderconstantb festgelegt werden.

Es gibt zwei Möglichkeiten, eine Konstante in einem Shader festzulegen.

1.  Verwenden Sie defi, um die Konstante direkt in einem Shader zu definieren.
2.  Verwenden Sie die API-Methoden, um eine Konstante festzulegen.
    -   Verwenden Sie [**setpixelshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) , um eine boolesche Konstante festzulegen.
    -   Verwenden Sie [**setpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) , um eine Gleit Komma Konstante festzulegen.
    -   Verwenden Sie [**setpixelshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) , um eine ganzzahlige Konstante festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 