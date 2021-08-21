---
description: Greifen Sie nach dem Commit auf das Gerät mit ID3DX10Mesh::CommitToDevice auf den Indexpuffer des Gitters zu. Dies ist ein anderer Wert als ID3DX10Mesh::GetIndexBuffer, der den Indexpuffer zurückgibt, bevor er an das Gerät übertragen wurde.
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: ID3DX10Mesh::GetDeviceIndexBuffer-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 869bd40b49801a1469ca08baa3a493cc23e6f6238624380411c8d91de829c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990370"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>ID3DX10Mesh::GetDeviceIndexBuffer-Methode

Greifen Sie mit [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)auf den Indexpuffer des Gitters zu, nachdem ein Commit auf das Gerät übertragen wurde. Dies ist ein anderer Wert als [**ID3DX10Mesh::GetIndexBuffer,**](id3dx10mesh-getindexbuffer.md)der den Indexpuffer zurückgibt, bevor er auf das Gerät übertragen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppIndexBuffer* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Der Indexpuffer, nachdem er an das Gerät übertragen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Wenn für den Indexpuffer des Gitters noch kein Commit an das Gerät ausgeführt wurde, führt diese API automatisch einen Commit für den Indexpuffer aus, bevor sie einen Zeiger auf den Puffer zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




