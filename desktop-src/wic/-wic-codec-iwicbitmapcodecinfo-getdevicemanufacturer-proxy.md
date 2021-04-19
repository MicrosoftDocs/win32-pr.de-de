---
description: Proxy Funktion für die getdevicemanufacturer-Methode.
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346302"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a>Iwicbitmapcodecinfo \_ getdevicemanufakturer \_ Proxy-Funktion

Proxy Funktion für die [**getdevicemanufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicbitmapcodecinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Zeiger auf dieses [_ *iwicbitmapcodecinfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) -Objekt.

</dd> <dt>

*cchdevicemanufakturer* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe des Namens der Gerätefertigung.

</dd> <dt>

*wzdebug-emanufakturer* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \** _

Ein Zeiger, der den Namen der Geräte Herstellung empfängt.

</dd> <dt>

_pcchActual * \[ in, out\]
</dt> <dd>

Typ: **uint \** _

Die tatsächliche Puffergröße, die zum Abrufen des Namens der Gerätefertigung benötigt wird.

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



 

 




