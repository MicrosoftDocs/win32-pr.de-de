---
title: Taskplaner Fehler-und Erfolgs Konstanten (Winerror. h)
description: Wenn ein Fehler auftritt, können die Taskplaner-APIs einen der folgenden Fehlercodes als HRESULT-Wert zurückgeben.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Taskplaner Taskplaner-, Verweis-, Fehler-und Erfolgs Konstanten
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369571"
---
# <a name="task-scheduler-error-and-success-constants"></a>Taskplaner Fehler-und Erfolgs Konstanten

Wenn ein Fehler auftritt, können die Taskplaner-APIs einen der folgenden Fehlercodes als **HRESULT** -Wert zurückgeben.

Die Konstanten, die mit "sched S" beginnen \_ \_ , sind Erfolgs Konstanten, und die Konstanten, die mit "sched E" beginnen, \_ \_ sind Fehler Konstanten.

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

Beispiel aus [C/C++-Code Beispiel: Abrufen des Aufgaben Status](c-c-code-example-retrieving-task-status.md).

> [!Note]  
> Einige Taskplaner APIs können System-und Netzwerkfehler Codes zurückgeben (z. b. 64). Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den Befehl **net helpmsg** im Eingabe Aufforderungs Fenster verwenden. Der Befehl **net helpmsg 64** gibt beispielsweise die folgende Meldung zurück: der angegebene Netzwerkname ist nicht mehr verfügbar.

 

Weitere Informationen zu Ereignissen und Fehlermeldungen finden Sie unter [Events And Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).

<dl> <dt>

<span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**Aufgabe ist \_ \_ \_ abgeschlossen.**
</dt> <dd> <dl> <dt>

0x00041300
</dt> <dt>



Der Task kann zum nächsten geplanten Zeitpunkt ausgeführt werden.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**sched \_ S- \_ Aufgabe wird \_ ausgeführt**
</dt> <dd> <dl> <dt>

0x00041301
</dt> <dt>



Die Aufgabe wird gerade ausgeführt.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**sched \_ S \_ Aufgabe \_ deaktiviert**
</dt> <dd> <dl> <dt>

0x00041302
</dt> <dt>



Der Task wird nicht zu den geplanten Zeiten ausgeführt, weil er deaktiviert wurde.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**der Task "sched \_ S" \_ \_ wurde \_ nicht \_ ausgeführt.**
</dt> <dd> <dl> <dt>

0x00041303
</dt> <dt>



Der Task wurde noch nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**der Task "sched S" wird \_ \_ \_ nicht \_ mehr \_ ausgeführt.**
</dt> <dd> <dl> <dt>

0x00041304
</dt> <dt>



Es sind keine weiteren Ausführungen für diese Aufgabe geplant.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**sched \_ S \_ Aufgabe \_ nicht \_ geplant**
</dt> <dd> <dl> <dt>

0x00041305
</dt> <dt>



Mindestens eine der Eigenschaften, die zum Ausführen dieser Aufgabe nach einem Zeitplan benötigt werden, wurde nicht festgelegt.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**sched \_ S \_ Aufgabe wurde \_ beendet.**
</dt> <dd> <dl> <dt>

0x00041306
</dt> <dt>



Die letzte Ausführungsdauer der Aufgabe wurde vom Benutzer beendet.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**sched \_ S- \_ Aufgabe \_ keine \_ gültigen \_ Trigger**
</dt> <dd> <dl> <dt>

0x00041307
</dt> <dt>



Entweder hat der Task keine Trigger, oder die vorhandenen Trigger sind deaktiviert oder nicht festgelegt.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**sched \_ S- \_ Ereignis \_ auslöst**
</dt> <dd> <dl> <dt>

0x00041308
</dt> <dt>



Ereignis Trigger haben keine festgelegten Laufzeiten.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**sched E-Auslösung \_ \_ \_ nicht \_ gefunden**
</dt> <dd> <dl> <dt>

