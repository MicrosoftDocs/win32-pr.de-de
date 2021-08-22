---
description: Proxyfunktion für die GetReaderByIndex-Methode.
ms.assetid: 9d70b339-9772-4c13-949e-109f354f9986
title: IWICMetadataBlockReader_GetReaderByIndex_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetReaderByIndex_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1540e6ff0e24125f9381c0dd177dd9dc77ea6fb7f9096d45b88fd7489704f496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965189"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a>IWICMetadataBlockReader \_ GetReaderByIndex-Proxyfunktion \_

Proxyfunktion für die [**GetReaderByIndex-Methode.**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICMetadataBlockReader_GetReaderByIndex_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _In_  UINT                    nIndex,
  _Out_ IWICMetadataReader      **ppIMetadataReader
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\***

Zeiger auf dieses [**IWICMetadataBlockReader-Objekt.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)

</dd> <dt>

*nIndex* \[ In\]
</dt> <dd>

Typ: **UINT**

</dd> <dt>

*ppIMetadataReader* \[ out\]
</dt> <dd>

Typ: **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




