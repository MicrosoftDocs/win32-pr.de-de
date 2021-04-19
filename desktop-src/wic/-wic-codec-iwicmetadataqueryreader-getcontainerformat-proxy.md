---
description: Proxy Funktion für die GetContainerFormat-Methode.
ms.assetid: 3a909151-53c2-4f82-9ead-f689b73f5faf
title: IWICMetadataQueryReader_GetContainerFormat_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d8138a1217611ff60be9001ce038f9ecfbe7e34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351719"
---
# <a name="iwicmetadataqueryreader_getcontainerformat_proxy-function"></a>IWICMetadataQueryReader \_ GetContainerFormat- \_ Proxy Funktion

Proxy Funktion für die [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICMetadataQueryReader_GetContainerFormat_Proxy(
  _In_  IWICMetadataQueryReader *THIS_PTR,
  _Out_ GUID                    *pguidContainerFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _

Zeiger auf dieses [_ *IWICMetadataQueryReader* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Objekt.

</dd> <dt>

*pguidcontainerformat* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **GUID \** _

Ein Zeiger, der die GUID des cointainer-Formats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




