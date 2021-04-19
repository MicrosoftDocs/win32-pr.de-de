---
description: Ruft Mesh-Geometrie-Verschiebungs Parameter ab.
ms.assetid: 155724ba-71be-4e9f-8c84-bb04f8eec578
title: 'ID3DXPatchMesh:: getverdräneparam-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 3ce6891af8a15aa8f4af5c85312f124db6c05321
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369342"
---
# <a name="id3dxpatchmeshgetdisplaceparam-method"></a>ID3DXPatchMesh:: getverdräneparam-Methode

Ruft Mesh-Geometrie-Verschiebungs Parameter ab.

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

*Textur* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***

Textur, die die Verschiebungs Daten enthält.

</dd> <dt>

*MinFilter* \[ in\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Minizierungsebene. Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MagFilter* \[ in\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

Vergrößerungs Stufe. Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

*MipFilter* \[ in\]
</dt> <dd>

Typ: **[ **D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md)\***

MIP-Filter Ebene. Weitere Informationen finden Sie unter [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).

</dd> <dt>

 Umbruch \[ in\]
</dt> <dd>

Typ: **[ **D3DTEXTUREADDRESS**](./d3dtextureaddress.md)\***

Der Textur Adress Umbruch Modus. Weitere Informationen finden Sie unter [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).

</dd> <dt>

*dwlodbias* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Grad des Detail-Bias-Werts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Verschiebungs Zuordnungen können nur 2D-Texturen sein. Mipmapping wird für nicht Adaptive Mosaik ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
