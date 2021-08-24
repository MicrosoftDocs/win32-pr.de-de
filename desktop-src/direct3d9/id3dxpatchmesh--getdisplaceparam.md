---
description: Ruft Gittergeometrieverschiebungsparameter ab.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: ID3DXPatchMesh::GetDisplaceParam-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDisplaceParam
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f079e66f20bfd9b2fab673a0f8c2310a9fd85d84fe4e7d0b8c5ad59d1d61e9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847450"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a>ID3DXPatchMesh::GetDisplaceParam-Methode

Ruft Gittergeometrieverschiebungsparameter ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDisplaceParam(
  [in] LPDIRECT3DBASETEXTURE9 *Texture,
  [in] D3DTEXTUREFILTERTYPE   *MinFilter,
  [in] D3DTEXTUREFILTERTYPE   *MagFilter,
  [in] D3DTEXTUREFILTERTYPE   *MipFilter,
  [in] D3DTEXTUREADDRESS      *Wrap,
  [in] DWORD                  *dwLODBias
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Textur* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

Textur, die die Verschiebungsdaten enthält.

</dd> <dt>

*MinFilter* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Minierungsstufe. Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MagFilter* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Vergrößerungsstufe. Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MipFilter* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

MIP-Filterebene. Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*Umschließen* \[ In\]
</dt> <dd>

Typ: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***

Texturadressen-Wrap-Modus. Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

*dwLODBias* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Wert der Detailvoreingenommenheit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Verschiebungszuordnungen können nur 2D-Texturen sein. Mipmapping wird bei nichtadaptivem Mosaik ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
