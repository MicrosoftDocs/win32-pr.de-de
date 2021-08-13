---
description: 'IWICBitmapClipper_Initialize_Proxy-Funktion: Proxyfunktion für die Initialize-Methode.'
ms.assetid: 60925f5c-aca4-4f49-96d2-9b58d8310e3c
title: IWICBitmapClipper_Initialize_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapClipper_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 588b1ae4edf524aaf0f8a9485af0de7bd7a7819e2526c01f19c4e53543f68cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331334"
---
# <a name="iwicbitmapclipper_initialize_proxy-function"></a>IWICBitmapClipper Initialize \_ \_ Proxy-Funktion

Proxyfunktion für die [**Initialize-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapClipper_Initialize_Proxy(
  _In_       IWICBitmapClipper *THIS_PTR,
  _In_       IWICBitmapSource  *pISource,
  _In_ const WICRect           *prc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\***

Zeiger auf dieses [**IWICBitmapClipper-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)

</dd> <dt>

*pISource* \[ In\]
</dt> <dd>

Typ: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Die Eingabebitmapquelle.

</dd> <dt>

*prc* \[ In\]
</dt> <dd>

Typ: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***

Das Rechteck der zu beschneidenden Bitmapquelle.

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



 

 




