---
description: Proxy Funktion für die getbitsperpixel-Methode.
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: IWICPixelFormatInfo_GetBitsPerPixel_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355336"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a>Iwicpixelformatinfo- \_ getbitsperpixel- \_ Proxy Funktion

Proxy Funktion für die [**getbitsperpixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicpixelformatinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _

Zeiger auf dieses [_ *iwicpixelformatinfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) -Objekt.

</dd> <dt>

*puibitsperpixel* \[ vorgenommen\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der den bpp des Pixel Formats empfängt.

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



 

 




