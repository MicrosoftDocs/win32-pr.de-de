---
description: Bestimmt, ob eine Matrix eine Identitätsmatrix ist.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: D3DXMatrixIsIdentity-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 913034d9cf3781dce4bb8c1ee643eac90bd23054300fbaa8b0a55eab62914958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044868"
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

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die auf Identität getestet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Wenn die Matrix eine Identitätsmatrix ist, gibt diese Funktion **TRUE** zurück. Andernfalls gibt diese Funktion **FALSE** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIdentity**](d3dxmatrixidentity.md)
</dt> </dl>

 

 
