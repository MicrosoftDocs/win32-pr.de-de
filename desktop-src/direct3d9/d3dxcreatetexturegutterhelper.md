---
description: Erstellt ein ID3DXTextureGutterHelper-Objekt aus einem eingabemesh und Textur Daten.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: D3DXCreateTextureGutterHelper-Funktion (D3DX9Mesh. h)
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
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353729"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a>D3DXCreateTextureGutterHelper-Funktion

Erstellt ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt aus einem eingabemesh und Textur Daten.

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

*Breite* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Breite der Textur in Pixel.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Höhe der Textur in Pixel.

</dd> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Eingabe Objekt.

</dd> <dt>

*Guttersize* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Anzahl von texeln, nach denen die Textur über Stichprobe und der bundlockbereich erstellt werden soll. Muss mindestens 1 sein.

</dd> <dt>

*ppbuffer* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***

Zeiger auf ein [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) -Objekt, das erstellt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert eines der folgenden Werte sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) , um eine Szene in neue Koordinaten umzuwandeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
