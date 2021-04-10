---
description: Mit dieser Methode kann der Benutzer die Mesh-Deklaration ändern, ohne das Datenlayout des Vertexpuffers zu ändern. Der-Rückruf ist nur gültig, wenn die alten und neuen Deklarations Formate die gleiche Scheitelpunkt Größe aufweisen.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'ID3DXBaseMesh:: updatesemantics-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050869"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a>ID3DXBaseMesh:: updatesemantics-Methode

Mit dieser Methode kann der Benutzer die Mesh-Deklaration ändern, ohne das Datenlayout des Vertexpuffers zu ändern. Der-Rückruf ist nur gültig, wenn die alten und neuen Deklarations Formate die gleiche Scheitelpunkt Größe aufweisen.

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

Ein Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, das das Scheitelpunkt Format der mesvertices beschreibt. Die Obergrenze dieses deklaratorarrays ist [**Max \_ \_ \_**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

[**ID3DXBaseMesh:: clonemesh**](id3dxbasemesh--clonemesh.md) dient zum erneuten Formatieren und Ändern des Vertex-Daten Layouts. Verwenden Sie es z. b. zum Hinzufügen von Platz für normale, Texturkoordinaten, Farben, Gewichtungen usw., die zuvor nicht vorhanden waren.

**ID3DXBaseMesh:: updatesemantics** ist eine Methode zum Aktualisieren der Scheitelpunkt Deklaration mit unterschiedlichen Semantik Informationen, ohne das Layout des Vertexpuffers zu ändern. Verwenden Sie diese z. b., um eine 3D-Textur Koordinate als Binormal oder Tangens neu zu bezeichnen (oder umgekehrt).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXBaseMesh:: clonemeshf VF**](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
