---
title: Execaction. Arguments (Eigenschaft)
description: Ruft bei der Skripterstellung die Argumente ab, die dem Befehlszeilen Vorgang zugeordnet sind, oder legt diese fest.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments-Eigenschaft Taskplaner
- Arguments-Eigenschaft Taskplaner, execaction-Objekt
- Execaction-Objekt Taskplaner, Arguments-Eigenschaft
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949647"
---
# <a name="execactionarguments-property"></a>Execaction. Arguments (Eigenschaft)

Ruft bei der Skripterstellung die Argumente ab, die dem Befehlszeilen Vorgang zugeordnet sind, oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Argumente, die für den Befehlszeilen Vorgang erforderlich sind.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML werden die Befehlszeilen-Vorgangs Argumente im [**Arguments**](taskschedulerschema-arguments-exectype-element.md) -Element des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Execaction**](execaction.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





