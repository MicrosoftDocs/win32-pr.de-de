---
title: IMsRdpDeviceCollection RescanDevices-Methode
description: Aktualisiert die Liste der Objekte in der Auflistung. | IMsRdpDeviceCollection RescanDevices-Methode
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- RescanDevices-Methode Remotedesktopdienste
- RescanDevices-Methode Remotedesktopdienste , IMsRdpDeviceCollection-Schnittstelle
- IMsRdpDeviceCollection-Schnittstelle Remotedesktopdienste , RescanDevices-Methode
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
ms.openlocfilehash: d62011697b21171f8de326689ca35195ad4057e2e6edd01a5159fcf89c32d0f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959240"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>IMsRdpDeviceCollection::RescanDevices-Methode

Aktualisiert die Liste der Objekte in der Auflistung.

## <a name="syntax"></a>Syntax


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vboolDynRedir* \[ In\]
</dt> <dd>

Der Standardumleitungsstatus, der auf alle neu ermittelten Geräte oder Laufwerke angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Jeder andere **HRESULT-Wert** gibt an, dass der Aufruf fehlgeschlagen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection ist als 56540617-d281-488c-8738-6a8fdf64a118 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





