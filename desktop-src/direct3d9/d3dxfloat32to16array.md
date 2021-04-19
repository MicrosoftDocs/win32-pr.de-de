---
description: Konvertiert ein Array von 32-Bit-Gleit Komma Zahlen in 16-Bit-Gleit Komma Zahlen.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: D3DXFloat32To16Array-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 360aebd5dd1af45fdc6fb5b9c23c514252f0ccf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371914"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a>D3DXFloat32To16Array-Funktion (D3dx9math. h)

Konvertiert ein Array von 32-Bit-Gleit Komma Zahlen in 16-Bit-Gleit Komma Zahlen.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

Zeiger auf das Array von 16-Bit-Gleit Komma Zahlen.

</dd> <dt>

*pIn* \[ in\]
</dt> <dd>

Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von 32-Bit-Gleit Komma Zahlen.

</dd> <dt>

*n* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Elemente im Array.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***

Zeiger auf ein Array von 16-Bit-Gleit Komma Zahlen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
