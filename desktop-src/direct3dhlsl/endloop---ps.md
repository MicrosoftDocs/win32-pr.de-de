---
title: endloop – ps
description: Ende einer Schleife – ps... endloop-Block.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b35daa5ca00db04b6e69dc70dd1a07aaf1287c2f9188819d5b65af9773edfe1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982490"
---
# <a name="endloop---ps"></a>endloop – ps

Ende einer [Schleife – ps](loop---ps.md)... endloop-Block.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| endloop               |      |      |      |      |      |      |       | x    | x     |



 

endloop muss der letzten Anweisung einer [Schleife](loop---ps.md) folgen – ps block.

## <a name="example"></a>Beispiel


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




