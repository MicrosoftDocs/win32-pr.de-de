---
description: 'ID3DX10Mesh::GetVertexBuffer-Methode: Ruft den Scheitelpunktpuffer ab, der dem Gitternetz zugeordnet ist.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: ID3DX10Mesh::GetVertexBuffer-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 804ece9ca82fbdd8dc5778b888fecc4ca8fbc04b8fc45976b857b417343f4b32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069974"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a>ID3DX10Mesh::GetVertexBuffer-Methode

Ruft den Scheitelpunktpuffer ab, der dem Gitternetz zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iBuffer* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Der zu erhaltende Scheitelpunktpuffer. Dies ist ein Indexwert.

</dd> <dt>

*ppVertexBuffer* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Der Scheitelpunktpuffer. Siehe [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