0x80041309
</dt> <dt>



Der auslösertyp einer Aufgabe wurde nicht gefunden.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**sched \_ E- \_ Aufgabe \_ nicht \_ bereit**
</dt> <dd> <dl> <dt>

0x8004130a
</dt> <dt>



Mindestens eine der zum Ausführen dieser Aufgabe erforderlichen Eigenschaften wurde nicht festgelegt.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**sched \_ E- \_ Aufgabe wird \_ nicht \_ ausgeführt**
</dt> <dd> <dl> <dt>

0x8004130b
</dt> <dt>



Es ist keine laufende Instanz der Aufgabe vorhanden.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**sched \_ E- \_ Dienst \_ nicht \_ installiert**
</dt> <dd> <dl> <dt>

0x8004130c
</dt> <dt>



Der Taskplaner-Dienst ist auf diesem Computer nicht installiert.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**sched \_ E \_ kann \_ Aufgabe nicht öffnen \_**
</dt> <dd> <dl> <dt>

0x8004130d
</dt> <dt>



Das Task Objekt konnte nicht geöffnet werden.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**sched \_ E \_ ungültige \_ Aufgabe**
</dt> <dd> <dl> <dt>

0x8004130e
</dt> <dt>



Das-Objekt ist entweder ein ungültiges Task Objekt oder kein Task Objekt.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**die sched \_ E- \_ Konto \_ Informationen \_ \_ wurden nicht festgelegt.**
</dt> <dd> <dl> <dt>

0x8004130f
</dt> <dt>



In der Taskplaner-Sicherheitsdatenbank wurden keine Kontoinformationen für die jeweilige Aufgabe gefunden.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**der sched \_ E- \_ \_ Kontoname wurde \_ nicht \_ gefunden.**
</dt> <dd> <dl> <dt>

0x80041310
</dt> <dt>



Das vorhanden sein des angegebenen Kontos kann nicht festgelegt werden.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**sched \_ E \_ Account \_ dBASE \_ beschädigt**
</dt> <dd> <dl> <dt>

0x80041311
</dt> <dt>



In der Taskplaner-Sicherheitsdatenbank wurde eine Beschädigung festgestellt. die Datenbank wurde zurückgesetzt.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**sched \_ E \_ No \_ Security \_ Services**
</dt> <dd> <dl> <dt>

0x80041312
</dt> <dt>



Taskplaner Sicherheitsdienste sind nur unter Windows NT verfügbar.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**sched \_ E \_ unbekannte \_ Objekt \_ Version**
</dt> <dd> <dl> <dt>

0x80041313
</dt> <dt>



Die Task Objekt Version wird entweder nicht unterstützt oder ist ungültig.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**sched \_ E \_ nicht unterstützte \_ Konto \_ Option**
</dt> <dd> <dl> <dt>

0x80041314
</dt> <dt>



Der Task wurde mit einer nicht unterstützten Kombination aus Kontoeinstellungen und Laufzeitoptionen konfiguriert.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**sched \_ E- \_ Dienst wird \_ nicht \_ ausgeführt**
</dt> <dd> <dl> <dt>

0x80041315
</dt> <dt>



Der Taskplaner-Dienst wird nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**sched \_ E \_ unexpectednode**
</dt> <dd> <dl> <dt>

0x80041316
</dt> <dt>



Die Task-XML-Datei enthält einen unerwarteten Knoten.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**sched \_ E- \_ Namespace**
</dt> <dd> <dl> <dt>

0x80041317
</dt> <dt>



Die Task-XML-Datei enthält ein Element oder Attribut aus einem unerwarteten Namespace.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**sched \_ E \_ invalidvalue**
</dt> <dd> <dl> <dt>

0x80041318
</dt> <dt>



Die Task-XML-Datei enthält einen Wert, der falsch formatiert oder außerhalb des gültigen Bereichs liegt.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**sched \_ E \_ missingnode**
</dt> <dd> <dl> <dt>

