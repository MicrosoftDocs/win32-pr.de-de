---
description: Wandelt das Bogenmaß in Grad um.
ms.assetid: 1b19af39-ca23-4364-9121-f532d7fed099
title: D3DXToDegree (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToDegree
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 284e59d8bb0a5b6f866286d67aa8c743716e333333d6c865077ce2cfd51778a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119010"
---
# <a name="d3dxtodegree"></a>D3DXToDegree

Wandelt das Bogenmaß in Grad um.

``` syntax
#define D3DXToDegree(radian) ((radian) * (180.0f / D3DX_PI))
```

## <a name="parameters"></a>Parameter



| Parameter                                                           | Beschreibung                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span id="radian"></span><span id="RADIAN"></span>Radian<br/> | Der Wert im Bogenmaß, der in Grad konvertiert werden soll.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Das Makro gibt den Bogenwert in Grad zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXToRadian**](d3dxtoradian.md)
</dt> <dt>

[D3DX \_ PI](other-d3dx-constants.md)
</dt> </dl>

 

 




