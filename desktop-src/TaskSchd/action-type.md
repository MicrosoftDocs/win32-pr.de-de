---
title: Action.Type-Eigenschaft
description: Ruft für die Skripterstellung den Typ der Aktion ab.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Typeigenschafts-Taskplaner
- Type-Eigenschaft Taskplaner , Aktionsobjekt
- Aktionsobjekt Taskplaner , Type-Eigenschaft
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
ms.openlocfilehash: 499c7e42b5b2578928796e6f878219e0c53612e454948d390cdb631dcaccd64c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739030"
---
# <a name="actiontype-property"></a>Action.Type-Eigenschaft

Ruft für die Skripterstellung den Typ der Aktion ab.

## <a name="syntax"></a>Syntax


```VB
Action.Type As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft gibt eine der folgenden [**TASK \_ ACTION \_ TYPE-Enumerationskonst**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) constants zurück.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**AUFGABE \_ ACTION \_ EXEC**</dt> <dt>0</dt> </dl>                          | Diese Aktion führt einen Befehlszeilenvorgang aus. Die Aktion kann z. B. ein Skript ausführen, eine ausführbare Datei starten oder, wenn der Name eines Dokuments angegeben ist, die zugehörige Anwendung suchen und die Anwendung mit dem Dokument starten.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**AUFGABE \_ ACTION \_ COM \_ HANDLER**</dt> <dt>5</dt> </dl>    | Diese Aktion gibt einen Handler aus.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**AUFGABE \_ AKTION \_ \_ E-MAIL SENDEN**</dt> <dt>6</dt> </dl>       | Mit dieser Aktion wird eine E-Mail gesendet.<br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**AUFGABE \_ AKTION \_ MELDUNG \_ 7**</dt> <dt>ANZEIGEN</dt> </dl> | Diese Aktion zeigt ein Meldungsfeld an.<br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Hinweise

Der Aktionstyp wird beim Erstellen der Aktion definiert und kann später nicht mehr geändert werden. Informationen zum Erstellen einer Aktion finden Sie unter [**ActionCollection.Create**](actioncollection-create.md).

Informationen zur Zusammenarbeit von Aktionen und Aufgaben finden Sie unter [Aufgabenaktionen](task-actions.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_ \_ TASKAKTIONSTYP**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Aktion**](action.md)
</dt> </dl>

 

 





