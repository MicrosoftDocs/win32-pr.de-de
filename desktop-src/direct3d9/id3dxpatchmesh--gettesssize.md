---
description: Ruft die Größe des mosaikierten Gitters bei einer Mosaikebene ab.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: ID3DXPatchMesh::GetTessSize-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4668f50236684f104aedf0ad9ecad413a583facbc45d5f3fa0331abb5938bf5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493050"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>ID3DXPatchMesh::GetTessSize-Methode

Ruft die Größe des mosaikierten Gitters bei einer Mosaikebene ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fTessLevel* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Mosaikebene.

</dd> <dt>

*Adaptive Anpassung* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Adaptive Mosaik. Legen Sie für adaptives Mosaik diesen Wert auf **TRUE** und fTessLevel auf den maximalen Mosaikwert fest. Dies führt zu der maximalen Gittergröße, die für das adaptive Mosaik erforderlich ist.

</dd> <dt>

*NumTriangles* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl von Dreiecken, die vom Mosaikgitter generiert werden.

</dd> <dt>

*NumVertices* \[ out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf die Anzahl von Scheitelpunkt, die vom Mosaikgitter generiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Methode geht von einem einheitlichen Mosaik aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
