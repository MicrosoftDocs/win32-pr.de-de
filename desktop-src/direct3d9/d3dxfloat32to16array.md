---
description: 'D3DXFloat32To16Array-Funktion (D3dx9math.h): Konvertiert ein Array von 32-Bit-Gleitkommaen in 16-Bit-Gleitkommakomma.'
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: D3DXFloat32To16Array-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d4b02a85a22d8490b36ad32511af0d85294045502d4e32ba82b757ac34e21ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027730"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a>D3DXFloat32To16Array-Funktion (D3dx9math.h)

Konvertiert ein Array von 32-Bit-Gleitkommaen in 16-Bit-Gleitkommakomma.

## <a name="syntax"></a>Syntax


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

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

Typ: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

Zeiger auf ein Array von 16-Bit-Gleitkommaen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
