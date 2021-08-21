---
title: RegisteredTask.RunEx-Methode
description: Führt für die Skripterstellung die registrierte Aufgabe sofort mithilfe der angegebenen Flags und eines Sitzungsbezeichners aus.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- RunEx-Methode Taskplaner
- RunEx-Methode Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Objekt Taskplaner , RunEx-Methode
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
ms.openlocfilehash: ecea66d57bf473b5000e84c707e652f1c49431a840da5cc50e43f9e091c3eefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943392"
---
# <a name="registeredtaskrunex-method"></a>RegisteredTask.RunEx-Methode

Führt für die Skripterstellung die registrierte Aufgabe sofort mithilfe der angegebenen Flags und eines Sitzungsbezeichners aus.

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

*params* \[ In\]
</dt> <dd>

Die Parameter, die als Werte in den Taskaktionen verwendet werden. Um keine Parameterwerte für die Taskaktionen anzugeben, legen Sie diesen Parameter auf **Nothing** fest. Andernfalls kann ein einzelner Zeichenfolgenwert oder ein Array von Zeichenfolgenwerten angegeben werden.

Die von Ihnen angegebenen Zeichenfolgenwerte werden mit Namen gekoppelt und als Name-Wert-Paare gespeichert. Wenn Sie einen einzelnen Zeichenfolgenwert angeben, ist Arg0 der Dem Wert zugewiesene Name. Der Wert kann in der Taskaktion verwendet werden, bei der die $(Arg0)-Variable in den Aktionseigenschaften verwendet wird.

Wenn Sie Werte wie "0", "100" und "250" als Array von Zeichenfolgenwerten übergeben, ersetzt "0" die $(Arg0)-Variablen, "100" die $(Arg1)-Variablen und "250" die $(Arg2)-Variablen, die in den Aktionseigenschaften verwendet werden.

Es können maximal 32 Zeichenfolgenwerte angegeben werden.

Weitere Informationen und eine Liste der Aktionseigenschaften, die variablen $(Arg0), $(Arg1), ..., $(Arg32) in ihren Werten verwenden können, finden Sie unter [Aufgabenaktionen.](task-actions.md)

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Eine [TASK \_ RUN \_ FLAGS-Konstante,](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) die definiert, wie der Task ausgeführt wird.

</dd> <dt>

*sessionID* \[ In\]
</dt> <dd>

Die Terminalserversitzung, in der Sie die Aufgabe starten möchten.

Wenn die \_ TASK RUN USE SESSION \_ \_ \_ ID-Konstante (0x4) nicht an den *flags-Parameter* übergeben wird, wird der in diesem Parameter angegebene Wert ignoriert. Wenn die \_ TASK RUN USE SESSION \_ \_ \_ ID-Konstante an den *flags-Parameter* übergeben wird und der sessionID-Wert kleiner oder gleich 0 ist, wird ein ungültiger Argumentfehler zurückgegeben.

Wenn die \_ TASK RUN USE SESSION \_ \_ \_ ID-Konstante an den *flags-Parameter* übergeben wird und der sessionID-Wert eine gültige Sitzungs-ID größer als 0 ist und kein Wert für den *Benutzerparameter* angegeben ist, versucht der Taskplaner-Dienst, die Aufgabe interaktiv als Benutzer zu starten, der an der angegebenen Sitzung angemeldet ist.

Wenn die \_ TASK RUN USE SESSION \_ \_ \_ ID-Konstante an den *flags-Parameter* übergeben wird und der sessionID-Wert eine gültige Sitzungs-ID größer als 0 ist und ein Benutzer im  *Benutzerparameter* angegeben ist, versucht der Taskplaner Dienst, die Aufgabe interaktiv als benutzerspezifischen Benutzer zu starten.

</dd> <dt>

*runningTask* \[ out\]
</dt> <dd>

Ein [**RunningTask-Objekt,**](runningtask.md) das die neue Instanz des Tasks definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode gibt ohne Fehler zurück, aber die Aufgabe wird nicht ausgeführt, wenn die [**TaskSettings.AllowDemandStart-Eigenschaft**](tasksettings-allowdemandstart.md) für den registrierten Task auf FALSE festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





