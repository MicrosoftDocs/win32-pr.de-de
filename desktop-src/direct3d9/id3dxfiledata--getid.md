---
description: Ruft die GUID dieses Dateidatenobjekts ab.
ms.assetid: 79bf56b5-5900-4427-8092-3a1df86f8a57
title: ID3DXFileData::GetId-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a9a1cbf98792b0ac36c35aabf40b8c125a497201b27c6a161c0706f077ffc491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295326"
---
# <a name="id3dxfiledatagetid-method"></a>ID3DXFileData::GetId-Methode

Ruft die GUID dieses Dateidatenobjekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pId* \[ out\]
</dt> <dd>

Typ: **LPGUID**

Zeiger auf eine GUID, um die ID dieses Dateidatenobjekts zu empfangen. Wenn das Dateidatenobjekt keine ID hat, ist der zurückgegebene Parameterwert GUID \_ NULL.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




