---
title: Registeredtask. RunEx-Methode
description: Führt bei der Skripterstellung die registrierte Aufgabe sofort mithilfe der angegebenen Flags und einer Sitzungs-ID aus.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- RunEx-Methode Taskplaner
- RunEx-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, RunEx-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104661"
---
# <a name="registeredtaskrunex-method"></a>Registeredtask. RunEx-Methode

Führt bei der Skripterstellung die registrierte Aufgabe sofort mithilfe der angegebenen Flags und einer Sitzungs-ID aus.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

 Parameter \[ in\]
</dt> <dd>

Die Parameter, die als Werte in den Aufgaben Aktionen verwendet werden. Wenn Sie keine Parameterwerte für die Task Aktionen angeben möchten, legen Sie diesen Parameter auf " **Nothing**" fest. Andernfalls kann ein einzelner Zeichen folgen Wert oder ein Array von Zeichen folgen Werten angegeben werden.

Die Zeichen folgen Werte, die Sie angeben, werden mit Namen gekoppelt und als Name-Wert-Paare gespeichert. Wenn Sie einen einzelnen Zeichen folgen Wert angeben, ist Arg0 der Name, der dem Wert zugewiesen wird. Der Wert kann in der Task Aktion verwendet werden, bei der die $ (Arg0)-Variable in den Aktions Eigenschaften verwendet wird.

Wenn Sie Werte wie z. b. "0", "100" und "250" als Array von Zeichen folgen Werten übergeben, ersetzt "0" die Variablen "$ (Arg0)", "100" ersetzt die Variablen "$ (arg1)", und "250" ersetzt die $ (arg2)-Variablen, die in den Aktions Eigenschaften verwendet werden.

Es können maximal 32 Zeichen folgen Werte angegeben werden.

Weitere Informationen und eine Liste der Aktions Eigenschaften, die die Variablen $ (Arg0), $ (arg1),..., $ (Arg32) in ihren Werten verwenden können, finden Sie unter [Task Actions](task-actions.md).

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Eine [ \_ \_ tasktestflags](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) -Konstante, die definiert, wie die Aufgabe ausgeführt wird.

</dd> <dt>

*SessionID* \[ in\]
</dt> <dd>

Die Terminal Server Sitzung, in der die Aufgabe gestartet werden soll.

Wenn die aufgabenrun- \_ \_ Sitzungs-ID- \_ \_ Konstante (0x4) nicht an den *Flags* -Parameter übergeben wird, wird der in diesem Parameter angegebene Wert ignoriert. Wenn die Task Ausführungs- \_ \_ ID der \_ Sitzungs \_ -ID an den *Flags* -Parameter übergeben wird und der SessionID-Wert kleiner oder gleich 0 ist, wird ein ungültiger Argument Fehler zurückgegeben.

Wenn die \_ \_ \_ aufgabenrun-Sitzungs- \_ ID-Konstante in den *Flags* -Parameter übergeben wird und der SessionID-Wert eine gültige Sitzungs-ID größer als 0 ist und kein Wert für den *User* -Parameter angegeben wird, versucht der Taskplaner Dienst, die Aufgabe interaktiv zu starten, als der Benutzer, der bei der angegebenen Sitzung angemeldet ist.

Wenn die \_ \_ \_ aufgabenrun-Sitzungs- \_ ID-Konstante in den *Flags* -Parameter übergeben wird und der SessionID-Wert eine gültige Sitzungs-ID ist, die größer als 0 ist, und wenn ein Benutzer im *Benutzer* Parameter angegeben wird, versucht der Taskplaner Dienst, die Aufgabe interaktiv zu starten, als der Benutzer, der im *Benutzer* Parameter angegeben ist.

</dd> <dt>

*runningtask* \[ vorgenommen\]
</dt> <dd>

Ein [**runningtask**](runningtask.md) -Objekt, das die neue Instanz der Aufgabe definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird ohne Fehler zurückgegeben, aber die Aufgabe wird nicht ausgeführt, wenn die [**Task Settings. allowdemandstart**](tasksettings-allowdemandstart.md) -Eigenschaft für die registrierte Aufgabe auf false festgelegt ist.

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

[**Registeredtask**](registeredtask.md)
</dt> </dl>

 

 





