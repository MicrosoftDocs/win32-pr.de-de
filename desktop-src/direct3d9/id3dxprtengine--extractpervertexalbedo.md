---
description: Kopiert Werte pro Scheitelpunkt-Albedo aus einem Gitternetz.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: ID3DXPRTEngine::ExtractPerVertexAlbedo-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e094a7681c13e21cdaab71648b3733749fc179f845e23496a07f3c2b7b99234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747750"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>ID3DXPRTEngine::ExtractPerVertexAlbedo-Methode

Kopiert Werte pro Scheitelpunkt-Albedo aus einem Gitternetz.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMesh* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf das [**ID3DXMesh-Meshobjekt,**](id3dxmesh.md) das in [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) zum Erstellen des [**ID3DXPRTEngine-Objekts**](id3dxprtengine.md) verwendet wird.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Vertexverwendungsbeschreibungen, die aus dem Gitternetz kopiert werden sollen. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*NumChinIn* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Farbkanäle, die aus dem Gitternetz kopiert werden sollen. Legen Sie auf 1 fest, um graue Materialien anzugeben (R = G = B) oder 3, um Farbunterdärkungseffekte zu ermöglichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
