---
title: texm3x2pad – ps
description: Führt die erste Zeilenmultiplikation einer Multiplikation einer zweizeilenbasierten Matrix durch. Diese Anweisung muss entweder mit texm3x2tex – ps oder texm3x2depth – ps kombiniert werden. Weitere Informationen zur Verwendung von texmpad finden Sie in diesen Anweisungen.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55943d2a62f49e6bdb45d893385f0824898d665ee4a4065c4f8c8ed75c2f8249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485440"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad – ps

Führt die erste Zeilenmultiplikation einer Multiplikation einer zweizeilenbasierten Matrix durch. Diese Anweisung muss entweder mit [texm3x2tex – ps](texm3x2tex---ps.md) oder [texm3x2depth – ps – kombiniert werden.](texm3x2depth---ps.md) Weitere Informationen zur Verwendung von texmpad finden Sie in diesen Anweisungen.

## <a name="syntax"></a>Syntax



| tex3x2pad dst, src |
|--------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung kann nicht allein verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




