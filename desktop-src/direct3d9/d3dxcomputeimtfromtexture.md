---
description: Berechnet pro Dreieck IMT aus einer Textur, die einem Gitternetz zugeordnet ist und optional als Eingabe für die D3DX UVAtlas-Funktionen verwendet werden soll.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: D3DXComputeIMTFromTexture-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c0fb2de39cfcc8b0571b05c85ffa3d03945f6c837ae10ba68252b5b9c24b524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299373"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>D3DXComputeIMTFromTexture-Funktion

Berechnet pro Dreieck-IMT aus einer Textur, die einem Gitternetz zugeordnet ist und optional als Eingabe für die D3DX [UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ein Zeiger auf ein Eingabegittermodell (siehe [**ID3DXMesh),**](id3dxmesh.md)das die Objektgeometrie zum Berechnen des IMT enthält.

</dd> <dt>

*pTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ein Zeiger auf die Textur (siehe [**IDirect3DTexture9),**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)die dem Gitternetz zugeordnet ist.

</dd> <dt>

*dwTextureIndex* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Nullbasierter Texturkoordinatenindex, der angibt, welche Menge von Texturkoordinaten verwendet werden soll.

</dd> <dt>

*dwOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Texturumbruchoptionen. Dies ist eine Kombination aus einem oder mehreren [**D3DXIMT-FLAGS.**](./d3dximt-flags.md)

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Typ: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Ein Zeiger auf eine Rückruffunktion zum Überwachen des IMT-Berechnungsfortschritts.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine benutzerdefinierte Variable, die an die Statusrückruffunktion übergeben wird. Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

</dd> <dt>

*ppIMTData* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ein Zeiger auf den Puffer (siehe [**ID3DXBuffer),**](id3dxbuffer.md)der das zurückgegebene IMT-Array enthält. Dieses Array kann als Eingabe für die D3DX [UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md) bereitgestellt werden, um die Texturraumzuordnung in der Texturparametrisierung zu priorisieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Andernfalls ist der Wert D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Bei einer Textur, die der Oberfläche des Gitternetzes zugeordnet ist, berechnet der Algorithmus den IMT für jedes Gesicht. Dies führt dazu, dass Dreiecke, die Signaldaten mit niedrigerer Frequenz enthalten, weniger Platz im endgültigen Texturat atlas einnehmen, wenn sie mit den UVAtlas-Funktionen parametrisiert werden. Es wird davon ausgegangen, dass die Textur bilinear über das Gitternetz interpoliert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[UVAtlas-Funktionen](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Verwenden von UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
