---
description: Bestimmt, ob eine Matrix eine Identitätsmatrix ist.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: D3DXMatrixIsIdentity-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355436"
---
# <a name="d3dxmatrixisidentity-function"></a>D3DXMatrixIsIdentity-Funktion

Bestimmt, ob eine Matrix eine Identitätsmatrix ist.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pm* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die auf die Identität getestet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Wenn die Matrix eine Identitätsmatrix ist, gibt diese Funktion " **true**" zurück. Andernfalls gibt diese Funktion **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIdentity**](d3dxmatrixidentity.md)
</dt> </dl>

 

 
