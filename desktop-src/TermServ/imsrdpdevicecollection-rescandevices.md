---
title: Imsrdpdevicecollection-Methode "rescandevices"
description: Aktualisiert die Liste der-Objekte in der Auflistung. | Imsrdpdevicecollection-Methode "rescandevices"
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Methode zum erneuten Hinzufügen der Geräte Remotedesktopdienste
- Methode "rescandevices" Remotedesktopdienste "imsrdpdevicecollection"-Schnittstelle
- Imsrdpdevicecollection-Schnittstelle Remotedesktopdienste, Methode zum erneuten konvertieren
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354326"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>Imsrdpdevicecollection:: rescandevices-Methode

Aktualisiert die Liste der-Objekte in der Auflistung.

## <a name="syntax"></a>Syntax


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vbooldynredir* \[ in\]
</dt> <dd>

Der Standard Umleitungs Status, der auf alle neu ermittelten Geräte oder Laufwerke angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT** -Wert gibt an, dass der-Fehler aufgetreten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ imsrdpendvicecollection ist als 56540617-d281-488c-8738-6a8sdf64a118 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imsrdpde vicecollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





