---
description: Definiert den Prioritätstyp, dem eine Animationsspur zugewiesen wird.
ms.assetid: 7bd83e31-09c4-4376-a22d-ed8023b78e84
title: D3DXPRIORITY_TYPE -Enumeration (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPRIORITY_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: e7ea5b7447b896c6b582280216af4d6c05cc540286ad31a2bfb337975fe6c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524849"
---
# <a name="d3dxpriority_type-enumeration"></a>D3DXPRIORITY \_ TYPE-Enumeration

Definiert den Prioritätstyp, dem eine Animationsspur zugewiesen wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXPRIORITY_TYPE { 
  D3DXPRIORITY_LOW          = 0,
  D3DXPRIORITY_HIGH         = 1,
  D3DXPRIORITY_FORCE_DWORD  = 0x7fffffff
} D3DXPRIORITY_TYPE, *LPD3DXPRIORITY_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXPRIORITY_LOW"></span><span id="d3dxpriority_low"></span>**D3DXPRIORITY \_ LOW**
</dt> <dd>

Die Spur sollte mit allen Spuren mit niedriger Priorität kombiniert werden, bevor die Mischung mit niedriger Priorität mit der Mischung mit hoher Priorität kombiniert wird.

</dd> <dt>

<span id="D3DXPRIORITY_HIGH"></span><span id="d3dxpriority_high"></span>**D3DXPRIORITY \_ HIGH**
</dt> <dd>

Die Spur sollte mit allen Titeln mit hoher Priorität kombiniert werden, bevor die Mischung mit hoher Priorität mit der Mischung mit niedriger Priorität kombiniert wird.

</dd> <dt>

<span id="D3DXPRIORITY_FORCE_DWORD"></span><span id="d3dxpriority_force_dword"></span>**D3DXPRIORITY \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Spuren mit der gleichen Priorität werden kombiniert, und die beiden resultierenden Werte werden dann mithilfe des Prioritätsmischungsfaktors kombiniert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




