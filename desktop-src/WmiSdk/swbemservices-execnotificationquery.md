---
description: Führt eine Abfrage zum Empfangen von Ereignissen aus. Der-Rückruf wird sofort zurückgegeben.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: SWbemServices.Execnotificationquery-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363518"
---
# <a name="swbemservicesexecnotificationquery-method"></a>SWbemServices.Execnotificationquery-Methode

Die **ExecNotificationQuery** -Methode des [**Swap Services**](swbemservices.md) -Objekts führt eine Abfrage zum Empfangen von Ereignissen aus. Der-Rückruf wird sofort zurückgegeben. Der Benutzer kann den zurückgegebenen Enumerator nach Ereignissen abrufen, sobald sie eintreffen.

Die-Methode wird im semisynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

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

Dies ist eine ganze Zahl, die das Verhalten der Abfrage bestimmt. Der Standardwert ist **wbemFlagReturnImmediately**  +  **wbemFlagForwardOnly**. Wenn Sie diesen Parameter angeben, muss dieser Parameter sowohl auf **wbemFlagReturnImmediately** als auch auf **wbemFlagForwardOnly** festgelegt werden, andernfalls tritt ein Fehler auf. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Bewirkt, dass ein vorwärts-Enumerator zurückgegeben wird. Vorwärts-Enumeratoren sind in der Regel viel schneller und verbrauchen weniger Arbeitsspeicher als herkömmliche Enumeratoren, aber Sie lassen keine Aufrufe von " [**errbemubject. Clone \_**](swbemobject-clone-.md)" zu.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Bewirkt, dass der-Rückruf sofort zurückgegeben wird.

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn kein Fehler auftritt, gibt diese Methode ein " [**errbemeventsource**](swbemeventsource.md) "-Objekt zurück. Sie können die Methode " [**errbemeventsource. NextEvent**](swbemeventsource-nextevent.md) " aufrufen, um Ereignisse abzurufen, sobald sie eintreffen.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **ExecNotificationQuery** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

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

Anders als bei der [**SWbemServices.Execqueryasync**](swbemservices-execqueryasync.md) -Methode gibt **ExecNotificationQuery** Ereignistyp Objekte zurück, die von zukünftigen Ereignissen generiert werden, und nicht von vorhandenen Objekten. Die Ereignis Objekte, die von **ExecNotificationQuery** angefordert werden, können System intern (z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md)) oder Extrinsisch (z. b. Registrierungs Anbieter Ereignisse wie z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) oder SNMP-Ereignisse) sein. Weitere Informationen finden Sie unter [bestimmen des Ereignis Typs zum empfangen](determining-the-type-of-event-to-receive.md) und [empfangen von Ereignis Benachrichtigungen](receiving-event-notifications.md).

Es gibt Einschränkungen für die Anzahl von **-** und- **oder** -Schlüsselwörtern, die in WQL-Abfragen verwendet werden können. Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann bewirken, dass WMI den Fehlercode der **WBEM \_ E- \_ Kontingent \_ Verletzung** als **HRESULT** -Wert zurückgibt Das Limit von WQL-Schlüsselwörtern hängt von der Komplexität der Abfrage ab.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden Änderungen an Volumes auf einem lokalen Computer überwacht. Beachten Sie, dass [**Win32 \_ volumechangeevent**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) ein extrinsisches Ereignis ist, das von einem Anbieter definiert wird, der kein System internes, von WMI definiertes Ereignis ist. Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



Im folgenden VBScript-Codebeispiel wird der Prozess Löschvorgang überwacht. Wenn Sie einen Prozess im Task-Manager löschen oder eine Anwendung schließen, zeigt das Skript eine Meldung an. Beachten Sie, dass dieses Skript ein System internes Ereignis abfragt, das von WMI- [**\_ \_ instancedeletionevent**](--instancedeletionevent.md)definiert wird.


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
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

[**"Errbemeventsource. NextEvent"**](swbemeventsource-nextevent.md)
</dt> <dt>

[**CquerySWbemServices.Exe**](swbemservices-execquery.md)
</dt> <dt>

[Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)
</dt> <dt>

[Abfragen mit WQL](querying-with-wql.md)
</dt> <dt>

[WQL (SQL für WMI)](wql-sql-for-wmi.md)
</dt> <dt>

[Bestimmen des zu empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

