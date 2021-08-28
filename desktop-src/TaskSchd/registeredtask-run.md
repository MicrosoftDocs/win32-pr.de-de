---
title: RegisteredTask.Run-Methode
description: Für die Skripterstellung führt den registrierten Task sofort aus.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Ausführen der Taskplaner
- Ausführen der Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Objekt Taskplaner , Run-Methode
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
ms.openlocfilehash: e747688ba80c08a39b0336fda126ae7d85a558f53c97aab230bc5d3d0113b360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681620"
---
# <a name="registeredtaskrun-method"></a>RegisteredTask.Run-Methode

Für die Skripterstellung führt den registrierten Task sofort aus.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*params* \[ In\]
</dt> <dd>

Die Parameter, die als Werte in den Aufgabenaktionen verwendet werden. Um keine Parameterwerte für die Aufgabenaktionen anzugeben, legen Sie diesen Parameter auf **Nothing fest.** Andernfalls kann ein einzelner Zeichenfolgenwert oder ein Array von Zeichenfolgenwerten angegeben werden.

Die angegebenen Zeichenfolgenwerte werden mit Namen gekoppelt und als Name-Wert-Paare gespeichert. Wenn Sie einen einzelnen Zeichenfolgenwert angeben, ist Arg0 der Name, der dem Wert zugewiesen ist. Der Wert kann in der Taskaktion verwendet werden, bei der die $(Arg0)-Variable in den Aktionseigenschaften verwendet wird.

Wenn Sie Werte wie "0", "100" und "250" als Array von Zeichenfolgenwerten übergeben, ersetzt "0" die $(Arg0)-Variablen, "100" ersetzt die $(Arg1)-Variablen, und "250" ersetzt die $(Arg2)-Variablen, die in den Aktionseigenschaften verwendet werden.

Es können maximal 32 Zeichenfolgenwerte angegeben werden.

Weitere Informationen und eine Liste der Aktionseigenschaften, die variablen $(Arg0), $(Arg1), ..., $(Arg32) in ihren Werten verwenden können, finden Sie unter [Aufgabenaktionen](task-actions.md).

</dd> <dt>

*ppRunningTask* \[ out\]
</dt> <dd>

Ein [**RunningTask-Objekt,**](runningtask.md) das die neue Instanz der Aufgabe definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **RegisteredTask.Run-Funktion** entspricht der [**RegisteredTask.RunEx-Funktion**](registeredtask-runex.md) mit dem flags-Parameter gleich 0 und nichts, das für den Benutzerparameter angegeben ist.

Diese Methode gibt ohne Fehler zurück, aber die Aufgabe wird nicht ausgeführt, wenn die [**TaskSettings.AllowDemandStart-Eigenschaft**](tasksettings-allowdemandstart.md) für den registrierten Task auf FALSE festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





