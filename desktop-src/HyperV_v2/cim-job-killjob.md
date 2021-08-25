---
description: Eine Methode, um diesen Auftrag und alle zugrunde liegenden Prozesse zu löschen und alle verfingenden Zuordnungen zu entfernen. Diese Methode ist veraltet. Verwenden Sie stattdessen RequestChangeState.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: KillJob-Methode der CIM_Job Klasse
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
ms.openlocfilehash: 681d6a878f90f29708812fce2c39f27024ed588deb5f3b8066cc4833487fd91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900330"
---
# <a name="killjob-method-of-the-cim_job-class"></a>KillJob-Methode der CIM \_ Job-Klasse

Eine Methode, um diesen Auftrag und alle zugrunde liegenden Prozesse zu löschen und alle "vergenden" Zuordnungen zu entfernen. Diese Methode ist veraltet. Verwenden **Sie stattdessen RequestChangeState.** **KillJob** ist veraltet, da kein Unterschied zwischen einem geordneten Herunterfahren und einem sofortigen Beenden besteht. [**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() stellt die Optionen "Terminate" und "Kill" zur Verfügung, um diese Unterscheidung zu ermöglichen.

## <a name="syntax"></a>Syntax


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DeleteOnKill* \[ In\]
</dt> <dd>

Gibt an, ob der Auftrag bei Beendigung automatisch gelöscht werden soll. Dieser Parameter hat Vorrang vor der **DeleteOnCompletion-Eigenschaft.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg eine 0 zurück. andernfalls gibt einen Fehler zurück.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Unbekannt** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Fehler** (4)
</dt> <dt>

**Zugriff verweigert** (6)
</dt> <dt>

**Nicht gefunden** (7)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Auftrag**](cim-job.md)
</dt> </dl>

 

 




