---
description: 'SWbemServices.ExecMethodAsync-Methode: Führt eine Methode aus, die von einem Methodenanbieter exportiert wird.'
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.ExecMethodAsync-Methode (Wbemdisp.h)
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
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105588"
---
# <a name="swbemservicesexecmethodasync-method"></a>SWbemServices.ExecMethodAsync-Methode

Die **ExecMethodAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) führt eine Methode aus, die von einem Methodenanbieter exportiert wird. Der Aufruf wird sofort an den Client zurückgegeben, während die eingehenden Parameter an den entsprechenden Anbieter weitergeleitet werden, an dem die Methode ausgeführt wird. Informationen und Status werden an den Aufrufer durch Ereignisse zurückgegeben, die an die in *objWbemSink* angegebene Senke übermittelt werden. Der Anbieter implementiert anstelle Windows-Verwaltungsinstrumentation (WMI) die -Methode.

Die -Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Weitere Informationen und eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

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

*objWbemSink* 
</dt> <dd>

Erforderlich. Erstellen Sie [**ein SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen. Objektsenke, die das Ergebnis des Methodenaufrufs empfängt. Die ausgehenden Parameter werden an das [**SWbemSink.OnObjectReady-Ereignis**](swbemsink-onobjectready.md) der angegebenen Objektsenke gesendet. Die Ergebnisse des Aufrufmechanismus werden an das [**SWbemSink.OnCompleted-Ereignis**](swbemsink-oncompleted.md) der angegebenen Objektsenke gesendet. Beachten Sie, **dass SWbemSink.OnCompleted** nicht den Rückgabecode der WMI-Methode erhält. Er empfängt jedoch den Rückgabecode des tatsächlichen Aufruf/Rückgabe-Mechanismus und ist nur nützlich, um zu überprüfen, ob der Aufruf aufgetreten ist oder dass er aus reinen Gründen fehlgeschlagen ist. Der von der WMI-Methode zurückgegebene Ergebniscode wird im ausgehenden Parameterobjekt zurückgegeben, das für **SWbemSink.OnObjectReady bereitgestellt wird.** Wenn ein Fehlercode zurückgegeben wird, wird das angegebene [**IWbemObjectSink-Objekt**](iwbemobjectsink.md) nicht verwendet. Wenn der Aufruf erfolgreich ist, wird die **IWbemObjectSink-Implementierung** des Benutzers aufgerufen, um das Ergebnis des Vorgangs anzugeben.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Objektpfad des Objekts enthält, für das die Methode ausgeführt wird. Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*strMethodName* 
</dt> <dd>

Erforderlich. Der Name der zu auszuführenden Methode.

</dd> <dt>

*objWbemInParams* \[ Optional\]
</dt> <dd>

Ein [**SWbemObject-Objekt,**](swbemobject.md) das die Eingabeparameter für die ausgeführte Methode enthält. Standardmäßig ist dieser Parameter nicht definiert. Weitere Informationen finden Sie unter [Constructing InParameters Objects (Erstellen von InParameters-Objekten) und Parsing OutParameters Objects (Analyse von OutParameters-Objekten).](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten des Aufrufs bestimmt. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Bewirkt, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Verhindert, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ Optional\]
</dt> <dd>

Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mit derselben Objektsenke vornehmen. Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie vornehmen. Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode**](swbemnamedvalueset-item.md) extrahiert werden. Weitere Informationen finden Sie unter [Erstellen eines asynchronen Aufrufs mit VBScript.](making-an-asynchronous-call-with-vbscript.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Wenn der Aufruf erfolgreich ist, wird ein [**OutParameters-Objekt,**](swbemmethod-outparameters.md) das auch ein [**SWbemObject**](swbemobject.md) ist, an die Senke bereitgestellt, die in *objWbemSink* angegeben ist. Das **zurückgegebene OutParameters-Objekt** enthält die Ausgabeparameter und den Rückgabewert für die ausgeführte Methode. Weitere Informationen finden Sie unter [Erstellen von InParameters-Objekten und Analysieren von OutParameters-Objekten.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ExecMethodAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der in der folgenden Liste aufgeführten Fehlercodes enthalten.

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

## <a name="remarks"></a>Bemerkungen

Wenn die ausgeführte Methode Eingabeparameter enthält, muss das [**InParameters-Objekt**](swbemmethod-inparameters.md) im *objWbemInParam-Parameter* mit der Beschreibung in den Themen [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) (Erstellen von InParameters-Objekten und Analyse von OutParameters-Objekten) identisch sein.

Verwenden **SWbemServices.ExecMethodAsync** als Alternative zum direkten Zugriff [](gloss-p.md) zum Ausführen einer Anbietermethode, wenn es nicht möglich ist, eine Methode direkt auszuführen. Verwenden Sie sie z. B. mit einer Skriptsprache, die keine Ausgabeparameter unterstützt, das heißt, wenn Ihre Methode OUT-Parameter enthält. Andernfalls wird empfohlen, den direkten Zugriff zum Aufrufen einer Methode zu verwenden. Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)

Die **SWbemServices.ExecMethodAsync-Methode** erfordert einen Objektpfad. Wenn das Skript bereits ein [**SWbemObject-Objekt**](swbemobject.md) enthält, können SieSWbemObject.Exe [**cMethodAsync aufrufen.**](swbemobject-execmethodasync-.md)

Dieser Aufruf wird sofort zurückgegeben. Die Statusinformationen werden über Rückrufe an die Senke zurückgegeben, die in *objWbemSink angegeben ist.* Um die Verarbeitung nach Abschluss des Aufrufs fortzufahren, implementieren Sie eine Unterroutine für *objWbemSink*. [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Weitere Informationen zum Beseitigen der Risiken finden Sie unter [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).

Verwenden Sie *den parameter objWbemAsyncContext,* um die Quelle eines Aufrufs zu überprüfen.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt die **ExecMethodAsync-Methode.** Das Skript erstellt ein [**Win32 \_ Process-Objekt,**](/windows/desktop/CIMWin32Prov/win32-process) das einen Prozess darstellt, in dem Editor ausgeführt wird. Es zeigt die Einrichtung eines [**InParameters-Objekts**](swbemmethod-inparameters.md) und das Abrufen von Ergebnissen aus einem [**OutParameters-Objekt.**](swbemmethod-outparameters.md) Ein Skript, das dieselben synchron ausgeführten Vorgänge zeigt, finden Sie unterSWbemServices.Exe [**cMethod**](swbemservices-execmethod.md). Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Ein Beispiel für den gleichen Vorgang mit [**SWbemObject**](swbemobject.md)finden Sie unter [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).


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



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Swbemservices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[Aufrufen einer Anbietermethode](calling-a-provider-method.md)
</dt> <dt>

[Bearbeiten von Klassen- und Instanzinformationen](manipulating-class-and-instance-information.md)
</dt> </dl>

 

