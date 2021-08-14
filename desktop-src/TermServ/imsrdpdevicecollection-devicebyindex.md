---
title: IMsRdpDeviceCollection DeviceByIndex-Eigenschaft
description: Ruft das Gerät am angegebenen Index ab.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- DeviceByIndex-Eigenschaft Remotedesktopdienste
- DeviceByIndex-Eigenschaft Remotedesktopdienste , IMsRdpDeviceCollection-Schnittstelle
- IMsRdpDeviceCollection-Schnittstelle Remotedesktopdienste , DeviceByIndex-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f13279cdf5bed0cd56921dde2344918262abed7e5473290560757e76f4c595c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606439"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a>IMsRdpDeviceCollection::D eviceByIndex-Eigenschaft

Ruft das Gerät am angegebenen Index ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**IMsRdpDevice-Schnittstellenzeiger.**](imsrdpdevice.md)

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection ist als 56540617-d281-488c-8738-6a8fdf64a118 definiert.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





