---
description: 'D3DXFloat16To32Array-Funktion (D3dx9math.h): Konvertiert ein Array von 16-Bit-Gleitkommaen in 32-Bit-Gleitkommakomma.'
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: D3DXFloat16To32Array-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 4c5ce94dcadac8952792e31b51ad84fc2326668500c625728a0af5fd985f1d31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118526037"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a>D3DXFloat16To32Array-Funktion (D3dx9math.h)

Konvertiert ein Array von 16-Bit-Gleitkommaen in 32-Bit-Gleitkommakomma.

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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf das Array von 32-Bit-Gleitkommaen.

</dd> <dt>

*pIn* \[ In\]
</dt> <dd>

Typ: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***

Zeiger auf ein Array von 16-Bit-Gleitkommaen.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von 32-Bit-Gleitkommaen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
