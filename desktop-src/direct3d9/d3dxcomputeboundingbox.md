---
description: Berechnet ein gerichtetes Begrenzungsfeld für eine Koordinatenachse.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: D3DXComputeBoundingBox-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df0376428153cfc02e499c9e26226cce81154023
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219555"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a>D3DXComputeBoundingBox-Funktion (D3DX9Mesh. h)

Berechnet ein gerichtetes Begrenzungsfeld für eine Koordinatenachse.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfirsich Position* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf die erste Position.

</dd> <dt>

*Numvertices* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Scheitel Punkte.

</dd> <dt>

*dwstride* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl oder Anzahl von Bytes zwischen Scheitel Punkten.

</dd> <dt>

*Pmin* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ein Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die zurückgegebene untere linke Ecke des umgebenden Felds beschreibt. Siehe Hinweise.

</dd> <dt>

*pmax* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die zurückgegebene obere rechte Ecke des Begrenzungs Rahmens beschreibt. Siehe Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
