---
description: 'D3DXMatrixDeterminant-Funktion (D3DX10Math.h): Gibt die Determinante einer Matrix zurück.'
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: D3DXMatrixDeterminant-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce78181cb2fe0c9f2ebeedc18ca57df7429a15d7e18329b511a1a5c0b95c12df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070050"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a>D3DXMatrixDeterminant-Funktion (D3DX10Math.h)

Gibt die Determinante einer Matrix zurück.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die D3DXMATRIX-Quellstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gibt die Determinante der Matrix zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
