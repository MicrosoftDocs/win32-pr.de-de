---
description: Definiert den Komprimierungsmodus, der zum Speichern komprimierter Animationssatzdaten verwendet wird.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: D3DXCOMPRESSION_FLAGS -Enumeration (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: a4d1e19e2e6fb8e0625b20c7755b3cf3b5c68c06cbc01da1b8a22fd9893d0027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299998"
---
# <a name="d3dxcompression_flags-enumeration"></a>D3DXCOMPRESSION \_ FLAGS-Enumeration

Definiert den Komprimierungsmodus, der zum Speichern komprimierter Animationssatzdaten verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ DEFAULT**
</dt> <dd>

Implementiert eine schnelle Komprimierung.

</dd> <dt>

<span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ STRONG**
</dt> <dd>

Implementiert langsame Komprimierung. Führt in der Regel zu einem komprimierten Animationssatz mit besserer Qualität als bei Verwendung von D3DXCOMPRESS \_ DEFAULT.

</dd> <dt>

<span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




