---
description: Initialisiert eine Farbe mit den angegebenen Alpha-, Rot-, Grün- und Blauwerten.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: D3DCOLOR_ARGB Makro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_ARGB
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 8b65ae82673e98d666754ae42348cb62b3c336a1e642a5f78607924dc58313dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805430"
---
# <a name="d3dcolor_argb-macro"></a>D3DCOLOR \_ ARGB-Makro

Initialisiert eine Farbe mit den angegebenen Alpha-, Rot-, Grün- und Blauwerten.

## <a name="syntax"></a>Syntax


```C++
D3DCOLOR D3DCOLOR_ARGB(
   int a,
   int r,
   int g,
   int b
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eine* 
</dt> <dd>

Alphakomponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

</dd> <dt>

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

Gibt den [D3DCOLOR-Wert](d3dcolor.md) zurück, der den angegebenen ARGB-Werten entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> <dt>

[**D3DCOLOR \_ XRGB**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




