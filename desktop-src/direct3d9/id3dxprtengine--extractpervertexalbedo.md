---
description: Kopiert pro-Vertex-Albedo-Werte aus einem Mesh.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'ID3DXPRTEngine:: extractperverse texalbedo-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: ed23b75b3113421b6242f49416e4b54bfce336f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961736"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>ID3DXPRTEngine:: extractperverse texalbedo-Methode

Kopiert pro-Vertex-Albedo-Werte aus einem Mesh.

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

*pmesh* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf das [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, das in [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) verwendet wird, um das [**ID3DXPRTEngine**](id3dxprtengine.md) -Objekt zu erstellen.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Vertex-Verwendungs Beschreibungen zum Kopieren aus dem Mesh. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*Numchanin* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Farbkanäle, die aus dem Mesh kopiert werden sollen. Legen Sie auf 1 fest, um graue Materialien (R = G = B) oder 3 anzugeben, um Farb Blutungen zu aktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
