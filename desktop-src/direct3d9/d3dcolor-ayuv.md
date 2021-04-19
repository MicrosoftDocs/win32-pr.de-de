---
description: Initialisiert eine Farbe mit den Werten (a, y, u, v).
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: D3DCOLOR_AYUV-Makro (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_AYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 62a34e94fbdc6c47ed034a46bdae6e9b32a7c95d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355168"
---
# <a name="d3dcolor_ayuv-macro"></a>D3DCOLOR \_ ayuv-Makro

Initialisiert eine Farbe mit den Werten (a, y, u, v).

## <a name="syntax"></a>Syntax


```C++
D3DCOLOR D3DCOLOR_AYUV(
   int a,
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ein* 
</dt> <dd>

Alpha Komponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

*y* 
</dt> <dd>

Die Leuchtkraft Komponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

*n* 
</dt> <dd>

Blaue Helligkeit der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

*Ramelow* 
</dt> <dd>

Rote Helligkeit der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [D3DCOLOR](d3dcolor.md) -Wert zurück, der den angegebenen ARGB-Werten entspricht.

## <a name="remarks"></a>Bemerkungen

Eine RGB-Farbe kann auf 16 Bits pro Pixel reduziert werden, indem Sie in Leuchtkraft-und Farbunterschiede mit den folgenden Gleichungen konvertiert wird:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




