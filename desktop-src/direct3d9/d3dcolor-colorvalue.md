---
description: Initialisiert eine Farbe mit den angegebenen Gleit Komma Werten für Rot, grün, blau und alpha.
ms.assetid: 61825e33-4150-47cd-97f2-2144434a45e2
title: D3DCOLOR_COLORVALUE-Makro (D3d9types. h)
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
ms.openlocfilehash: 3d5bb780a5999d8931335da1e9f49ad8af88dc12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761955"
---
# <a name="d3dcolor_colorvalue-macro"></a>D3DCOLOR \_ ColorValue-Makro

Initialisiert eine Farbe mit den angegebenen Gleit Komma Werten für Rot, grün, blau und alpha.

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

Rote Komponente der Farbe. Dieser Wert muss ein Gleit Komma Wert im Bereich zwischen 0,0 und 1,0 sein.

</dd> <dt>

*g* 
</dt> <dd>

Grüne Komponente der Farbe. Dieser Wert muss ein Gleit Komma Wert im Bereich zwischen 0,0 und 1,0 sein.

</dd> <dt>

*b* 
</dt> <dd>

Blaue Komponente der Farbe. Dieser Wert muss ein Gleit Komma Wert im Bereich zwischen 0,0 und 1,0 sein.

</dd> <dt>

*ein* 
</dt> <dd>

Alpha Komponente der Farbe. Dieser Wert muss ein Gleit Komma Wert im Bereich zwischen 0,0 und 1,0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**D3DCOLOR**](d3dcolor.md) -Wert zurück, der den angegebenen RGBA-Werten entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




