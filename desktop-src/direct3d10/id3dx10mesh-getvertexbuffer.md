---
description: Ruft den dem Mesh zugeordneten Vertex-Puffer ab.
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'ID3DX10Mesh:: getvertexbuffer-Methode (d3dx10. h)'
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
ms.openlocfilehash: b78db368f2467c25b4bb4218a314a22027d5d3f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361228"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a>ID3DX10Mesh:: getvertexbuffer-Methode

Ruft den dem Mesh zugeordneten Vertex-Puffer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ibuffer* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der abzuzurufendene Vertex-Puffer. Dabei handelt es sich um einen Indexwert.

</dd> <dt>

*ppvertexbuffer* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Der Scheitelpunkt Puffer. Siehe [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
