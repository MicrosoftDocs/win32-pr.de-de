---
description: Definiert den Grad der Variablen in der Gleichung, die eine Kurve beschreibt.
ms.assetid: 52a9c57e-a48d-4d8a-a208-97a3d09e7abf
title: D3DDEGREETYPE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEGREETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6daacc007438903d3f003a19038b4ea6909814e3a5d024d3df6daa95a0c60602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989050"
---
# <a name="d3ddegreetype-enumeration"></a>D3DDEGREETYPE-Enumeration

Definiert den Grad der Variablen in der Gleichung, die eine Kurve beschreibt.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDEGREETYPE { 
  D3DDEGREE_LINEAR     = 1,
  D3DDEGREE_QUADRATIC  = 2,
  D3DDEGREE_CUBIC      = 3,
  D3DDEGREE_QUINTIC    = 5,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DDEGREETYPE, *LPD3DDEGREETYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DDEGREE_LINEAR"></span><span id="d3ddegree_linear"></span>**D3DDEGREE \_ LINEAR**
</dt> <dd>

Die Kurve wird durch Variablen der ersten Reihenfolge beschrieben.

</dd> <dt>

<span id="D3DDEGREE_QUADRATIC"></span><span id="d3ddegree_quadratic"></span>**D3DDEGREE \_ QUADRATIC**
</dt> <dd>

Die Kurve wird durch Variablen der zweiten Reihenfolge beschrieben.

</dd> <dt>

<span id="D3DDEGREE_CUBIC"></span><span id="d3ddegree_cubic"></span>**D3DDEGREE \_ KUBISCH**
</dt> <dd>

Die Kurve wird durch Variablen der dritten Reihenfolge beschrieben.

</dd> <dt>

<span id="D3DDEGREE_QUINTIC"></span><span id="d3ddegree_quintic"></span>**D3DDEGREE– \_ MICIC**
</dt> <dd>

Die Kurve wird durch Variablen der vierten Reihenfolge beschrieben.

</dd> <dt>

<span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Werte in dieser Enumeration werden verwendet, um die Kurven zu beschreiben, die von Rechteck- und Dreieckspatches verwendet werden. Weitere Informationen finden Sie unter D3DRS \_ CULLMODE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
