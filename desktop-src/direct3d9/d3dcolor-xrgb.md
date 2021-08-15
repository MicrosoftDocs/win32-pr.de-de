---
description: Initialisiert eine Farbe mit den angegebenen Werten für Rot, Grün und Blau.
ms.assetid: 832a4a78-c166-4e45-a907-57730da1c2c8
title: D3DCOLOR_XRGB Makro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_XRGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: a31801236720d0a01eefe7f41ac6bd260c1364bb81c437cf6a85088c1c022b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527600"
---
# <a name="d3dcolor_xrgb-macro"></a>D3DCOLOR \_ XRGB-Makro

Initialisiert eine Farbe mit den angegebenen Werten für Rot, Grün und Blau.

## <a name="syntax"></a>Syntax


```C++
D3DCOLOR D3DCOLOR_XRGB(
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*r* 
</dt> <dd>

Rote Komponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

*g* 
</dt> <dd>

Grüne Komponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

*b* 
</dt> <dd>

Blaue Komponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**D3DCOLOR-Wert**](d3dcolor.md) zurück, der den angegebenen RGB-Werten entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ ARGB**](d3dcolor-argb.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> </dl>

 

 




