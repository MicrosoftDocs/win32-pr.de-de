---
description: Bestimmt, ob eine Quaternion eine Identitäts quaternion ist.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: D3DXQuaternionIsIdentity-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b34debbe70ec6edcd3f08a1ec83383335a0d4f97801d122bc1bd73a82a81ff36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731592"
---
# <a name="d3dxquaternionisidentity-function"></a>D3DXQuaternionIsIdentity-Funktion

Bestimmt, ob eine Quaternion eine Identitäts quaternion ist.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pQ* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die auf Identität getestet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Wenn die Quaternion eine Identitäts quaternion ist, gibt diese Funktion **TRUE** zurück. Andernfalls gibt diese Funktion **FALSE** zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
</dt> </dl>

 

 
