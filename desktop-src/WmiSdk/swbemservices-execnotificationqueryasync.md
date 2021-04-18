---
description: Führt eine Abfrage zum Empfangen von Ereignissen aus.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Execnotificationqueryasync-Methode (wbemdisp. h)
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
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347309"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a>SWbemServices.Execnotificationqueryasync-Methode

Die **ExecNotificationQueryAsync** -Methode des-Objekts " [**Swap-Dienste**](swbemservices.md) " führt eine Abfrage zum Empfangen von Ereignissen aus. Dieser Aufruf wird sofort zurückgegeben, und die Ergebnisse und der Status werden über Ereignisse an die Senke, die in *objwbemsink* angegeben ist, an den Aufrufer zurückgegeben.

Die in der Abfrage angegebenen Ereignisse können systeminterne Windows-Verwaltungsinstrumentation (WMI)-Ereignisse (z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md)) oder extrinsische Ereignisse wie z. b. [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) oder [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)sein. Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

Die-Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

*objwbemsink* 
</dt> <dd>

Erforderlich. Objekt Senke, die die Benachrichtigung über Ereignisse asynchron empfängt. Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.

</dd> <dt>

*"-Abfrage"* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Text der ereignisbezogenen Abfrage enthält. Dieser Parameter darf nicht leer sein. Weitere Informationen zum Aufbau von WMI-Abfrage Zeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und [WQL](wql-sql-for-wmi.md) -Referenz.

</dd> <dt>

"in der *Sprache* \[ " optionale\]
</dt> <dd>

Eine Zeichenfolge, die die zu verwendende Abfragesprache enthält. Wenn angegeben, muss dieser Wert "WQL" lauten.

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten der Abfrage bestimmt. Dieser Parameter kann auf die folgenden Werte festgelegt werden.

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

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> <dt>

*objwbemasynccontext* \[ optionale\]
</dt> <dd>

Dabei handelt es sich um ein Objekt vom Typ " [**taubemnamedvalueset**](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen. Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke auszuführen. Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert. Das Objekt " **taubemnamedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz. Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **ExecNotificationQueryAsync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der in der folgenden Liste identifizierten Fehlercodes enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer ist nicht autorisiert, das Resultset anzuzeigen.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrInvalidQuery** -2147749911 (0x80041017)
</dt> <dd>

Die Abfrage Syntax ist ungültig.

</dd> <dt>

**wbemErrInvalidQueryType** -2147749912 (0x80041018)
</dt> <dd>

Die angeforderte Abfragesprache wird nicht unterstützt.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **ExecNotificationQueryAsync** -Methode gibt Ereignistyp Objekte zurück, die von zukünftigen Ereignissen generiert werden. Die Ereignis Objekte, die **ExecNotificationQueryAsync** -Anforderungen haben, können System intern (z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md)) oder System externe (z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) -oder SNMP-Ereignisse) sein. Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

Der Aufruf von **ExecNotificationQueryAsync** wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist. Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine. Nachdem alle Objekte zurückgegeben wurden, führen Sie die endgültige Verarbeitung aus, um die *objwbemsink*-Komponente zu implementieren. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, finden Sie weitere Informationen unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können. Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den Wert für die **WBEM \_ E- \_ Kontingent \_ Verletzungs** Fehlercode- **HRESULT** Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel wird ein Skript gezeigt, das auf eine WMI-Ereignis Benachrichtigung wartet, die angibt, dass ein Prozess beendet wurde. Er wartet auf ein System eigenes WMI-Ereignis, eine Instanz der Ereignisklasse [**\_ \_ instancedeletionevent**](--instancedeletionevent.md). Das **\_ \_ instancedeletionevent** muss das Löschen einer Instanz des Win32- [**\_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process)darstellen. Weitere Informationen zu systeminternen WMI-Ereignissen finden [Sie unter Bestimmen des zu empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).

Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden. Verwenden Sie zum programmgesteuerten beenden die Methode " [**Beenden**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) " in der Win32- \_ Prozess Klasse.


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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austauschdienste<br/>                                                         |
| IID<br/>                      | IID \_ iswbemservices<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**CquerySWbemServices.Exe**](swbemservices-execquery.md)
</dt> <dt>

[**CqueryasyncSWbemServices.Exe**](swbemservices-execqueryasync.md)
</dt> <dt>

[Registrierung für System Registrierungs Ereignisse](registering-for-system-registry-events.md)
</dt> <dt>

[Bestimmen des zu empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> <dt>

[Festlegen der Sicherheit für einen asynchronen-Befehl](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

