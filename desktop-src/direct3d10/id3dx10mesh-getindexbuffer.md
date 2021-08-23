---
description: 'ID3DX10Mesh::GetIndexBuffer-Methode: Ruft die Daten in einem Indexpuffer ab.'
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: ID3DX10Mesh::GetIndexBuffer-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 03babe487bfd28048f726590ce567ac191c6cd3cf737daecc4853afaa53e535d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046918"
---
# <a name="id3dx10meshgetindexbuffer-method"></a>ID3DX10Mesh::GetIndexBuffer-Methode

Ruft die Daten in einem Indexpuffer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppIndexBuffer* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Adresse eines Zeigers auf eine ID3DX10MeshBuffer-Schnittstelle, die den dem Gitternetz zugeordneten Indexpuffer darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

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

 

 




