---
description: Eine Methode, um diesen Auftrag und alle zugrunde liegenden Prozesse zu beenden und um alle verbleibenden Zuordnungen zu entfernen. Diese Methode ist veraltet. Verwenden Sie stattdessen requestchangestate.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Killjob-Methode der CIM_Job-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959562"
---
# <a name="killjob-method-of-the-cim_job-class"></a>Killjob-Methode der CIM- \_ Auftrags Klasse

Eine Methode, um diesen Auftrag und alle zugrunde liegenden Prozesse zu beenden und alle "verbleibenden" Zuordnungen zu entfernen. Diese Methode ist veraltet. Verwenden Sie stattdessen **requestchangestate** . " **Killjob** " ist veraltet, da zwischen einem ordnungsgemäßen Herunterfahren und einem sofortigen Abbruch kein Unterschied besteht. [**CIM \_ "Concretejob**](cim-concretejob.md)". **RequestStateChange**() stellt die Optionen "beenden" und "Kill" bereit, um diesen Unterschied zuzulassen.

## <a name="syntax"></a>Syntax


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deleteonkill* \[ in\]
</dt> <dd>

Gibt an, ob der Auftrag bei Beendigung automatisch gelöscht werden soll. Dieser Parameter hat Vorrang vor der **deleteoncompletion** -Eigenschaft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannt** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

Fehler **(4** )
</dt> <dt>

**Zugriff verweigert** (6)
</dt> <dt>

**Nicht gefunden** (7)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Auftrag**](cim-job.md)
</dt> </dl>

 

 