0x80041319
</dt> <dt>



In der XML-Aufgabe fehlt ein erforderliches Element oder Attribut.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**sched \_ E \_ malformedxml**
</dt> <dd> <dl> <dt>

0x8004131a
</dt> <dt>



Die Task-XML-Datei ist falsch formatiert.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**Fehler beim \_ \_ auslösen einiger \_ Trigger \_**
</dt> <dd> <dl> <dt>

0x0004131b
</dt> <dt>



Der Task wird registriert, aber nicht alle angegebenen Trigger starten den Task.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**sched \_ S-Problem bei der \_ Batch \_ Anmeldung \_**
</dt> <dd> <dl> <dt>

0x0004131c
</dt> <dt>



Der Task ist registriert, kann jedoch möglicherweise nicht gestartet werden. Die Batch Anmelde Berechtigung muss für den Task Prinzipal aktiviert werden.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**sched \_ E \_ zu \_ viele \_ Knoten**
</dt> <dd> <dl> <dt>

0x8004131d
</dt> <dt>



Die Task-XML-Datei enthält zu viele Knoten desselben Typs.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**sched \_ E \_ nach \_ Ende \_ Grenze**
</dt> <dd> <dl> <dt>

0x8004131e
</dt> <dt>



Der Task kann nicht nach der Endpunkt Grenze des Auslösers gestartet werden.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**sched \_ E wird \_ bereits \_ ausgeführt**
</dt> <dd> <dl> <dt>

0x8004131f
</dt> <dt>



Eine Instanz dieser Aufgabe wird bereits ausgeführt.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**sched \_ E \_ Benutzer \_ nicht \_ angemeldet \_**
</dt> <dd> <dl> <dt>

0x80041320
</dt> <dt>



Der Task wird nicht ausgeführt, da der Benutzer nicht angemeldet ist.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**sched \_ E \_ ungültiger \_ \_ taskhash**
</dt> <dd> <dl> <dt>

0x80041321
</dt> <dt>



Das Aufgaben Image ist beschädigt oder wurde manipuliert.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**sched \_ E- \_ Dienst \_ nicht \_ verfügbar**
</dt> <dd> <dl> <dt>

0x80041322
</dt> <dt>



Der Taskplaner-Dienst ist nicht verfügbar.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**sched \_ E- \_ Dienst \_ zu \_ stark ausgelastet**
</dt> <dd> <dl> <dt>

0x80041323
</dt> <dt>



Der Taskplaner-Dienst ist zu stark ausgelastet, um Ihre Anforderung zu verarbeiten. Versuchen Sie es später noch mal.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**sched \_ E- \_ Aufgabe \_ versucht**
</dt> <dd> <dl> <dt>

0x80041324
</dt> <dt>



Der Taskplaner Dienst hat versucht, die Aufgabe auszuführen, aber die Aufgabe wurde aufgrund einer der Einschränkungen in der Aufgabendefinition nicht ausgeführt.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**sched \_ S \_ Task in \_ Warteschlange eingereiht**
</dt> <dd> <dl> <dt>

0x00041325
</dt> <dt>



Der Taskplaner-Dienst hat die Aufgabe zur Durchführung der Aufgabe aufgefordert.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**sched \_ E- \_ Aufgabe \_ deaktiviert**
</dt> <dd> <dl> <dt>

0x80041326
</dt> <dt>



Der Task ist deaktiviert.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**Sched \_ E \_ Task \_ nicht \_ v1- \_ Kompatibilität**
</dt> <dd> <dl> <dt>

0x80041327
</dt> <dt>



Der Task verfügt über Eigenschaften, die mit früheren Versionen von Windows nicht kompatibel sind.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**sched \_ E \_ \_ bei \_ Bedarf starten**
</dt> <dd> <dl> <dt>

0x80041328
</dt> <dt>



Mit den Task Einstellungen kann die Aufgabe nicht bei Bedarf gestartet werden.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



 

 





