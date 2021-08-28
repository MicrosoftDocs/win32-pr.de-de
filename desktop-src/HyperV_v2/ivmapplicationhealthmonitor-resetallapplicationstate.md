---
description: Setzt den Integritätsstatus für alle Anwendungen auf einem virtuellen Computer zurück.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: IVmApplicationHealthMonitor::ResetAllApplicationState-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4e97d5d16200501d77acf8b0b02cc5562d51706fcc46298421ad7f7e8fc0dfac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694350"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>IVmApplicationHealthMonitor::ResetAllApplicationState-Methode

Setzt den Integritätsstatus für alle Anwendungen auf einem virtuellen Computer zurück. Wenn der Status erfolgreich ist, wird der Integritätsstatus für alle überwachten Anwendungen auf **ApplicationStateHealthy festgelegt.**

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Um dieses Programmierelement verwenden zu können, müssen Windows 8 Integrationskomponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Integrationskomponenten für Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




