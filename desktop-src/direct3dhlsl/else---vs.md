---
title: Else-vs
description: Start eines Else-Blocks. | Else-vs
ms.assetid: c3bd99c2-35a1-4ffd-9781-4bac9f6bb0ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97481d7cb651719fdf0843fd1b985c6586e54b3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981913"
---
# <a name="else---vs"></a>Else-vs

Start eines Else-Blocks.

## <a name="syntax"></a>Syntax



| else |
|------|



 

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| else                   |      | x    | x    | x     | x    | x     |



 

Wenn die Bedingung in der entsprechenden [if bool-vs-](if-bool---vs.md) Anweisung True ist, wird der Code, der von der if bool-vs-Anweisung und der passenden [EndIf](endif---vs.md) eingeschlossen wird, ausgeführt. Andernfalls wird der Code, der von der else... ENDIF-Anweisungen werden ausgeführt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[Wenn bool-vs](if-bool---vs.md)
</dt> <dt>

[umdif-vs](endif---vs.md)
</dt> </dl>

 

 




