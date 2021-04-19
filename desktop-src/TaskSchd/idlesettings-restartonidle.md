---
title: Idlesettings. restartondle (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt, oder legt diesen fest.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Restartondle-Eigenschaft Taskplaner
- Restartondle-Eigenschaft Taskplaner, idlesettings-Objekt
- Idlesettings-Objekt Taskplaner, restartondle-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342216"
---
# <a name="idlesettingsrestartonidle-property"></a>Idlesettings. restartondle (Eigenschaft)

Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

Ein boolescher Wert, der angibt, ob die Aufgabe neu gestartet werden muss, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt. Die Standardeinstellung lautet „false“.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nur verwendet, wenn die [**idlesettings. stoponidleend**](idlesettings-stoponidleend.md) -Eigenschaft auf true festgelegt ist.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**restartondle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Idlesettings**](idlesettings.md)
</dt> </dl>

 

 





