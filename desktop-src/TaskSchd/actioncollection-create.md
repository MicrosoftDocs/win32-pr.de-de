---
title: ActionCollection.Create-Methode
description: Für die Skripterstellung erstellt und fügt der Auflistung eine neue Aktion hinzu.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Erstellen einer Taskplaner
- Erstellen einer Methode Taskplaner , ActionCollection-Objekt
- ActionCollection-Objekt Taskplaner , Create-Methode
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce517ae33681fcb106e83720fc5ddd7685f26f673c466e24162ce95e9ca442
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072700"
---
# <a name="actioncollectioncreate-method"></a>ActionCollection.Create-Methode

Für die Skripterstellung erstellt und fügt der Auflistung eine neue Aktion hinzu.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* \[ In\]
</dt> <dd>

Dieser Parameter wird auf eine der folgenden [**TASK \_ ACTION \_ TYPE-Enumerationskonst**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) constants festgelegt.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**AUFGABE \_ ACTION \_ EXEC**</dt> <dt>0</dt> </dl>                          | Die Aktion führt einen Befehlszeilenvorgang aus. Beispielsweise kann die Aktion ein Skript ausführen, eine ausführbare Datei starten oder, wenn der Name eines Dokuments angegeben wird, die zugehörige Anwendung suchen und die Anwendung mit dem Dokument starten.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**AUFGABE \_ ACTION \_ COM \_ HANDLER**</dt> <dt>5</dt> </dl>    | Die Aktion gibt einen Handler aus.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**AUFGABE \_ AKTION \_ \_ E-MAIL SENDEN**</dt> <dt>6</dt> </dl>       | Diese Aktion sendet eine E-Mail.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**AUFGABE \_ AKTION \_ MELDUNG \_ 7**</dt> <dt>ANZEIGEN</dt> </dl> | Diese Aktion zeigt ein Meldungsfeld an.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Action-Objekt,**](action.md) das die neue Aktion darstellt.

## <a name="remarks"></a>Hinweise

Sie können der Sammlung nicht mehr als 32 Aktionen hinzufügen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_ \_ TASKAKTIONSTYP**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**ActionCollection**](actioncollection.md)
</dt> <dt>

[**Aktion**](action.md)
</dt> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[**EmailAction**](emailaction.md)
</dt> <dt>

[**ShowMessageAction**](showmessageaction.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





