---
description: Die ExecMethodAsync- \_ Methode von "errbemubject" führt asynchron eine Methode aus, die von einem Methoden Anbieter exportiert wird.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: SWbemObject.ExecMethodAsync_-Methode (wbemdisp. h)
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
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218169"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.Execmethodasync- \_ Methode

Die **ExecMethodAsync \_** -Methode von " [**errbemubject**](swbemobject.md) " führt asynchron eine Methode aus, die von einem Methoden Anbieter exportiert wird. Diese Methode ähnelt [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md), funktioniert jedoch direkt mit dem-Objekt der auszuführenden Methode. Diese Methode wird von Windows-Verwaltungsinstrumentation (WMI) nicht implementiert. Der Anbieter implementiert diese Methode.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

*objwbemsink* \[ in\]
</dt> <dd>

Erforderlich. Dies ist die Objekt Senke, die die Ergebnisse des Methoden Aufrufes empfängt. Die ausgehenden Parameter werden an das Ereignis " [**slibemsink. onobjectready**](swbemsink-onobjectready.md) " der angegebenen Objekt Senke gesendet. Die Ergebnisse des-aufrufungsmechanismus werden an das Ereignis " [**slibemsink. onabgeschlossene**](swbemsink-oncompleted.md) " der angegebenen Objekt Senke gesendet. Beachten Sie, dass " **taubemsink. onabgeschlossene** " nicht den Rückgabecode der Methode empfängt. Er empfängt jedoch den Rückgabecode des eigentlichen Rückrufmechanismus und ist nur nützlich, um zu überprüfen, ob der-Befehl aufgetreten ist, oder dass er aus mechanischen Gründen fehlgeschlagen ist. Der von der-Methode zurückgegebene Ergebniscode wird im ausgehenden Parameter Objekt zurückgegeben, das für " **Swap. onobjectready**" bereitgestellt wird. Wenn ein Fehlercode zurückgegeben wird, wird das angegebene [**iwbejebjectsink**](iwbemobjectsink.md) -Objekt nicht verwendet. Wenn der Aufruf erfolgreich ist, wird die **iwberobjectsink** -Implementierung des Benutzers aufgerufen, um das Ergebnis des Vorgangs anzuzeigen.

</dd> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Dies ist der Name der-Methode für das-Objekt.

</dd> <dt>

*objwbeminparameams* \[ in, optional\]
</dt> <dd>

Hierbei handelt es sich um ein Objekt vom [**typaustausch**](swbemobject.md) , das die Eingabeparameter für die Methode enthält, die ausgeführt wird. Standardmäßig ist dieser Parameter nicht definiert. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten](constructing-inparameters-objects.md) und Überprüfen von [outparameter-Objekten](parsing-outparameters-objects.md).

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus * * * * (128 (0x80))


</dt> <dd>

Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus * * * * (0 (0x0))


</dt> <dd>

Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

In der Regel ist Sie nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> <dt>

*objwbemasynccontext* \[ in, optional\]
</dt> <dd>

Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen. Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert. Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode hat keine Rückgabewerte. Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**OutParameters**](swbemmethod-outparameters.md) -Objekt, das auch ein " [**errbefubject**](swbemobject.md) "-Objekt ist, an die in *objwbemsink* angegebene Senke bereitgestellt. Das zurückgegebene **OutParameters** -Objekt enthält die Ausgabeparameter und den Rückgabewert für die Methode, die ausgeführt wird.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ExecMethodAsync \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse war ungültig.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrInvalidMethod** -2147749934 (0x8004102e)
</dt> <dd>

Die angeforderte Methode war nicht verfügbar.

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer war nicht autorisiert, die Methode auszuführen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **SWbemObject.Exe\_ cmethodasync** -Methode als Alternative zum direkten Zugriff auf die Ausführung einer [*Anbieter Methode*](gloss-p.md) , wenn Sie eine Methode nicht direkt ausführen können. Wenn Ihre Methode z. b. über out-Parameter verfügt, verwenden Sie die **SWbemObject.Exe\_ cmethodasync** -Methode mit einer Skriptsprache, die keine Ausgabeparameter unterstützt. Andernfalls wird empfohlen, eine Methode mithilfe des direkten Zugriffs aufzurufen. Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

Dieser Rückruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist. Um jedes Objekt zu verarbeiten, sobald es eintrifft, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine. Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Wenn die ausgeführte Methode über Eingabeparameter verfügt, müssen das [**InParameters**](swbemmethod-inparameters.md) -Objekt und der *objwbeminparam* -Parameter erstellt werden, wie unter [Erstellen von inparameter-Objekten](constructing-inparameters-objects.md) und [Parsing outparameter-Objekten](parsing-outparameters-objects.md)beschrieben.

Die **SWbemObject.Execmethodasync \_** -Methode geht davon aus, dass [**das durch das**](swbemobject.md) -Objekt dargestellte Objekt die auszuführende Methode enthält. Die [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md) -Methode erfordert einen Objekt Pfad.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die [**ExecMethodAsync**](swbemservices-execmethodasync.md) -Methode. Das Skript erstellt ein [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekt, das einen Prozess darstellt, der Notepad ausgeführt wird. Es zeigt das Einrichten des [**InParameters**](swbemmethod-inparameters.md) -Objekts und das Abrufen von Ergebnissen von einem [**OutParameters**](swbemmethod-outparameters.md) -Objekt.

Informationen zu einem Skript, das die synchron ausgeführten Vorgänge anzeigt, finden Sie unter [**SWbemObject.Execmethod**](swbemobject-execmethod-.md). Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [**Create method \_ in der Win32-Klasse**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Ein Beispiel für denselben Vorgang mit einem " [**Swap Services**](swbemservices.md) "-Objekt finden Sie unter [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md).


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Objekt**](swbemobject.md)
</dt> <dt>

[**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

