---
description: Ruft die Vertex-Deklaration ab.
ms.assetid: 53ff2fb5-68b6-4edd-b48f-e06df306ee3f
title: 'ID3DXPatchMesh:: getDeclaration-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d2d39192368fdca8ccaba7c51e64f60ea030568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356086"
---
# <a name="id3dxpatchmeshgetdeclaration-method"></a>ID3DXPatchMesh:: getDeclaration-Methode

Ruft die Vertex-Deklaration ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeclaration(
  [out] LPD3DVERTEXELEMENT9 pDeclaration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdeclaration* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format der Mesh-Scheitel Punkte beschreiben. Die Dimension dieses deklaratorarrays ist die [**Maximale Anzahl von \_ SVF- \_ decls \_**](./max-fvf-decl-size.md). Das Vertex-Element Array endet mit dem [**D3DDECL \_ End**](d3ddecl-end.md) -Makro.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Das Array von-Elementen enthält das [**D3DDECL \_ End**](d3ddecl-end.md) -Makro, das die Deklaration beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
