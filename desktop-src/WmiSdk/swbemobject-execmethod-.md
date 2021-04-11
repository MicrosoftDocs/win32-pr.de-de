---
description: Die ExecMethod- \_ Methode des errbemubject-Objekts führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: SWbemObject.ExecMethod_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130984"
---
# <a name="swbemobjectexecmethod_-method"></a>SWbemObject.Execmethod- \_ Methode

Die **ExecMethod \_** -Methode des [**errbemubject**](swbemobject.md) -Objekts führt eine Methode aus, die von einem Methoden Anbieter exportiert wird.

Diese Methode wird angehalten, während die an den entsprechenden Anbieter weitergeleitete Methode ausgeführt wird. Die Informationen und der Status werden dann zurückgegeben. Der Anbieter implementiert die-Methode anstelle von WMI.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name der Methode für das-Objekt.

</dd> <dt>

*objwbeminparameams* \[ in, optional\]
</dt> <dd>

Hierbei handelt es sich um ein Objekt vom [**typaustausch**](swbemobject.md) , das die Eingabeparameter für die Methode enthält, die ausgeführt wird. Standardmäßig ist dieser Parameter nicht definiert. Weitere Informationen finden Sie unter [Erstellen von inparameter-Objekten und Überprüfen von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert und muss auf 0 (null) festgelegt werden, wenn angegeben.

</dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

In der Regel ist Sie nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, gibt ein [**Swap**](swbemobject.md) -Objekt zurück. Das zurückgegebene-Objekt enthält die Out-Parameter und den Rückgabewert für die Methode, die ausgeführt wird.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **ExecMethod \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

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

Diese Methode ähnelt [**SWbemServices.Execmethod**](swbemservices-execmethod.md), funktioniert jedoch direkt mit dem Objekt, dessen-Methode ausgeführt werden soll. Im folgenden Codebeispiel wird die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Anbieter Methode im Win32- [**\_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) aufgerufen und der [direkte Zugriff](manipulating-class-and-instance-information.md)verwendet.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Diese Version ruft **SWbemObject.Execmethod \_** auf, um die [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) -Methode auszuführen.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



Verwenden Sie **SWbemObject.Execmethod \_** als Alternative zum direkten Zugriff auf die Ausführung einer [*Anbieter Methode*](gloss-p.md) , wenn es nicht möglich ist, eine Methode direkt auszuführen. Beispielsweise können Sie **SWbemObject.Execmethod \_** mit einer Skriptsprache verwenden, die keine Ausgabeparameter unterstützt, wenn die Methode out-Parameter aufweist. Andernfalls besteht die empfohlene Methode zum Aufrufen einer Methode darin, den direkten Zugriff zu verwenden.

-   Die **SWbemObject.Execmethod \_** -Methode geht davon aus, dass [**das durch das**](swbemobject.md) -Objekt dargestellte Objekt die auszuführende Methode enthält. Im Gegensatz dazu erfordert [**SWbemServices.Execmethod**](swbemservices-execmethod.md) einen Objekt Pfad. Verwenden Sie **SWbemObject.Execmethod \_** , wenn Sie bereits das Objekt abgerufen haben, dessen Methode Sie ausführen möchten.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die [**ExecMethod**](swbemservices-execmethod.md) -Methode. Das Skript erstellt ein [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Objekt, das einen Prozess darstellt, der Editor ausgeführt wird. Weitere Informationen zu einem Skript, das die asynchron durchgeführten Vorgänge veranschaulicht, finden Sie unter [**SWbemObject.Execmethodasync \_**](swbemobject-execmethodasync-.md). Ein Beispiel für die Verwendung des direkten Zugriffs finden Sie unter [**Create method \_ in der Win32-Klasse**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Ein Beispiel für denselben Vorgang mit einem " [**Swap Services**](swbemservices.md) "-Objekt finden Sie unter **SWbemServices.Execmethod**.


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
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
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
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
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Objekt**](swbemobject.md)
</dt> <dt>

[**SWbemObject.Execmethodasync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.Execmethod**](swbemservices-execmethod.md)
</dt> </dl>

 

