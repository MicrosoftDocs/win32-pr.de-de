---
description: Die ReferencesAsync-Methode von SWbemObject stellt eine Auflistung aller Zuordnungsklassen oder -instanzen zur Anwendung, \_ die auf das aktuelle Objekt verweisen. Diese Methode führt dieselbe Funktion aus wie die WQL REFERENCES OF-Abfrage.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: SWbemObject.ReferencesAsync_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
- ISWbemObject.ReferencesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 551a54430724e52ede0ee0000ac48a8593f4145e2a875766c61da9c24de45c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640070"
---
# <a name="swbemobjectreferencesasync_-method"></a>SWbemObject.ReferencesAsync-Methode \_

Die **ReferencesAsync-Methode \_** von [**SWbemObject**](swbemobject.md) stellt eine Auflistung aller Zuordnungsklassen oder -instanzen zur Anwendung, die auf das aktuelle Objekt verweisen. Diese Methode führt dieselbe Funktion aus wie die WQL [REFERENCES OF-Abfrage.](references-of-statement.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemObject.ReferencesAsync_( _
  ByVal objWbemSink, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objWbemSink* \[ In\]
</dt> <dd>

Erforderlich. Objektsenke, die die Objekte asynchron empfängt.

</dd> <dt>

*strResultClass* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte zu der in diesem Parameter angegebenen Klasse gehören oder von dieser abgeleitet werden müssen.

</dd> <dt>

*strRole* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Eigenschaftennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte auf diejenigen beschränkt werden müssen, in denen das Quellobjekt eine bestimmte Rolle spielt. Der Name einer angegebenen Verweiseigenschaft definiert die Rolle einer Zuordnung.

</dd> <dt>

*bClassesOnly* \[ in, optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob anstelle der tatsächlichen Instanzen der Klassen eine Liste von Klassennamen zurückgegeben werden soll. Dies sind die Klassen, zu denen die Zuordnungsobjekte gehören. Der Standardwert für diesen Parameter ist **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ in, optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird. Der Standardwert für diesen Parameter ist **FALSE.** Sie kann nur auf **TRUE festgelegt werden,** wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist. Bei True **stellt der** Satz zurückgegebener Endpunkte Klassen dar, die der Quellklasse im Schema entsprechend zugeordnet sind.

</dd> <dt>

*strRequiredQualifier* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte den angegebenen Qualifizierer enthalten müssen.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Ganze Zahl, die zusätzliche Flags für den Vorgang angibt. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Bewirkt, dass asynchrone Aufrufe Statusupdates an den [**SWbemSink.OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** (0 (0x0))


</dt> <dd>

Verhindert, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Bewirkt, Windows Management Instrumentation (WMI) Klassenänderungsdaten mit der Basisklassendefinition zurück gibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [SWbemNamedValueSet-Objekt,](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ in, optional\]
</dt> <dd>

Dies ist ein [SWbemNamedValueSet-Objekt,](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mit derselben Objektsenke ausführen. Um diesen Parameter zu verwenden, erstellen Sie ein SWbemNamedValueSet-Objekt, und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie ausführen. Dieses SWbemNamedValueSet-Objekt wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode extrahiert**](swbemnamedvalueset-item.md) werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei Erfolg empfängt die Senke ein [**OnObjectReady-Ereignis**](swbemsink-onobjectready.md) pro Instanz. Nach der letzten Instanz empfängt die Objektsenke ein [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ReferencesAsync-Methode \_** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung, eine oder mehrere der vom Aufruf zurückgegebenen Klassen anzeigen zu können.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ungültiger Parameter wurde angegeben.

</dd> <dt>

**wbemErrOutOfMemory** : 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieser Aufruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden an den Aufrufer über Rückrufe zurückgegeben, die an die in *objWbemSink* angegebene Senke übermittelt werden. Um jedes Objekt zu verarbeiten, wenn es eintrifft, erstellen Sie *einen objWbemSink*. [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md) Nachdem alle -Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in Ihrer Implementierung von *objWbemSink ausführen.* [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken zu beseitigen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Weitere Informationen zu den REFERENCES OF zugeordneten WQL-Abfragen, Quellinstanzen und Zuordnungsobjekten finden Sie unter [ASSOCIATORS OF Statement](associators-of-statement.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices.ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

