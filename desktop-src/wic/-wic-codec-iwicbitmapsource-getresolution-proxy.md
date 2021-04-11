---
description: Proxy Funktion für die GetResolution-Methode.
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: IWICBitmapSource_GetResolution_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216394"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a>IWICBitmapSource \_ GetResolution- \_ Proxy Funktion

Proxy Funktion für die [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Zeiger auf dieses [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) -Objekt.

</dd> <dt>

*pdpix* \[ vorgenommen\]
</dt> <dd>

Typ: **Double \** _

Ein Zeiger, der die x-Achse-dpi-Auflösung empfängt.

</dd> <dt>

_pDpiY * \[ out\]
</dt> <dd>

Typ: **Double \** _

Ein Zeiger, der die dpi-Auflösung der y-Achse empfängt.

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



 

 




