---
description: 'ID3DXSkinInfo::GetDeclaration-Methode: Ruft die Scheitelpunktdeklaration ab.'
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: ID3DXSkinInfo::GetDeclaration-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83554b13fe8e20890b1edecd690c540c2e14d4d7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093138"
---
# <a name="id3dxskininfogetdeclaration-method"></a>ID3DXSkinInfo::GetDeclaration-Methode

Ruft die Scheitelpunktdeklaration ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deklaration* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) die das Scheitelpunktformat der Gitternetzvertices beschreiben. Die Obergrenze dieses Deklaratorarrays ist [**MAX \_ FVF \_ DECL \_ SIZE.**](./max-fvf-decl-size.md) Das Vertexelementarray endet mit dem [**D3DDECL \_ END-Makro.**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Das Array von Elementen enthält das [**D3DDECL \_ END-Makro,**](d3ddecl-end.md) das die Deklaration beendet.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetDeclaration**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
