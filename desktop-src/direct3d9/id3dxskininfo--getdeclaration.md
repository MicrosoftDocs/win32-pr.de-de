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
ms.openlocfilehash: 8188094801ed3a9cef4be3c441d6afb5032e86178da50d837017c0836a702c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800950"
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

Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) die das Scheitelpunktformat der Gitternetzvertices beschreiben. Die Obergrenze dieses Deklaratorarrays ist [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md). Das Vertexelementarray endet mit dem [**D3DDECL-END-Makro. \_**](d3ddecl-end.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Das Array von Elementen enthält das [**D3DDECL-END-Makro, \_**](d3ddecl-end.md) das die Deklaration beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo::SetDeclaration**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
