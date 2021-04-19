---
description: Proxy Funktion für die getchannelcount-Methode.
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: IWICPixelFormatInfo_GetChannelCount_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6bf3f0d8aaf6cf95633fa4cce771bd7c7e8db85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369101"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a>Iwicpixelformatinfo ( \_ getchannelcount- \_ Proxy Funktion)

Proxy Funktion für die [**getchannelcount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicpixelformatinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _

Zeiger auf dieses [_ *iwicpixelformatinfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) -Objekt.

</dd> <dt>

*puichannelcount* \[ vorgenommen\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der die Kanalanzahl empfängt.

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



 

 




