---
description: Klont ein Mesh mit einem flexiblen Scheitelpunkt Formatierungs Code (FVF).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'ID3DXBaseMesh:: clonemeschf VF-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355804"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a>ID3DXBaseMesh:: clonemeschf VF-Methode

Klont ein Mesh mit einem flexiblen Scheitelpunkt Formatierungs Code (FVF).

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [**D3DXMESH**](./d3dxmesh.md) -Flags, die Erstellungs Optionen für das Mesh angeben.

</dd> <dt>

*F-VF* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination von f-Codes, die das Scheitelpunkt Format für die Scheitel Punkte im Ausgabe Mesh angibt. Die Werte der Codes finden Sie unter [D3DFVF](d3dfvf.md).

</dd> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ein Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das dem Mesh zugeordnete Geräte Objekt darstellt.

</dd> <dt>

*ppclonemesh* \[ Out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das geklonte Mesh darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

**ID3DXBaseMesh:: clonemeschfvf** dient zum erneuten Formatieren und Ändern des Vertex-Daten Layouts. Dies erfolgt durch Erstellen eines neuen Mesh-Objekts. Verwenden Sie es z. b. zum Hinzufügen von Platz für normale, Texturkoordinaten, Farben, Gewichtungen usw., die zuvor nicht vorhanden waren.

[**ID3DXBaseMesh:: updatesemantics**](id3dxbasemesh--updatesemantics.md) aktualisiert die Vertex-Deklaration mit anderen Semantik Informationen, ohne das Layout des Vertexpuffers zu ändern. Mit dieser Methode wird der Inhalt des Vertex-Puffers nicht geändert. Verwenden Sie diese z. b., um eine 3D-Textur Koordinate als Binormal oder Tangens neu zu bezeichnen, oder umgekehrt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
