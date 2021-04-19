---
title: Registeredtask. Run-Methode
description: Führt bei der Skripterstellung die registrierte Aufgabe sofort aus.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Run-Methode Taskplaner
- Run-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, Run-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343045"
---
# <a name="registeredtaskrun-method"></a>Registeredtask. Run-Methode

Führt bei der Skripterstellung die registrierte Aufgabe sofort aus.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
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

*pprunningtask* \[ vorgenommen\]
</dt> <dd>

Ein [**runningtask**](runningtask.md) -Objekt, das die neue Instanz der Aufgabe definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **registeredtask. Run** -Funktion entspricht der [**registeredtask. RunEx**](registeredtask-runex.md) -Funktion, wobei der Flags-Parameter gleich 0 und für den User-Parameter nichts angegeben ist.

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

 

 





