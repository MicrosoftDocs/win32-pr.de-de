---
description: Setzt den Integritäts Status aller Anwendungen auf einem virtuellen Computer zurück.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'Ivmapplicationhealthmonitor:: resetallapplicationstate-Methode'
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
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863567"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>Ivmapplicationhealthmonitor:: resetallapplicationstate-Methode

Setzt den Integritäts Status aller Anwendungen auf einem virtuellen Computer zurück. Bei erfolgreicher Ausführung wird der Integritäts Status für alle überwachten Anwendungen auf **applicationstatehealthy** festgelegt.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Um dieses Programmier Element zu verwenden, müssen die Windows 8-Integrations Komponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                      |
| Version<br/>                  | Integrations Komponenten für Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>Vmapplicationhealthmonitor. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmapplicationhealthmonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




