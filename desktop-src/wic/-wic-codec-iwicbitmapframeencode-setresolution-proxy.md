---
description: 'IWICBitmapFrameEncode_SetResolution_Proxy Funktion: Proxyfunktion für die SetResolution-Methode.'
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: IWICBitmapFrameEncode_SetResolution_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc873338af1c043b0cf1a6fa3cebc60bfde1ebf0510817a378b424d939c6e9fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711647"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a>IWICBitmapFrameEncode \_ \_ SetResolution-Proxyfunktion

Proxyfunktion für die [**SetResolution-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***

Zeiger auf dieses [**IWICBitmapFrameEncode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)

</dd> <dt>

*dpiX* \[ In\]
</dt> <dd>

Typ: **double**

Der horizontale Auflösungswert.

</dd> <dt>

*dpiY* \[ In\]
</dt> <dd>

Typ: **double**

Der vertikale Auflösungswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows NUR XP mit SP2, Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




