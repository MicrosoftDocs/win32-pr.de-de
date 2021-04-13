---
title: Aktioncollection. Create-Methode
description: Bei der Skripterstellung wird von eine neue Aktion erstellt und der Auflistung hinzugefügt.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Create-Methode Taskplaner
- Create Method Taskplaner, Aktions Sammlungsobjekt
- Aktions Sammlungsobjekt Taskplaner, Create-Methode
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
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518233"
---
# <a name="actioncollectioncreate-method"></a>Aktioncollection. Create-Methode

Bei der Skripterstellung wird von eine neue Aktion erstellt und der Auflistung hinzugefügt.

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Dieser Parameter ist auf eine der folgenden [**\_ \_ Aufgabentyp**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) -Enumerationskonstanten für Aufgaben festgelegt.



| Wert                                                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <dt>**Aufgabe \_ Aktion \_ exec**</dt> <dt>0</dt> </dl>                          | Die Aktion führt einen Befehlszeilen Vorgang aus. Beispielsweise könnte die Aktion ein Skript ausführen, eine ausführbare Datei starten oder, wenn der Name eines Dokuments bereitgestellt wird, die zugehörige Anwendung suchen und die Anwendung mit dem Dokument starten.<br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <dt>**Aufgabe \_ Aktions- \_ com- \_ Handler**</dt> <dt>5</dt> </dl>    | Die Aktion löst einen Handler aus.<br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <dt>**Aufgabe \_ Aktion \_ \_ e-Mail senden**</dt> <dt>6</dt> </dl>       | Diese Aktion sendet eine e-Mail-Nachricht.<br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <dt>**Aufgabe \_ Aktion \_ zeigt \_ Meldung**</dt> <dt>7</dt> an </dl> | Diese Aktion zeigt ein Meldungs Feld an.<br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Aktions**](action.md) Objekt, das die neue Aktion darstellt.

## <a name="remarks"></a>Bemerkungen

Der Sammlung können nicht mehr als 32 Aktionen hinzugefügt werden.

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

[**ActionCollection**](actioncollection.md)
</dt> <dt>

[**Aktion**](action.md)
</dt> <dt>

[**Execaction**](execaction.md)
</dt> <dt>

[**Emailaction**](emailaction.md)
</dt> <dt>

[**Showmessageaction**](showmessageaction.md)
</dt> <dt>

[**Comhandleraction**](comhandleraction.md)
</dt> </dl>

 

 





