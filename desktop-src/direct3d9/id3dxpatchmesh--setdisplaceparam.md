---
description: Legt Gittergeometrieverschiebungsparameter fest.
ms.assetid: 4c78e5b3-fb63-4341-a811-5531cf9564e7
title: ID3DXPatchMesh::SetDisplaceParam-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.SetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 84445c3d18fa38bbeff4085c6da1fda191bb6ca5bbe147c17f3f5f8769d2a63d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629200"
---
# <a name="id3dxpatchmeshsetdisplaceparam-method"></a>ID3DXPatchMesh::SetDisplaceParam-Methode

Legt Gittergeometrieverschiebungsparameter fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 Texture,
  [in] D3DTEXTUREFILTERTYPE   MinFilter,
  [in] D3DTEXTUREFILTERTYPE   MagFilter,
  [in] D3DTEXTUREFILTERTYPE   MipFilter,
  [in] D3DTEXTUREADDRESS      Wrap,
  [in] DWORD                  dwLODBias
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Textur* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**

Textur, die die Verschiebungsdaten enthält.

</dd> <dt>

*MinFilter* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Minification level ( Minification-Ebene). Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*MagFilter* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Vergrößerungsstufe. Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)**

Mip-Filterebene. Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE.**](./d3dtexturefiltertype.md)

</dd> <dt>

*Umschließen* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)**

Texturadressumbruchmodus. Weitere Informationen finden Sie unter [ **D3DTEXTUREADDRESS.**](./d3dtextureaddress.md)

</dd> <dt>

*dwLODBias* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Ebene des Detailabweichungswerts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Verschiebungskarten können nur 2D-Texturen sein. Mipmapping wird für nichtadaptive Mosaike ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
