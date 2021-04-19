---
description: Proxy Funktion für die GetReaderByIndex-Methode.
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
ms.openlocfilehash: e2fc967f810b9ac8e43ad7da543bb1723500da48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351043"
---
# <a name="iwicmetadatablockreader_getreaderbyindex_proxy-function"></a>IWICMetadataBlockReader \_ GetReaderByIndex- \_ Proxy Funktion

Proxy Funktion für die [**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) -Methode.

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

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _

Zeiger auf dieses [_ *IWICMetadataBlockReader* *](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Objekt.

</dd> <dt>

*nIndex* \[ in\]
</dt> <dd>

Typ: **uint**

</dd> <dt>

*ppIMetadataReader* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\*\***

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




