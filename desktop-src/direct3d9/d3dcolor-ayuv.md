---
description: Initialisiert eine Farbe mithilfe der (a,y,u,v)-Werte.
ms.assetid: 47b65aab-511a-44c1-ab94-973bc2da7e04
title: D3DCOLOR_AYUV Makro (D3d9types.h)
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
ms.openlocfilehash: 5e1900bf0d400971786eb37dd5138154913562982e1a1e3221c8002ac51fbf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300314"
---
# <a name="d3dcolor_ayuv-macro"></a>\_D3DCOLOR-AYUV-Makro

Initialisiert eine Farbe mithilfe der (a,y,u,v)-Werte.

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

*Eine* 
</dt> <dd>

Alphakomponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

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

Gibt den [D3DCOLOR-Wert](d3dcolor.md) zurück, der den angegebenen ARGB-Werten entspricht.

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

[**D3DCOLOR \_ XYUV**](d3dcolor-xyuv.md)
</dt> </dl>

 

 




