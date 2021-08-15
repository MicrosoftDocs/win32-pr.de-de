---
description: Erstellt ein ID3DXTextureGutterHelper-Objekt aus einem Eingabegittermodell und Texturdaten.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: D3DXCreateTextureGutterHelper-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e62f89911199497abfd905376f272121c6c5a9996ec5685e556453bc378e65e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045138"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a>D3DXCreateTextureGutterHelper-Funktion

Erstellt ein [**ID3DXTextureGutterHelper-Objekt**](id3dxtexturegutterhelper.md) aus einem Eingabegittermodell und Texturdaten.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Breite der Textur in Pixel.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Höhe der Textur in Pixel.

</dd> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**EINGABE-ID3DXMesh-Gittermodellobjekt.**](id3dxmesh.md)

</dd> <dt>

*GutterSize* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Anzahl der Texel, nach denen die Textur übersampelt und der Bundstegbereich erstellt werden soll. Muss mindestens 1 sein.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***

Zeiger auf ein [**id3DXTextureGutterHelper-Objekt,**](id3dxtexturegutterhelper.md) das erstellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Verwenden Sie [**D3DXConcatenateMeshes,**](d3dxconcatenatemeshes.md) um eine Szene in neue Koordinaten zu transformieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorausberechnen von Übertragungsfunktionen für Die Radiance](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
