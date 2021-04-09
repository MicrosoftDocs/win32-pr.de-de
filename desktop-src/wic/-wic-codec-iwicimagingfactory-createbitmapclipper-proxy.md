---
description: Proxy Funktion für die Methode "kreatebitmapclipper".
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: IWICImagingFactory_CreateBitmapClipper_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960496"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a>IWICImagingFactory- \_ Funktion "endbitmapclipper" \_

Proxy Funktion für die Methode " [**kreatebitmapclipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) ".

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfactory* \[ in\]
</dt> <dd>

Typ: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_ppIBitmapClipper * \[ out\]
</dt> <dd>

Typ: **[ **iwicbitmapclipperdatei**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***

Ein Zeiger, der einen Zeiger auf ein neues [**iwicbitmapclipperelement**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)empfängt.

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



 

 




