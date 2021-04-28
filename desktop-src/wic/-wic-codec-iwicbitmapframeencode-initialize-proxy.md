---
description: 'IWICBitmapFrameEncode_Initialize_Proxy Funktion: Proxyfunktion für die Initialize-Methode.'
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: IWICBitmapFrameEncode_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e8c8a7526343e6dfcda9859fd06259700019a9bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100548"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a>IWICBitmapFrameEncode-Funktion \_ "Proxy initialisieren" \_

Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***

Zeiger auf dieses [**IWICBitmapFrameEncode-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)

</dd> <dt>

*pIEncoderOptions* \[ In\]
</dt> <dd>

Typ: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\***

Der Satz von Eigenschaften, die für die Initialisierung von [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) verwendet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

