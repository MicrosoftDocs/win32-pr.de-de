---
description: Ruft eine Deklaration ab, die die Scheitel Punkte im Mesh beschreibt.
ms.assetid: e9028282-acf1-4ca4-8af0-7fb655dcb5d1
title: 'ID3DXBaseMesh:: getDeclaration-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 34f8736e822bfe4a959f35f60bb79783e79f2d52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371877"
---
# <a name="id3dxbasemeshgetdeclaration-method"></a>ID3DXBaseMesh:: getDeclaration-Methode

Ruft eine Deklaration ab, die die Scheitel Punkte im Mesh beschreibt.

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

Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format der Mesh-Scheitel Punkte beschreiben. Die Obergrenze dieses deklaratorarrays ist [**Max \_ \_ \_**](./max-fvf-decl-size.md). Das Vertex-Element Array endet mit dem [**D3DDECL \_ End**](d3ddecl-end.md) -Makro.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Das Array von-Elementen enthält das [**D3DDECL \_ End**](d3ddecl-end.md) -Makro, das die Deklaration beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
