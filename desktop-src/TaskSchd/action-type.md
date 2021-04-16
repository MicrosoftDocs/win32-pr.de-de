---
title: Action. Type-Eigenschaft
description: Ruft bei der Skripterstellung den Typ der Aktion ab.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Type-Eigenschafts Taskplaner
- Type-Eigenschafts Taskplaner, Aktions Objekt
- Aktions Objekt Taskplaner, Typeigenschaft
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477811"
---
# <a name="actiontype-property"></a>Action. Type-Eigenschaft

Ruft bei der Skripterstellung den Typ der Aktion ab.

## <a name="syntax"></a>Syntax


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft gibt eine der folgenden Aufzählungstyp-Enumerationskonstanten zurück. [**\_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Aufgabe \_ Aktion \_ exec**</dt> <dt>0</dt> </dl>                          | Diese Aktion führt einen Befehlszeilen Vorgang aus. Beispielsweise könnte die Aktion ein Skript ausführen, eine ausführbare Datei starten oder, wenn der Name eines Dokuments bereitgestellt wird, die zugehörige Anwendung suchen und die Anwendung mit dem Dokument starten.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Aufgabe \_ Aktions- \_ com- \_ Handler**</dt> <dt>5</dt> </dl>    | Durch diese Aktion wird ein Handler ausgelöst.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Aufgabe \_ Aktion \_ \_ e-Mail senden**</dt> <dt>6</dt> </dl>       | Mit dieser Aktion wird eine e-Mail-Nachricht gesendet.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Aufgabe \_ Aktion \_ zeigt \_ Meldung**</dt> <dt>7</dt> an </dl> | Diese Aktion zeigt ein Meldungs Feld an.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Der Aktionstyp wird definiert, wenn die Aktion erstellt wird, und kann später nicht geändert werden. Weitere Informationen zum Erstellen einer Aktion finden Sie unter " [**Action Collection. Create**](actioncollection-create.md)".

Informationen zur Zusammenarbeit von Aktionen und Aufgaben finden Sie unter [Aufgaben Aktionen](task-actions.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Task \_ \_ Aktionstyp**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Aktion**](action.md)
</dt> </dl>

 

 





