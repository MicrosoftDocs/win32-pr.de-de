---
description: Führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Execmethodasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898912efae276fc0404576e162468e06e1b95a68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347888"
---
# <a name="swbemservicesexecmethodasync-method"></a>SWbemServices.Execmethodasync-Methode

Die **ExecMethodAsync** -Methode des [**Swap Services**](swbemservices.md) -Objekts führt eine Methode aus, die von einem Methoden Anbieter exportiert wird. Der-Befehl kehrt sofort an den Client zurück, während die eingehenden Parameter an den entsprechenden Anbieter weitergeleitet werden, in dem die Methode ausgeführt wird. Informationen und Status werden an den Aufrufer zurückgegeben, indem Ereignisse an die Senke gesendet werden, die in *objwbemsink* angegeben ist. Der Anbieter implementiert die-Methode anstelle von Windows-Verwaltungsinstrumentation (WMI).

Die-Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Weitere Informationen und eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objwbemsink* 
</dt> <dd>

Erforderlich. Erstellen Sie ein " [**taubemsink**](swbemsink.md) "-Objekt zum Empfangen der Objekte. Objekt Senke, die das Ergebnis des Methoden Aufrufes empfängt. Die ausgehenden Parameter werden an das Ereignis " [**slibemsink. onobjectready**](swbemsink-onobjectready.md) " der angegebenen Objekt Senke gesendet. Die Ergebnisse des-aufrufungsmechanismus werden an das Ereignis " [**slibemsink. onabgeschlossene**](swbemsink-oncompleted.md) " der angegebenen Objekt Senke gesendet. Beachten Sie, dass " **taubemsink. onabgeschlossene** " den Rückgabecode der WMI-Methode nicht empfängt. Er empfängt jedoch den Rückgabecode des eigentlichen Rückrufmechanismus und ist nur nützlich, um zu überprüfen, ob der-Befehl aufgetreten ist, oder dass er aus mechanischen Gründen fehlgeschlagen ist. Der Ergebniscode, der von der WMI-Methode zurückgegeben wird, wird im ausgehenden Parameter Objekt zurückgegeben, das an " **taubemsink. onobjectready**" übergeben wird. Wenn ein Fehlercode zurückgegeben wird, wird das angegebene Objekt " [**iwbejebjectsink**](iwbemobjectsink.md) " nicht verwendet. Wenn der Aufruf erfolgreich ist, wird die **iwberobjectsink** -Implementierung des Benutzers aufgerufen, um das Ergebnis des Vorgangs anzuzeigen.

</dd> <dt>

*strobjectpath* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Objekt Pfad des-Objekts enthält, für das die-Methode ausgeführt wird. Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*"Name"* 
</dt> <dd>

Erforderlich. Der Name der zu auszuführenden Methode.

</dd> <dt>

*objwbeminparameams* \[ optionale\]
</dt> <dd>

Ein [**-**](swbemobject.md) Objekt, das die Eingabeparameter für die Methode enthält, die ausgeführt wird. Standardmäßig ist dieser Parameter nicht definiert. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus * * * * (128 (0x80))


</dt> <dd>

Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus * * * * (0 (0x0))


</dt> <dd>

Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> <dt>

*objwbemasynccontext* \[ optionale\]
</dt> <dd>

Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen. Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert. Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden. Weitere Informationen finden Sie unter [Erstellen eines asynchronen Aufrufes mit VBScript](making-an-asynchronous-call-with-vbscript.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Wenn der-Befehl erfolgreich ausgeführt wurde, wird ein [**OutParameters**](swbemmethod-outparameters.md) -Objekt, das ebenfalls ein " [**errbefubject**](swbemobject.md) "-Objekt ist, an die Senke bereitgestellt, die in *objwbemsink* angegeben ist. Das zurückgegebene **OutParameters** -Objekt enthält die Ausgabeparameter und den Rückgabewert für die Methode, die ausgeführt wird. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **ExecMethodAsync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der in der folgenden Liste aufgeführten Fehlercodes enthalten.

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

Wenn die ausgeführte Methode Eingabeparameter enthält, muss das [**InParameters**](swbemmethod-inparameters.md) -Objekt im *objwbeminparam* -Parameter mit der Beschreibung in den Themen [Erstellen von InParameters-Objekten und Parsing OutParameters-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md) identisch sein.

Verwenden Sie **SWbemServices.Execmethodasync** als Alternative zum direkten Zugriff auf die Ausführung einer [*Anbieter Methode*](gloss-p.md) , wenn es nicht möglich ist, eine Methode direkt auszuführen. Verwenden Sie diese z. b. mit einer Skriptsprache, die keine Ausgabeparameter unterstützt, d. h., wenn die Methode out-Parameter aufweist. Andernfalls wird empfohlen, den direkten Zugriff zu verwenden, um eine Methode aufzurufen. Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

Die **SWbemServices.Execmethodasync** -Methode erfordert einen Objekt Pfad. Wenn das Skript bereits ein " [**errbemubject**](swbemobject.md) "-Objekt enthält, können Sie [**SWbemObject.Execmethodasync**](swbemobject-execmethodasync-.md)aufrufen.

Dieser Rückruf wird sofort zurückgegeben. Die Statusinformationen werden an den Aufrufer zurückgegeben, indem die Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist. Um die Verarbeitung fortzusetzen, wenn der-Befehl abgeschlossen ist, implementieren Sie eine Unterroutine für die *objwbemsink*. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Weitere Informationen zum Beseitigen der Risiken finden Sie unter Festlegen der [Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

Verwenden Sie den *objwbemasynccontext* -Parameter, um die Quelle eines Aufrufes zu überprüfen.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt die **ExecMethodAsync** -Methode. Das Skript erstellt ein [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekt, das einen Prozess darstellt, der Notepad ausgeführt wird. Es zeigt das Einrichten eines [**InParameters**](swbemmethod-inparameters.md) -Objekts und das Abrufen von Ergebnissen von einem [**OutParameters**](swbemmethod-outparameters.md) -Objekt. Informationen zu einem Skript, das die synchron ausgeführten Vorgänge anzeigt, finden Sie unter [**SWbemServices.Execmethod**](swbemservices-execmethod.md). Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [Create Method in \_ der Win32-Klasse](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Ein Beispiel für denselben Vorgang mit " [**Swap**](swbemobject.md)" finden Sie unter [**SWbemObject.Execmethodasync**](swbemobject-execmethodasync-.md).


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
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
| CLSID<br/>                    | CLSID- \_ Austauschdienste<br/>                                                         |
| IID<br/>                      | IID \_ iswbemservices<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.Execmethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.Execmethodasync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.Execmethod**](swbemservices-execmethod.md)
</dt> <dt>

[Aufrufen einer Anbieter Methode](calling-a-provider-method.md)
</dt> <dt>

[Manipulieren von Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md)
</dt> </dl>

 

