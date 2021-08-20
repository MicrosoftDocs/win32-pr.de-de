---
title: RedirectDeviceType-Enumeration
description: Wird verwendet, um den Typ eines Geräts anzugeben.
ms.assetid: B6356217-814E-462F-9DBC-F6D3C0CE129F
ms.tgt_platform: multiple
keywords:
- RedirectDeviceType-Enumerations Remotedesktopdienste
topic_type:
- apiref
api_name:
- RedirectDeviceType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e4f6424c030cdb4ff0699efadaf34f2f9ad14ec49dd8d7e7043f9b55cd9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127900"
---
# <a name="redirectdevicetype-enumeration"></a>RedirectDeviceType-Enumeration

Wird verwendet, um den Typ eines Geräts anzugeben.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  UsbDevice  = 0
} RedirectDeviceType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="UsbDevice"></span><span id="usbdevice"></span><span id="USBDEVICE"></span>**UsbDevice**
</dt> <dd>

Ein USB-Gerät.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AddDeviceByInstanceId**](imsrdpdevicecollection2-adddevicebyinstanceid.md)
</dt> <dt>

[**RedirectNow**](imsrdpdevicecollection2-redirectnow.md)
</dt> </dl>

 

 





