---
title: texm3x2pad-PS
description: Führt die erste Zeilen Multiplikation einer zweizeiligen Matrix Multiplikation aus. Diese Anweisung muss entweder mit texm3x2tex-PS oder texm3x2depth-PS kombiniert werden. Weitere Informationen zur Verwendung von texmpad finden Sie in den folgenden Anweisungen.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857787"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad-PS

Führt die erste Zeilen Multiplikation einer zweizeiligen Matrix Multiplikation aus. Diese Anweisung muss entweder mit [texm3x2tex-PS](texm3x2tex---ps.md) oder [texm3x2depth-PS](texm3x2depth---ps.md)kombiniert werden. Weitere Informationen zur Verwendung von texmpad finden Sie in den folgenden Anweisungen.

## <a name="syntax"></a>Syntax



| tex3x2pad DST, src |
|--------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung kann nicht allein verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




