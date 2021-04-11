---
description: Konvertiert ein Array von 16-Bit-Gleit Komma Zahlen in 32-Bit-Gleit Komma Zahlen.
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: D3DXFloat16To32Array-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a813553234c9e59ad34720da6f380977779e5d96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354987"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a>D3DXFloat16To32Array-Funktion (D3DX10Math. h)

Konvertiert ein Array von 16-Bit-Gleit Komma Zahlen in 32-Bit-Gleit Komma Zahlen.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Ein Zeiger auf das Array von 32-Bit-Gleit Komma Zahlen.

</dd> <dt>

*pIn* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***

Zeiger auf ein Array von 16-Bit-Gleit Komma Zahlen.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von 32-Bit-Gleit Komma Zahlen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
