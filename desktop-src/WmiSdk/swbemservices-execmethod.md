---
description: 'SWbemServices.ExecMethod-Methode: Führt eine Methode aus, die von einem Methodenanbieter exportiert wird.'
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.ExecMethod-Methode (Wbemdisp.h)
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
ms.openlocfilehash: e8cce3f7f190ded1b86fef5ea5b43016d5f8b08ebc9c1e5483280a2b4305200a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995596"
---
# <a name="swbemservicesexecmethod-method"></a>SWbemServices.ExecMethod-Methode

Die **ExecMethod-Methode** des [**SWbemServices-Objekts**](swbemservices.md) führt eine Methode aus, die von einem Methodenanbieter exportiert wird. Diese Methode blockiert, während die Methode ausgeführt wird, die an den entsprechenden Anbieter weitergeleitet wird. Die Informationen und der Status werden dann zurückgegeben. Der Anbieter implementiert anstelle von WMI die -Methode.

Diese Methode wird im synchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

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

*strObjectPath* 
</dt> <dd>

Erforderlich. Zeichenfolge, die den Objektpfad des Objekts enthält, für das die Methode ausgeführt wird. Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*strMethodName* 
</dt> <dd>

Erforderlich. Name der Methode für das Objekt.

</dd> <dt>

*objWbemInParams* \[ Optional\]
</dt> <dd>

Ein [**SWbemObject-Objekt,**](swbemobject.md) das die Eingabeparameter für die ausgeführte Methode enthält. Dieser Parameter ist standardmäßig nicht definiert. Weitere Informationen finden Sie unter [Erstellen von InParameters-Objekten und Analysieren von OutParameters-Objekten.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Reserviert. Dieser Wert muss null (0) sein.

</dd> <dt>

*objWbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung wartet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird ein [**SWbemObject-Objekt**](swbemobject.md) zurückgegeben. Das zurückgegebene -Objekt enthält die out-Parameter und den Rückgabewert für die Methode, die ausgeführt wird.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ExecMethod-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

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

Verwenden Sie **SWbemServices.ExecMethod** als Alternative zum direkten Zugriff für die Ausführung einer [*Anbietermethode*](gloss-p.md) in Fällen, in denen es nicht möglich ist, eine Methode direkt auszuführen. Mit der **ExecMethod-Methode** können Sie Ausgabeparameter abrufen, wenn sie vom Anbieter bereitgestellt werden, mit einer Skriptsprache, die keine Ausgabeparameter unterstützt. Andernfalls wird empfohlen, einen direkten Zugriff zu verwenden, um eine Methode auf den Weg zu bringen. Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen.](manipulating-class-and-instance-information.md)

Das folgende Codebeispiel, das die [**StartService-Anbietermethode**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) in [**Win32 \_ Service**](/windows/desktop/CIMWin32Prov/win32-service) aufruft, verwendet beispielsweise direkten Zugriff.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



In diesem Beispiel **wirdSWbemServices.ExecMethod** aufgerufen, um die [**StartService-Methode**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) auszuführen. Beachten Sie, dass ein Objektpfad erforderlich ist, da **SWbemServices.ExecMethod** im Gegensatz zu [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md)nicht bereits für das Objekt verwendet wird.


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



Die **SWbemServices.ExecMethod-Methode** erfordert einen Objektpfad. Wenn das Skript bereits ein [**SWbemObject-Objekt**](swbemobject.md) enthält, verwenden Sie die [**SWbemObject.ExecMethod-Methode.**](swbemobject-execmethod-.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die **ExecMethod-Methode.** Das Skript erstellt ein [**\_ Win32-Prozessobjekt,**](/windows/desktop/CIMWin32Prov/win32-process) das einen Prozess darstellt, der Editor ausgeführt wird. Es zeigt die Einrichtung eines [**InParameters-Objekts**](swbemmethod-inparameters.md) und das Abrufen von Ergebnissen aus einem [**OutParameters-Objekt.**](swbemmethod-outparameters.md) Ein Skript, das die gleichen asynchron ausgeführten Vorgänge anzeigt, finden Sie unter [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md). Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Ein Beispiel für den gleichen Vorgang mit einem [**SWbemObject**](swbemobject.md)finden Sie unter [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


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

[Aufrufen einer Anbietermethode](calling-a-provider-method.md)
</dt> <dt>

[Bearbeiten von Klassen- und Instanzinformationen](manipulating-class-and-instance-information.md)
</dt> </dl>

 

