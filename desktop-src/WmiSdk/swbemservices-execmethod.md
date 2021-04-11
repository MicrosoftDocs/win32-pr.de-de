---
description: Führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Execmethod-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c95bc3b0fa85d7c682f9ffd2436439da9a05763f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042364"
---
# <a name="swbemservicesexecmethod-method"></a>SWbemServices.Execmethod-Methode

Die **ExecMethod** -Methode des [**Swap Services**](swbemservices.md) -Objekts führt eine Methode aus, die von einem Methoden Anbieter exportiert wird. Diese Methode wird blockiert, während die Methode, die an den entsprechenden Anbieter weitergeleitet wird, ausgeführt wird. Die Informationen und der Status werden dann zurückgegeben. Der Anbieter implementiert die-Methode anstelle von WMI.

Diese Methode wird im synchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strobjectpath* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Objekt Pfad des Objekts enthält, für das die Methode ausgeführt wird. Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*"Name"* 
</dt> <dd>

Erforderlich. Der Name der Methode für das-Objekt.

</dd> <dt>

*objwbeminparameams* \[ optionale\]
</dt> <dd>

Ein [**-**](swbemobject.md) Objekt, das die Eingabeparameter für die ausgeführte Methode enthält. Standardmäßig ist dieser Parameter nicht definiert. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Reserviert. Dieser Wert muss null (0) sein.

</dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird ein " [**errbemujeject**](swbemobject.md) "-Objekt zurückgegeben. Das zurückgegebene-Objekt enthält die Out-Parameter und den Rückgabewert für die Methode, die ausgeführt wird.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **ExecMethod** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

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

Verwenden Sie **SWbemServices.Execmethod** als Alternative zum direkten Zugriff auf die Ausführung einer [*Anbieter Methode*](gloss-p.md) , wenn es nicht möglich ist, eine Methode direkt auszuführen. Die **ExecMethod** -Methode ermöglicht Ihnen das Abrufen von Ausgabeparametern, wenn der Anbieter Sie mit einer Skriptsprache bereitstellt, die keine Ausgabeparameter unterstützt. Andernfalls besteht die empfohlene Methode zum Aufrufen einer Methode darin, den direkten Zugriff zu verwenden. Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).

Beispielsweise verwendet das folgende Codebeispiel, das die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Anbieter Methode im [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) aufruft, den direkten Zugriff.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



In diesem Beispiel wird **SWbemServices.Execmethod** aufgerufen, um die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Methode auszuführen. Beachten Sie, dass ein Objekt Pfad erforderlich ist, weil **SWbemServices.Execmethod** im Gegensatz zu [**SWbemObject.Execmethod**](swbemobject-execmethod-.md)nicht bereits auf dem Objekt ausgeführt wird.


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



Die **SWbemServices.Execmethod** -Methode erfordert einen Objekt Pfad. Wenn das Skript bereits ein " [**errbemubject**](swbemobject.md) "-Objekt enthält, verwenden Sie die [**SWbemObject.Execmethod**](swbemobject-execmethod-.md) -Methode.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die **ExecMethod** -Methode. Das Skript erstellt ein [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekt, das einen Prozess darstellt, der Notepad ausgeführt wird. Es zeigt das Einrichten eines [**InParameters**](swbemmethod-inparameters.md) -Objekts und das Abrufen von Ergebnissen von einem [**OutParameters**](swbemmethod-outparameters.md) -Objekt. Ein Skript, das die asynchron durchgeführten Vorgänge anzeigt, finden Sie unter [**SWbemServices.Execmethodasync**](swbemservices-execmethodasync.md). Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [Create Method in \_ der Win32-Klasse](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Ein Beispiel für den gleichen Vorgang, der ein [**Swap-Objekt**](swbemobject.md)verwendet, finden Sie unter [**SWbemObject.Execmethod**](swbemobject-execmethod-.md).


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
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

[Aufrufen einer Anbieter Methode](calling-a-provider-method.md)
</dt> <dt>

[Manipulieren von Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md)
</dt> </dl>

 

