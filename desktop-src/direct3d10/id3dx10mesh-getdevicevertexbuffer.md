---
description: Greifen Sie mit ID3DX10Mesh::CommitToDevice auf den Scheitelpunktpuffer des Gitters zu, nachdem ein Commit auf das Gerät ausgeführt wurde. Dies unterscheidet sich von ID3DX10Mesh::GetVertexBuffer, das den Scheitelpunktpuffer zurückgibt, bevor ein Commit auf das Gerät ausgeführt wurde.
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: ID3DX10Mesh::GetDeviceVertexBuffer-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 11493392f710fe3fd3bebab5187b61522434b268bf099489d84ea1cc3ec99309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540263"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a>ID3DX10Mesh::GetDeviceVertexBuffer-Methode

Greifen Sie mit [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)auf den Scheitelpunktpuffer des Gitters zu, nachdem ein Commit auf das Gerät ausgeführt wurde. Dies unterscheidet sich von [**ID3DX10Mesh::GetVertexBuffer,**](id3dx10mesh-getvertexbuffer.md)das den Scheitelpunktpuffer zurückgibt, bevor ein Commit auf das Gerät ausgeführt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iBuffer* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Ein Index, der angibt, auf welchen Scheitelpunktpuffer zugegriffen werden soll.

</dd> <dt>

*ppVertexBuffer* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Der Scheitelpunktpuffer, nachdem ein Commit auf das Gerät ausgeführt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
