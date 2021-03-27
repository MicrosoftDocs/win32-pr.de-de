---
title: Wenn bool-PS
description: Beginn eines If-Blocks.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719355"
---
# <a name="if-bool---ps"></a>Wenn bool-PS

Beginn eines If-Blocks.

## <a name="syntax"></a>Syntax



| Wenn bool |
|---------|



 

Hierbei gilt:

-   bool ist eine boolesche (Boolean) Registernummer. Siehe [konstantes boolesches Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Wenn bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Wenn das boolesche Quell Konto in der if-Anweisung den Wert true hat, wird der Code, der von der if-Anweisung und der entsprechenden [EndIf-PS](endif---ps.md) oder [else-PS](else---ps.md) eingeschlossen wird, ausgeführt. Andernfalls wird der Code, der von der Else-PS... EndIf-PS-Anweisungen werden ausgeführt. Diese Anweisung verwendet einen Anweisungs Slot.

Ein If-Block kann eingefügt werden.

Ein If-Block kann einen Schleifen Block nicht verspannen.

Auf einen If-Block kann ein Anweisungsblock und/oder eine [else-PS](else---ps.md) -Anweisung und/oder eine [EndIf-PS-](endif---ps.md) Anweisung folgen.

## <a name="example"></a>Beispiel

Diese Anweisung stellt bedingte statische Fluss Steuerung bereit.


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Else-PS](else---ps.md)
</dt> <dt>

[in-PS-PS](endif---ps.md)
</dt> </dl>

 

 




