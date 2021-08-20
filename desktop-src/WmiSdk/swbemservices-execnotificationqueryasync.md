---
description: Führt eine Abfrage zum Empfangen von Ereignissen aus.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.ExecNotificationQueryAsync-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0f6c02be1be258f84afcbc941dafdaae6b492f995c25d9718ddbf719c347ae27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108034"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a>SWbemServices.ExecNotificationQueryAsync-Methode

Die **ExecNotificationQueryAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) führt eine Abfrage aus, um Ereignisse zu empfangen. Dieser Aufruf wird sofort zurückgegeben, und die Ergebnisse und der Status werden dem Aufrufer über Ereignisse zurückgegeben, die an die Senke übermittelt werden, die in *objWbemSink* angegeben ist.

Die in der Abfrage angegebenen Ereignisse können systeminterne Windows WMI-Ereignisse (Management Instrumentation, Verwaltungsinstrumentation) wie [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)oder extrinsische Ereignisse wie [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) oder [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)sein. Weitere Informationen finden Sie unter [Bestimmen des Typs des zu empfangenden Ereignisses.](determining-the-type-of-event-to-receive.md)

Die -Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Erforderlich. Objektsenke, die die Benachrichtigung über Ereignisse asynchron empfängt. Erstellen Sie ein [**SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen.

</dd> <dt>

*strQuery* 
</dt> <dd>

Erforderlich. Zeichenfolge, die den Text der ereignisbezogenen Abfrage enthält. Dieser Parameter darf nicht leer sein. Weitere Informationen zum Erstellen von WMI-Abfragezeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und in der [WQL-Referenz.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Optional\]
</dt> <dd>

Zeichenfolge, die die zu verwendende Abfragesprache enthält. Wenn angegeben, muss dieser Wert "WQL" sein.

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Ganze Zahl, die das Verhalten der Abfrage bestimmt. Dieser Parameter kann auf die folgenden Werte festgelegt werden.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus( (128 (0x80))


</dt> <dd>

Bewirkt, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus( (0 (0x0))


</dt> <dd>

Verhindert, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ Optional\]
</dt> <dd>

Dies ist ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mit derselben Objektsenke vorzunehmen. Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie vornehmen. Das **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode**](swbemnamedvalueset-item.md) extrahiert werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei Erfolg empfängt die Senke ein [**OnObjectReady-Ereignis**](swbemsink-onobjectready.md) pro Instanz. Nach der letzten Instanz empfängt die Objektsenke ein [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ExecNotificationQueryAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der in der folgenden Liste identifizierten Fehlercodes enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer ist nicht berechtigt, das Resultset anzuzeigen.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Es wird ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrInvalidQuery** – 2147749911 (0x80041017)
</dt> <dd>

Die Abfragesyntax ist ungültig.

</dd> <dt>

**wbemErrInvalidQueryType** – 2147749912 (0x80041018)
</dt> <dd>

Die angeforderte Abfragesprache wird nicht unterstützt.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **ExecNotificationQueryAsync-Methode** gibt Ereignistypobjekte zurück, die zukünftige Ereignisse generieren. Die Ereignisobjekte, die **ExecNotificationQueryAsync** anfordert, können systeminterne (z. [**\_ \_ B. InstanceCreationEvent)**](--instancecreationevent.md)oder extrinsisch (z. B. [**RegistryKeyChangeEvent-**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) oder SNMP-Ereignisse) sein. Weitere Informationen finden Sie unter [Bestimmen des Typs des zu empfangenden Ereignisses.](determining-the-type-of-event-to-receive.md)

Der Aufruf von **ExecNotificationQueryAsync** wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden dem Aufrufer über Rückrufe zurückgegeben, die an die Senke übermittelt werden, die in *objWbemSink* angegeben ist. Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie einen *objWbemSink*. [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md) Nachdem alle Objekte zurückgegeben wurden, führen Sie die abschließende Verarbeitung aus, um *objWbemSink* zu implementieren. [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke bereitzustellen. Dies stellt Sicherheitsrisiken für Ihre Skripts und Anwendungen dar. Informationen zum Beseitigen der Risiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

Die Anzahl von **AND-** und OR-Schlüsselwörtern, die in WQL-Abfragen verwendet werden können, ist begrenzt.  Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den **WBEM \_ E \_ QUOTA \_ VIOLATION-Fehlercode** als **HRESULT-Wert** zurückgibt. Die Beschränkung der WQL-Schlüsselwörter hängt davon ab, wie komplex die Abfrage ist.

## <a name="examples"></a>Beispiele

Das folgende VBScript-Codebeispiel zeigt ein Skript, das auf eine WMI-Ereignisbenachrichtigung wartet, die angibt, dass ein Prozess beendet wurde. Sie wartet auf ein systeminternes WMI-Ereignis, eine Instanz der Ereignisklasse [**\_ \_ InstanceDeletionEvent.**](--instancedeletionevent.md) **\_ \_ InstanceDeletionEvent** muss das Löschen einer Instanz von [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process)darstellen. Weitere Informationen zu systeminternen WMI-Ereignissen finden Sie unter [Bestimmen des Typs des zu empfangenden Ereignisses.](determining-the-type-of-event-to-receive.md)

Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Verwenden Sie zum programmgesteuerten Beenden die [**Terminate-Methode**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) in der Win32 \_ Process-Klasse.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swbemservices**](swbemservices.md)
</dt> <dt>

[**SWbemServices.ExecQuery**](swbemservices-execquery.md)
</dt> <dt>

[**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
</dt> <dt>

[Registrieren für Systemregistrierungsereignisse](registering-for-system-registry-events.md)
</dt> <dt>

[Bestimmen des Zu empfangenden Ereignistyps](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> <dt>

[Festlegen der Sicherheit für einen asynchronen Aufruf](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

