---
description: 'D3DXFloat16To32Array-Funktion (D3DX10Math.h): Konvertiert ein Array von 16-Bit-Gleitkommadaten in 32-Bit-Gleitkomma.'
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: D3DXFloat16To32Array-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 00e5b7847e89687cf0b9414d3845652c0943661a2fc801fd4016eb54a8677c91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677750"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a>D3DXFloat16To32Array-Funktion (D3DX10Math.h)

Konvertiert ein Array von 16-Bit-Gleitkommadaten in 32-Bit-Gleitkomma.

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

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf das Array von 32-Bit-Gleitkommadaten.

</dd> <dt>

*pIn* \[ In\]
</dt> <dd>

Typ: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***

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



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
