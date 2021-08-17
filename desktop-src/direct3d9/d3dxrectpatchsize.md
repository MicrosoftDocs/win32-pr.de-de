---
description: Ruft die Größe des Rechteckpatches ab.
ms.assetid: d25373ef-789d-4515-83da-7049f040c9a4
title: D3DXRectPatchSize-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRectPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 51b00ab5ffcd0fa88d3523412c0f340404bbdd782bed6f3f01e1b5f7ee1ca91b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460120"
---
# <a name="d3dxrectpatchsize-function"></a>D3DXRectPatchSize-Funktion

Ruft die Größe des Rechteckpatches ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXRectPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pwdVertices
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfNumSegs* \[ In\]
</dt> <dd>

Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Anzahl der Segmente pro Edge, für die ein Mosaik zu erstellen ist.

</dd> <dt>

*pdwTriangles* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein DWORD, das die Anzahl der Dreiecke im Patch enthält.

</dd> <dt>

*pwdVertices* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein DWORD, das die Anzahl der Scheitelpunkte im Patch enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meshfunktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
