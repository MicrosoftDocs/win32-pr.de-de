---
title: if bool - ps
description: Start eines if-Blocks.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 611ec04a5c3a53bbb8c6c35380bd0d9f824dc697a7d27a3656b262d885fb4eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457510"
---
# <a name="if-bool---ps"></a>if bool - ps

Start eines if-Blocks.

## <a name="syntax"></a>Syntax



| if bool |
|---------|



 

Hierbei gilt:

-   bool ist eine boolesche Registernummer. Weitere Informationen [finden Sie unter Konstantes boolesches Register.](dx9-graphics-reference-asm-ps-registers-constant-boolean.md)

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| if bool               |      |      |      |      |      | x    | x     | x    | x     |



 

Wenn das boolesche Quellregister in der if-Anweisung true ist, wird der code ausgeführt, der von der if-Anweisung und dem entsprechenden [endif - ps](endif---ps.md) oder [else - ps eingeschlossen](else---ps.md) wird. Andernfalls wird der Code, der von else eingeschlossen ist, ps... endif: PS-Anweisungen werden ausgeführt. Diese Anweisung verwendet einen Anweisungsslot.

Ein if-Block kann geschachtelt werden.

Ein if-Block kann einen Schleifenblock nicht umschnallen.

Auf einen if-Block kann ein Anweisungsblock und/oder eine [else - ps-Anweisung](else---ps.md) und/oder eine [endif - ps-Anweisung folgen.](endif---ps.md)

## <a name="example"></a>Beispiel

Diese Anweisung bietet eine bedingte statische Flusssteuerung.


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

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[else – ps](else---ps.md)
</dt> <dt>

[endif – ps](endif---ps.md)
</dt> </dl>

 

 




