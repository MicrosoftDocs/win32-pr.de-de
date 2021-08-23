---
description: Erstellt ein N-Patch-Gitter aus einem Dreiecksgitter.
ms.assetid: f565ed0b-72fc-4184-b423-f68b0acfafb0
title: D3DXCreateNPatchMesh-Funktion (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateNPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb23022bfa79ba9bc429bc76a5c42892403b783b4ed634e9b7887b74db126b87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241370"
---
# <a name="d3dxcreatenpatchmesh-function"></a>D3DXCreateNPatchMesh-Funktion

Erstellt ein N-Patch-Gitter aus einem Dreiecksgitter.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreateNPatchMesh(
  _In_    LPD3DXMESH      pMeshSysMem,
  _Inout_ LPD3DXPATCHMESH *pPatchMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMeshSysMem* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Adresse eines Zeigers auf eine [**ID3DXMesh-Schnittstelle,**](id3dxmesh.md) die das Dreiecksgittermodellobjekt darstellt.

</dd> <dt>

*pPatchMesh* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXPatchMesh-Schnittstelle,**](id3dxpatchmesh.md) die das erstellte Patchmeshobjekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




