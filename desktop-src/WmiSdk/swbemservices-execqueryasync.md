---
description: 'SWbemServices.ExecQueryAsync-Methode: Führt eine Abfrage aus, um Objekte abzurufen.'
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.ExecQueryAsync-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 93b80f7571630b306951c9efddef459930b23ab66a0f1b62913836f459db8033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312649"
---
# <a name="swbemservicesexecqueryasync-method"></a>SWbemServices.ExecQueryAsync-Methode

Die **ExecQueryAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) führt eine Abfrage aus, um Objekte abzurufen. Der Aufruf dieser Methode wird sofort zurückgegeben, und die Ergebnisse und der Status werden dem Aufrufer über Ereignisse zurückgegeben, die an die Senke übermittelt werden, die in *objWbemSink* angegeben ist. Um jedes zurückgegebene Objekt zu verarbeiten, erstellen Sie einen *objWbemSink*. [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md)

Die -Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objWbemSink* \[ Optional\]
</dt> <dd>

Objektsenke, die die Abfrage asynchron ausführt. Erstellen Sie ein [**SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen.

</dd> <dt>

*strQuery* 
</dt> <dd>

Erforderlich. Zeichenfolge, die den Text der Abfrage enthält. Dieser Parameter darf nicht leer sein. Weitere Informationen zum Erstellen von WMI-Abfragezeichenfolgen finden Sie unter [Abfragen mit WQL](querying-with-wql.md) und in der [WQL-Referenz.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Optional\]
</dt> <dd>

Zeichenfolge, die die zu verwendende Abfragesprache enthält. Wenn angegeben, muss der Wert "WQL" sein.

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Ganze Zahl, die das Verhalten der Abfrage bestimmt. Dieser Parameter kann die folgenden Werte akzeptieren.

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

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype( (2 (0x2))


</dt> <dd>

Wird für einen Prototyp verwendet. Sie verhindert, dass die Abfrage stattfindet, und gibt stattdessen ein Objekt zurück, das wie ein typisches Ergebnisobjekt aussieht.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers( (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI Klassenänderungsdaten mit der Basisklassendefinition zurückgibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der Kontextinformationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ Optional\]
</dt> <dd>

Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mit derselben Objektsenke vorzunehmen. Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie vornehmen. Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode**](swbemnamedvalueset-item.md) extrahiert werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode verfügt über keine Rückgabewerte. Bei Erfolg empfängt die Senke ein [**OnObjectReady-Ereignis**](swbemsink-onobjectready.md) pro Instanz. Nach der letzten Instanz empfängt die Objektsenke ein [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ExecQueryAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen des Resultset.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

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

Dieser Aufruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden dem Aufrufer über Rückrufe zurückgegeben, die an die Senke übermittelt werden, die in *objWbemSink* angegeben ist. Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie einen *objWbemSink*. [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md) Nachdem alle Objekte zurückgegeben wurden, führen Sie die abschließende Verarbeitung in Ihrer Implementierung von *objWbemSink* aus. [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke bereitzustellen. Dies stellt Sicherheitsrisiken für Ihre Skripts und Anwendungen dar. Informationen zum Beseitigen der Risiken finden Sie unter [Festlegen der Sicherheit bei einem asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

Die **ExecQueryAsync-Methode** gibt ein leeres Resultset zurück, wenn keine Objekte vorhanden sind, die den Kriterien in der Abfrage entsprechen. Diese Methode gibt Schlüsseleigenschaften zurück, unabhängig davon, ob die [**Key-Eigenschaft**](standard-qualifiers.md) im *strQuery-Parameter* angefordert wird.

Die Anzahl von **AND-** und OR-Schlüsselwörtern, die in WQL-Abfragen verwendet werden können, ist begrenzt.  Eine große Anzahl von WQL-Schlüsselwörtern, die in einer komplexen Abfrage verwendet werden, kann dazu führen, dass WMI den WBEM \_ E \_ QUOTA \_ VIOLATION-Fehlercode als **HRESULT-Wert** zurückgibt. Die Beschränkung der WQL-Schlüsselwörter hängt davon ab, wie komplex die Abfrage ist.

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

[Aufrufen einer Methode](calling-a-method.md)
</dt> <dt>

[**SWbemServices.Get**](swbemservices-get.md)
</dt> </dl>

 

