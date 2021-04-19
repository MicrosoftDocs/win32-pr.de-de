---
description: Führt ein adaptives Mosaik basierend auf dem z-basierten adaptiven Mosaik Kriterium aus.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'ID3DXPatchMesh:: tttellateadaptive-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353377"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>ID3DXPatchMesh:: Tess. Adaptive-Methode

Führt ein adaptives Mosaik basierend auf dem z-basierten adaptiven Mosaik Kriterium aus.

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

*ptrans* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Gibt einen 4D-Vektor an, der mit den Scheitel Punkten dargestellt wird, um die pro-vertexadaptive Mosaik Menge zu erhalten. Jeder Rand wird auf den Durchschnittswert der Mosaik Ebenen für die beiden Scheitel Punkte, die er verbindet, festgesetzt.

</dd> <dt>

*dwmaxtess Level* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Maximale Beschränkung für das adaptive Mosaik. Dies ist die Anzahl der Scheitel Punkte, die zwischen vorhandenen Vertices eingeführt wurden. Dieser ganzzahlige Wert kann zwischen 1 und 32 (einschließlich) liegen.

</dd> <dt>

*dwmintess Level* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Mindestgrenzwert für das adaptive Mosaik. Dies ist die Anzahl der Scheitel Punkte, die zwischen vorhandenen Vertices eingeführt wurden. Dieser ganzzahlige Wert kann zwischen 1 und 32 (einschließlich) liegen.

</dd> <dt>

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Resultierende Mosaik Gitter. Siehe [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird effizienter durchgeführt, wenn das patchmesh mit [**ID3DXPatchMesh:: optimiert**](id3dxpatchmesh--optimize.md)optimiert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
