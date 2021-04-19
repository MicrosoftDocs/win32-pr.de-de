---
description: 'Greifen Sie auf den Index Puffer des Mesh zu, nachdem er mit ID3DX10Mesh:: committedevice an das Gerät übertragen wurde. Dies unterscheidet sich von ID3DX10Mesh:: getindexbuffer, das den Index Puffer zurückgibt, bevor er an das Gerät übertragen wurde.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'ID3DX10Mesh:: getdeviceidexbuffer-Methode (d3dx10. h)'
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
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353747"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a>ID3DX10Mesh:: getdeviceidexbuffer-Methode

Greifen Sie auf den Index Puffer des Mesh zu, nachdem er mit [**ID3DX10Mesh:: committedevice**](id3dx10mesh-committodevice.md)an das Gerät übertragen wurde. Dies unterscheidet sich von [**ID3DX10Mesh:: getindexbuffer**](id3dx10mesh-getindexbuffer.md), das den Index Puffer zurückgibt, bevor er an das Gerät übertragen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppindexbuffer* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***

Der Index Puffer, nachdem ein Commit für das Gerät ausgeführt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Wenn der Index Puffer des Netzes noch nicht an das Gerät übergeben wurde, führt diese API automatisch einen Commit für den Index Puffer aus, bevor er einen Zeiger auf den Puffer zurückgibt.

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

 

 




