---
description: Resamples für eine Textur in die Parametrisierung dieses Gutterhelpers.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: ID3DXTextureGutterHelper::ResampleTex-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7d3afe8155eb33a37b30abcfc96aae83c0a96461c1ee2dd6118a671701cfed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800319"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>ID3DXTextureGutterHelper::ResampleTex-Methode

Resamples für eine Textur in die Parametrisierung dieses Gutterhelpers.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTextureIn* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textur, die der ursprünglichen Parametrisierung in pMeshIn entspricht. Diese Textur wird zum Erstellen von pTextureOut verwendet.

</dd> <dt>

*pMeshIn* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Mesh, das die ursprünglichen und neuen Parametrisierungen enthält. Die neue Parametrisierung muss im D3DDECLUSAGE \_ TEXCOORD-Index 0 gespeichert werden.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Vertexdatenverwendung (in Kombination mit UsageIndex), die die Komponente der Scheitelpunktdeklaration identifiziert, die die ursprüngliche Parametrisierung in pMeshIn enthält. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndex* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Nullbasierter Index (wird in Kombination mit Usage verwendet), der die Komponente der Scheitelpunktdeklaration identifiziert, die die ursprüngliche Parametrisierung in pMeshIn enthält. Die Kombination aus D3DDECLUSAGE TEXCOORD und Index 0 ist für die neue Parametrisierung erforderlich. Es kann jede andere Kombination aus Verwendung und \_ Index verwendet werden.

</dd> <dt>

*pTextureOut* \[ out\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Resampled-Textur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Eine Parametrisierung im Fall dieser Funktion ist eine Reihe von Texturkoordinaten, die die Dreiecke eines Gitters den Dreiecken einer Textur zustellen. Bei der neuen Parametrisierung handelt es sich um den Satz von Texturkoordinaten, die in der Bundsten-Hilfsschnittstelle enthalten sind, und die ursprüngliche Parametrisierung ist der Satz von Texturkoordinaten, die im Eingabegitternetz enthalten sind.

Es wird davon ausgegangen, dass Texturkoordinaten zwischen 0 und 1 (einschließlich) liegen, und die neue Parametrisierung muss in der Scheitelpunktdeklaration als Texturkoordinatenindex 0 deklariert werden. Die ursprüngliche Textur und die Neusampledertextur müssen die gleiche Breite und Höhe aufweisen.

So bereiten Sie beispielsweise das Resampling einer Textur vor:

-   Erstellen Sie die ursprüngliche Texturschnittstelle (pOriginalTex unten) mithilfe einer Funktion wie [**D3DXCreateTextureFromFile.**](d3dxcreatetexturefromfile.md)
-   Erstellen Sie die neue Texturschnittstelle für die Neusampledtextur (pResampledTex unten). Die Größe dieser Textur muss mit der Größe (Breite und Höhe) der Textur des Bundster-Hilfsers übereinstimmen.
-   Rufen [**Sie D3DXCreateTextureGutterHelper auf,**](d3dxcreatetexturegutterhelper.md) um die neue Parametrisierung wie hier gezeigt zu erhalten:


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



Ein häufiges Szenario ist die Verwendung von UVAtlas zum Erstellen eines Texturatlas und anschließendes Verwenden von ResampleTex, um die Textur in die neue Parametrisierung neu zu sampeln. Weitere Informationen zu Atlass finden Sie unter [Verwenden von UVAtlas (Direct3D 9).](using-uvatlas.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
