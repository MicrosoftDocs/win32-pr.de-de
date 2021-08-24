---
description: Initialisiert eine Farbe mit den angegebenen Rot-, Grün-, Blau- und Alpha-Gleitkommawerten.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: D3DCOLOR_COLORVALUE -Makro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLOR_COLORVALUE
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f4ee10003e0f4fdeae937d8ac786b4d389a91ec0326c2d6288d10af2a63e2286
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751230"
---
# <a name="d3dcolor_colorvalue-macro"></a>D3DCOLOR \_ COLORVALUE-Makro

Initialisiert eine Farbe mit den angegebenen Rot-, Grün-, Blau- und Alpha-Gleitkommawerten.

## <a name="syntax"></a>Syntax


```C++
D3DCOLOR D3DCOLOR_COLORVALUE(
   float r,
   float g,
   float b,
   float a
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*r* 
</dt> <dd>

Rote Komponente der Farbe. Dieser Wert muss ein Gleitkommawert im Bereich von 0,0 bis 1,0 sein.

</dd> <dt>

*g* 
</dt> <dd>

Grüne Komponente der Farbe. Dieser Wert muss ein Gleitkommawert im Bereich von 0,0 bis 1,0 sein.

</dd> <dt>

*b* 
</dt> <dd>

Blaue Komponente der Farbe. Dieser Wert muss ein Gleitkommawert im Bereich von 0,0 bis 1,0 sein.

</dd> <dt>

*Eine* 
</dt> <dd>

Alphakomponente der Farbe. Dieser Wert muss ein Gleitkommawert im Bereich von 0,0 bis 1,0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**D3DCOLOR-Wert**](d3dcolor.md) zurück, der den angegebenen RGBA-Werten entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




