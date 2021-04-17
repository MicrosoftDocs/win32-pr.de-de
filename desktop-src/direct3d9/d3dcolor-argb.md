---
description: Initialisiert eine Farbe mit den angegebenen Alpha-, rot-, grün-und blauen Werten.
ms.assetid: e862ba1b-fdcf-4058-8835-e58b4fc5e21a
title: D3DCOLOR_ARGB-Makro (D3d9types. h)
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
ms.openlocfilehash: bd0138c435c15c0c2ac026487471554e0edf0afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354426"
---
# <a name="d3dcolor_argb-macro"></a>D3DCOLOR \_ ARGB-Makro

Initialisiert eine Farbe mit den angegebenen Alpha-, rot-, grün-und blauen Werten.

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

*ein* 
</dt> <dd>

Alpha Komponente der Farbe. Dieser Wert muss zwischen 0 und 255 liegen.

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

Gibt den [D3DCOLOR](d3dcolor.md) -Wert zurück, der den angegebenen ARGB-Werten entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md)
</dt> <dt>

[**D3DCOLOR \_ xrgb**](d3dcolor-xrgb.md)
</dt> </dl>

 

 




