---
description: Konvertiert ein Array von 16-Bit-Gleit Komma Zahlen in 32-Bit-Gleit Komma Zahlen.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: D3DXFloat16To32Array-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6760ce36341883c26030df91d3d46b5b21fdb012
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355011"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a>D3DXFloat16To32Array-Funktion (D3dx9math. h)

Konvertiert ein Array von 16-Bit-Gleit Komma Zahlen in 32-Bit-Gleit Komma Zahlen.

## <a name="syntax"></a>Syntax


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Ein Zeiger auf das Array von 32-Bit-Gleit Komma Zahlen.

</dd> <dt>

*pIn* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXFLOAT16**](d3dxfloat16.md) \***

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
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
