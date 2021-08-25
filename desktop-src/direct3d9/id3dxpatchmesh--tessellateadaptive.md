---
description: Führt ein adaptives Mosaik basierend auf dem z-basierten Adaptiven Mosaikkriterium aus.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: ID3DXPatchMesh::TessellateAdaptive-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6365cfcf50debfeeb28fd493b76ac60943ee14f27a2dadec168b3dd4d31ace1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856290"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>ID3DXPatchMesh::TessellateAdaptive-Methode

Führt ein adaptives Mosaik basierend auf dem z-basierten Adaptiven Mosaikkriterium aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTrans* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Gibt einen 4D-Vektor an, der mit den Scheitelpunkten gepunktet ist, um die Menge des adaptiven Mosaiks pro Scheitelpunkt abzurufen. Jeder Rand wird mit dem Durchschnittswert der Mosaikebenen für die beiden Scheitelpunkte verknüpft, die er verbindet.

</dd> <dt>

*dwMaxTessLevel* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Maximales Limit für adaptive Mosaik. Dies ist die Anzahl von Scheitelpunkten, die zwischen vorhandenen Scheitelpunkten eingeführt werden. Dieser ganzzahlige Wert kann zwischen 1 und einschließlich 32 liegen.

</dd> <dt>

*dwMinTessLevel* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Mindestlimit für adaptive Mosaik. Dies ist die Anzahl von Scheitelpunkten, die zwischen vorhandenen Scheitelpunkten eingeführt werden. Dieser ganzzahlige Wert kann zwischen 1 und einschließlich 32 liegen.

</dd> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Resultierendes Mosaikgitternetz. Siehe [**ID3DXMesh.**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Diese Funktion wird effizienter ausgeführt, wenn das Patchmesh mit [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md)optimiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
