---
title: IMsRdpDeviceV2 IsUSBDevice (Eigenschaft)
description: Gibt an, ob das Gerät für die USB-Umleitung bestimmt ist.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- IsUSBDevice-Remotedesktopdienste
- IsUSBDevice-Eigenschaft Remotedesktopdienste , IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste , IsUSBDevice-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e03e2572912487cb924f65350dbdd7818d07d2a7b172d18cb28fab87335a00dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138563"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a>IMsRdpDeviceV2::IsUSBDevice (Eigenschaft)

Gibt an, ob das Gerät für die USB-Umleitung bestimmt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a>Eigenschaftswert

**TRUE,** wenn das Gerät für die USB-Umleitung verwendet wird; andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 mit SP1<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 mit SP1<br/>                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 ist als 5fb94466-7661-42a8-98b7-01904c11668f definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





