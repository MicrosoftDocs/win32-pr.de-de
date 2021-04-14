---
description: Bestimmt das Punktprodukt von zwei 4D-Vektoren.
ms.assetid: 565dede8-6cc8-4313-9480-2f252cac94f2
title: D3DXVec4Dot-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0ef075a768fe9b70a38a4bc3d88b094359bd546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394149"
---
# <a name="d3dxvec4dot-function"></a>D3DXVec4Dot-Funktion

Bestimmt das Punktprodukt von zwei 4D-Vektoren.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXVec4Dot(
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Das Skalarprodukt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Cross**](d3dxvec4cross.md)
</dt> </dl>

 

 
