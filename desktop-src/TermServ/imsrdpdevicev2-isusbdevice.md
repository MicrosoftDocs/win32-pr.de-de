---
title: IMsRdpDeviceV2 isusbdevice (Eigenschaft)
description: Gibt an, ob das Gerät für die USB-Umleitung vorgesehen ist.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- Isusbdevice-Eigenschaft Remotedesktopdienste
- Isusbdevice-Eigenschaft Remotedesktopdienste, IMsRdpDeviceV2-Schnittstelle
- IMsRdpDeviceV2-Schnittstelle Remotedesktopdienste, isusbdevice-Eigenschaft
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
ms.openlocfilehash: 3741972fdd81887713e75ed5b596e0ba1a10fd3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391521"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a>IMsRdpDeviceV2:: isusbdevice-Eigenschaft

Gibt an, ob das Gerät für die USB-Umleitung vorgesehen ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a>Eigenschaftswert

**true** , wenn das Gerät für die USB-Umleitung vorgesehen ist. andernfalls **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 mit SP1<br/>                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 mit SP1<br/>                                             |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 wird als 5b94466-7661-42a8-98b7-01904c11668f definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





