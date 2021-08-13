---
description: Initialisiert eine Farbe mit den Werten (y, u, v).
ms.assetid: e3091eaf-8639-428c-8dd8-6feeb7d7776e
title: D3DCOLOR_XYUV Makro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XYUV
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: caa6bc1eb9586c1526a7af674040fd703ff0a75a5055ce42e13378206e82c879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300324"
---
# <a name="d3dcolor_xyuv-macro"></a>\_D3DCOLOR-XYUV-Makro

Initialisiert eine Farbe mit den Werten (y, u, v).

## <a name="syntax"></a>Syntax


```C++
D3DCOLOR D3DCOLOR_XYUV(
   int y,
   int u,
   int v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*y* 
</dt> <dd>

Leuchtdichtekomponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

*n* 
</dt> <dd>

Blaue Helligkeit der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

*V* 
</dt> <dd>

Rote Helligkeit der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**D3DCOLOR-Wert**](d3dcolor.md) zurück, der den angegebenen Werten (y, u, v) entspricht.

## <a name="remarks"></a>Hinweise

Eine RGB-Farbe kann durch Konvertierung in Leuchtdichte und Farbunterschiede mit den folgenden Gleichungen auf 16 Bits pro Pixel reduziert werden:


```C++
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ AYUV**](d3dcolor-ayuv.md)
</dt> </dl>

 

 




