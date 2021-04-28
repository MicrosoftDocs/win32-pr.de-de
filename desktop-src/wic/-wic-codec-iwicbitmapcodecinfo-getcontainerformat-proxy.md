---
description: 'IWICBitmapCodecInfo_GetContainerFormat_Proxy-Funktion: Proxyfunktion für die GetContainerFormat-Methode.'
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086368"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a>IWICBitmapCodecInfo \_ \_ GetContainerFormat-Proxyfunktion

Proxyfunktion für die [**GetContainerFormat-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Zeiger auf dieses [**IWICBitmapCodecInfo-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)

</dd> <dt>

*pguidContainerFormat* \[ out\]
</dt> <dd>

Typ: **GUID \***

Ein Zeiger, der die Container-GUID empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




