---
description: Wandelt das Bogenmaß in Grad um.
ms.assetid: 1b19af39-ca23-4364-9121-f532d7fed099
title: D3DXToDegree (D3dx9math. h)
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
ms.openlocfilehash: ad77ea661f4d67318566079aa7c1072fe0f86c91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355005"
---
# <a name="d3dxtodegree"></a>D3DXToDegree

Wandelt das Bogenmaß in Grad um.

``` syntax
#define D3DXToDegree(radian) ((radian) * (180.0f / D3DX_PI))
```

## <a name="parameters"></a>Parameter



| Parameter                                                           | BESCHREIBUNG                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span id="radian"></span><span id="RADIAN"></span>Bogenmaß Wert<br/> | Der Wert im Bogenmaß, der in Grad konvertiert werden soll.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Das-Makro gibt den Bogenmaß Wert-Wert in Grad zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXToRadian**](d3dxtoradian.md)
</dt> <dt>

[D3DX \_ Pi](other-d3dx-constants.md)
</dt> </dl>

 

 




