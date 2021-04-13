---
description: Erstellt ein neues patchmesh mit der angegebenen Scheitelpunkt Deklaration.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'ID3DXPatchMesh:: clonemesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354326"
---
# <a name="id3dxpatchmeshclonemesh-method"></a>ID3DXPatchMesh:: clonemesh-Methode

Erstellt ein neues patchmesh mit der angegebenen Scheitelpunkt Deklaration.

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Optionen* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination aus einem oder mehreren [**D3DXMESH**](./d3dxmesh.md) -Flags, die Erstellungs Optionen für das Mesh angeben.

</dd> <dt>

*pdecl* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format für die Scheitel Punkte im Ausgabe Mesh angeben.

</dd> <dt>

*pmesh* \[ Out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXPatchMesh**](id3dxpatchmesh.md) -Schnittstelle, die das geklonte Mesh darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

**Clonemesh** konvertiert den Scheitelpunkt Puffer in die neue Scheitelpunkt Deklaration. Einträge in der Vertex-Deklaration, die neu im ursprünglichen Mesh sind, werden auf 0 festgelegt. Wenn das aktuelle Mesh über eine beliebige Konsistenz verfügt, ist das neue Mesh ebenfalls mit der Sicherheit vertraut.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
