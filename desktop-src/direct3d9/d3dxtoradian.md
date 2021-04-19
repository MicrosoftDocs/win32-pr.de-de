---
description: Wandelt Grad in Bogenmaß um.
ms.assetid: 450806bd-db2f-47be-ae80-c261088b1bb8
title: D3DXToRadian (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToRadian
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: e06184a0d3c654a2c0e82431ff25a339f5682837
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350679"
---
# <a name="d3dxtoradian"></a>D3DXToRadian

Wandelt Grad in Bogenmaß um.

``` syntax
#define D3DXToRadian(degree) ((degree) * (D3DX_PI / 180.0f))
```

## <a name="parameters"></a>Parameter



| Parameter                                                           | BESCHREIBUNG                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span id="degree"></span><span id="DEGREE"></span>theits<br/> | Der Wert in Grad, der in das Bogenmaß konvertiert werden soll.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Das-Makro gibt den Wert für den Grad im Bogenmaß zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Makros](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXToDegree**](d3dxtodegree.md)
</dt> <dt>

[D3DX \_ Pi](other-d3dx-constants.md)
</dt> </dl>

 

 




