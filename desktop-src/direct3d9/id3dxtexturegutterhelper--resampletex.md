---
description: Erstellt eine Textur in der Parametrisierung dieses gutterhelper neu.
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'ID3DXTextureGutterHelper:: resampletex-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219632"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a>ID3DXTextureGutterHelper:: resampletex-Methode

Erstellt eine Textur in der Parametrisierung dieses gutterhelper neu.

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

*ptexturein* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textur, die der ursprünglichen Parametrisierung in pmeshin entspricht. Diese Textur wird zum Erstellen von ptextureout verwendet.

</dd> <dt>

*pmeshat* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Gitter, das die ursprünglichen und neuen parametrizierungen enthält. Die neue Parametrisierung muss in D3DDECLUSAGE \_ texcoord Index 0 gespeichert werden.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Vertex-Datenverwendung (in Kombination mit usageindex verwendet), die die Komponente der Vertex-Deklaration identifiziert, die die ursprüngliche Parametrisierung in pmeshat enthält. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

Start *Index* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

NULL basierter Index (verwendet in Kombination mit der Verwendung), der die Komponente der Vertex-Deklaration identifiziert, die die ursprüngliche Parametrisierung in pmeshat enthält. Die Kombination aus D3DDECLUSAGE \_ texcoord und Index 0 ist für die neue Parametrisierung erforderlich. es kann eine beliebige andere Kombination von Verwendung/Index verwendet werden.

</dd> <dt>

*ptextureout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Textur wird erneut entnommen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Bei einer Parametrisierung im Fall dieser Funktion handelt es sich um einen Satz von Texturkoordinaten, der die Dreiecke eines Netzes den Dreiecken einer Textur zuordnet. Die neue Parametrisierung ist der Satz von Texturkoordinaten, der in der bundbundhilfsschnittstelle enthalten ist, und die ursprüngliche Parametrisierung ist der Satz von Texturkoordinaten, der im Eingabe Mesh enthalten ist.

Es wird davon ausgegangen, dass die Texturkoordinaten zwischen 0 und 1 (einschließlich) liegen, und die neue Parametrisierung muss in der Scheitelpunkt Deklaration als Texturkoordinaten Index 0 deklariert werden. Die ursprüngliche Textur und die neu komprimierte Textur müssen dieselbe Breite und Höhe aufweisen.

So bereiten Sie z. b. die Neuerstellung einer Textur vor:

-   Erstellen Sie die ursprüngliche Textur Schnittstelle (poriginaltex unten), indem Sie eine Funktion wie [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)verwenden.
-   Erstellen Sie die neue Textur Schnittstelle für die neu komprimierte Textur (presampledtex unten). Die Größe dieser Textur muss mit der Größe (Breite und Höhe) der Struktur des bundstehilfsobjekts identisch sein.
-   Rufen Sie [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) auf, um die neue Parametrisierung zu erhalten, wie hier gezeigt:


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



Ein häufiges Szenario ist die Verwendung von uvatlas zum Erstellen eines Textur Atlas und die anschließende erneute Stichprobe der Textur mithilfe von resampletex in die neue Parametrisierung. Weitere Informationen zu Atlases finden Sie unter [Verwenden von uvatlas (Direct3D 9)](using-uvatlas.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> <dt>

[**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)
</dt> </dl>

 

 
