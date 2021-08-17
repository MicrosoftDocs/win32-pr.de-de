---
description: Die ExecMethodAsync-Methode \_ von SWbemObject führt asynchron eine Methode aus, die ein Methodenanbieter exportiert.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: SWbemObject.ExecMethodAsync_-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37d7a0ab0b2e4d1ab893619eda4b3d32b8b4e1f60791e0981125d4445bda5f98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857350"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.Exe\_ cMethodAsync-Methode

Die **\_ ExecMethodAsync-Methode** von [**SWbemObject**](swbemobject.md) führt asynchron eine Methode aus, die ein Methodenanbieter exportiert. Diese Methode ähnelt [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), arbeitet jedoch direkt mit dem Objekt der auszuführenden Methode. Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) implementiert diese Methode nicht. Der Anbieter implementiert diese Methode.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objWbemSink* \[ In\]
</dt> <dd>

Erforderlich. Dies ist die Objektsenke, die die Ergebnisse des Methodenaufrufs empfängt. Die ausgehenden Parameter werden an das [**SWbemSink.OnObjectReady-Ereignis**](swbemsink-onobjectready.md) der angegebenen Objektsenke gesendet. Die Ergebnisse des Aufrufmechanismus werden an das [**SWbemSink.OnCompleted-Ereignis**](swbemsink-oncompleted.md) der angegebenen Objektsenke gesendet. Beachten Sie, dass **SWbemSink.OnCompleted** nicht den Rückgabecode der -Methode empfängt. Er empfängt jedoch den Rückgabecode des tatsächlichen Aufrufrückgabemechanismus und ist nur nützlich, um zu überprüfen, ob der Aufruf aufgetreten ist oder dass er aus mechanischen Gründen fehlgeschlagen ist. Der von der -Methode zurückgegebene Ergebniscode wird im ausgehenden Parameterobjekt zurückgegeben, das für **SWbemSink.OnObjectReady** bereitgestellt wird. Wenn ein Fehlercode zurückgegeben wird, wird das angegebene [**IWbemObjectSink-Objekt**](iwbemobjectsink.md) nicht verwendet. Wenn der Aufruf erfolgreich ist, wird die **IWbemObjectSink-Implementierung** des Benutzers aufgerufen, um das Ergebnis des Vorgangs anzugeben.

</dd> <dt>

*strMethodName* \[ In\]
</dt> <dd>

Erforderlich. Dies ist der Name der Methode für das -Objekt.

</dd> <dt>

*objwbemInParams* \[ in, optional\]
</dt> <dd>

Dies ist ein [**SWbemObject-Objekt,**](swbemobject.md) das die Eingabeparameter für die ausgeführte Methode enthält. Dieser Parameter ist standardmäßig nicht definiert. Weitere Informationen finden Sie unter [Erstellen von InParameters-Objekten](constructing-inparameters-objects.md) und [Analysieren von OutParameters-Objekten.](parsing-outparameters-objects.md)

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Ganze Zahl, die das Verhalten des Aufrufs bestimmt. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Bewirkt, dass asynchrone Aufrufe Statusupdates an den [**SWbemSink.OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus( (0 (0x0))


</dt> <dd>

Verhindert, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, optional\]
</dt> <dd>

In der Regel ist sie nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ in, optional\]
</dt> <dd>

Dies ist ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mit derselben Objektsenke vornehmen. Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie vornehmen. Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode**](swbemnamedvalueset-item.md) extrahiert werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode verfügt über keine Rückgabewerte. Wenn der Aufruf erfolgreich ist, wird ein [**OutParameters-Objekt,**](swbemmethod-outparameters.md) das auch ein [**SWbemObject-Objekt**](swbemobject.md) ist, an die Senke bereitgestellt, die in *objWbemSink* angegeben ist. Das **zurückgegebene OutParameters-Objekt** enthält die Ausgabeparameter und den Rückgabewert für die ausgeführte Methode.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **\_ ExecMethodAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidClass** – 2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse war ungültig.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrInvalidMethod** – 2147749934 (0x8004102E)
</dt> <dd>

Die angeforderte Methode war nicht verfügbar.

</dd> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer war nicht berechtigt, die -Methode auszuführen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie die **SWbemObject.Exe\_ cMethodAsync-Methode** als Alternative zum direkten Zugriff zum Ausführen einer [*Anbietermethode,*](gloss-p.md) wenn Sie eine Methode nicht direkt ausführen können. Wenn Ihre Methode beispielsweise out-Parameter aufweist, verwenden Sie die **SWbemObject.Exe\_ cMethodAsync-Methode** mit einer Skriptsprache, die keine Ausgabeparameter unterstützt. Andernfalls wird empfohlen, eine Methode mithilfe des direkten Zugriffs aufzurufen. Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)

Dieser Aufruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden dem Aufrufer über Rückrufe zurückgegeben, die an die Senke übermittelt werden, die in *objWbemSink* angegeben ist. Um jedes Objekt zu verarbeiten, wenn es eintrifft, erstellen Sie einen *objWbemSink*. [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md) Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in Ihrer Implementierung von *objWbemSink* ausführen. [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke bereitzustellen. Dies stellt Sicherheitsrisiken für Ihre Skripts und Anwendungen dar. Um die Risiken zu vermeiden, verwenden Sie entweder semisynchrone Kommunikation oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Wenn die ausgeführte Methode Über Eingabeparameter verfügt, müssen das [**InParameters-Objekt**](swbemmethod-inparameters.md) und der *objWbemInParam-Parameter* wie unter [Erstellen von InParameters-Objekten](constructing-inparameters-objects.md) und [Analysieren von OutParameters-Objekten](parsing-outparameters-objects.md)beschrieben erstellt werden.

Die **SWbemObject.ExecMethodAsync-Methode \_** geht davon aus, dass das durch [**SWbemObject**](swbemobject.md) dargestellte Objekt die auszuführende Methode enthält. Die [**SWbemServices.ExecMethodAsync-Methode**](swbemservices-execmethodasync.md) erfordert einen Objektpfad.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die [**ExecMethodAsync-Methode.**](swbemservices-execmethodasync.md) Das Skript erstellt ein [**\_ Win32-Prozessobjekt,**](/windows/desktop/CIMWin32Prov/win32-process) das einen Prozess darstellt, der Editor ausgeführt wird. Es zeigt das Einrichten des [**InParameters-Objekts**](swbemmethod-inparameters.md) und das Abrufen von Ergebnissen aus einem [**OutParameters-Objekt.**](swbemmethod-outparameters.md)

Ein Skript, das die gleichen Vorgänge zeigt, die synchron ausgeführt werden, finden Sie unter [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md). Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [**Create Method in Class Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Ein Beispiel für den gleichen Vorgang mit einem [**SWbemServices-Objekt**](swbemservices.md) finden Sie unter [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

