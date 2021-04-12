---
description: Gibt das Punktprodukt von zwei Quaternionen zurück.
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: D3DXQuaternionDot-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355517"
---
# <a name="d3dxquaterniondot-function"></a>D3DXQuaternionDot-Funktion

Gibt das Punktprodukt von zwei Quaternionen zurück.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pQ1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.

</dd> <dt>

*pQ2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Das Punktprodukt von zwei Quaternionen.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
