---
description: Greifen Sie auf den Attributpuffer des Gitters zu.
ms.assetid: 01ebb592-1e0d-4d93-b3f5-ad5f1e0225d0
title: ID3DX10Mesh::GetAttributeBuffer-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1368ad4e783a047b6cc0e9d1e6cb47b6bd9653e3122ff10c16adbd4dc20b3839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046948"
---
# <a name="id3dx10meshgetattributebuffer-method"></a>ID3DX10Mesh::GetAttributeBuffer-Methode

Greifen Sie auf den Attributpuffer des Gitters zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAttributeBuffer(
  [out] ID3DX10MeshBuffer **ppAttributeBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppAttributeBuffer* \[ out\]
</dt> <dd>

Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Der Attributpuffer. Siehe [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).

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

 

 




