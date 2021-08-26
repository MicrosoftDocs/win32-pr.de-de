---
description: Beendet den Gastdienst.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: Msvm_GuestService::StopService-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f67234a09ad150f2f039a57b321797e03444c75defe2e83cfd06b60de320a664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050390"
---
# <a name="msvm_guestservicestopservice-method"></a>Msvm \_ GuestService::StopService-Methode

Beendet den Gastdienst.

## <a name="syntax"></a>Syntax


```C++
uint32 StopService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.



| Rückgabecode/-wert                                                                                                                                             | Beschreibung         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt> </dl> | Erfolg.<br/> |
| <dl> <dt>**Nicht unterstützt**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




