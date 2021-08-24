---
description: Mit dieser Methode kann der Benutzer die Gitternetzdeklaration ändern, ohne das Datenlayout des Scheitelpunktpuffers zu ändern. Der Aufruf ist nur gültig, wenn das alte und das neue Deklarationsformat die gleiche Scheitelpunktgröße aufweisen.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: ID3DXBaseMesh::UpdateSemantics-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a9a628c16e7f4a26db9953298be1adcba2cef364153d4bb2e6b29dbc4d9ef83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607320"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>ID3DXBaseMesh::UpdateSemantics-Methode

Mit dieser Methode kann der Benutzer die Gitternetzdeklaration ändern, ohne das Datenlayout des Scheitelpunktpuffers zu ändern. Der Aufruf ist nur gültig, wenn das alte und das neue Deklarationsformat die gleiche Scheitelpunktgröße aufweisen.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deklaration* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Ein Array von [**D3DVERTEXELEMENT9-Elementen,**](d3dvertexelement9.md) das das Scheitelpunktformat der Netzvertices beschreibt. Die Obergrenze dieses Deklaratorarrays ist [**MAX \_ FVF \_ DECL \_ SIZE**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) wird verwendet, um das Vertexdatenlayout neu zu formatiert und zu ändern. Verwenden Sie es beispielsweise, um Platz für Normalitäten, Texturkoordinaten, Farben, Gewichtungen usw. hinzuzufügen, die zuvor nicht vorhanden waren.

**ID3DXBaseMesh::UpdateSemantics** ist eine Methode zum Aktualisieren der Scheitelpunktdeklaration mit anderen semantischen Informationen, ohne das Layout des Scheitelpunktpuffers zu ändern. Verwenden Sie sie beispielsweise, um eine 3D-Texturkoordinate als binormal oder Tangens neu zu bezeichnen oder umgekehrt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh::CloneMeshFVF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
