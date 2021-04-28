---
description: 'D3DXFloat16To32Array-Funktion (D3dx9math.h): Konvertiert ein Array von 16-Bit-Gleitkommadaten in 32-Bit-Gleitkomma.'
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
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107598"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a>D3DXFloat16To32Array-Funktion (D3dx9math.h)

Konvertiert ein Array von 16-Bit-Gleitkommadaten in 32-Bit-Gleitkommadaten.

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

Zeiger auf das Array von 32-Bit-Gleitkommadaten.

</dd> <dt>

*pIn* \[ In\]
</dt> <dd>

Typ: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***

Zeiger auf ein Array von 16-Bit-Gleitkommadaten.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von 32-Bit-Gleitkommadaten.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
