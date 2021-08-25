---
description: 'D3DXFloat32To16Array-Funktion (D3DX10Math.h): Konvertiert ein Array von 32-Bit-Gleitkommaen in 16-Bit-Gleitkommakomma.'
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: D3DXFloat32To16Array-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f0de2e2cda9724a5bfa12d13171276694bcd8fbcbbd5dffbb81ae185ebbda381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853410"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a>D3DXFloat32To16Array-Funktion (D3DX10Math.h)

Konvertiert ein Array von 32-Bit-Gleitkommaen in 16-Bit-Gleitkommakomma.

## <a name="syntax"></a>Syntax


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ In\]
</dt> <dd>

Typ: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Zeiger auf das Array von 16-Bit-Gleitkommaen.

</dd> <dt>

*pIn* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von 32-Bit-Gleitkommaen.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***

Zeiger auf ein Array von 16-Bit-Gleitkommaen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
