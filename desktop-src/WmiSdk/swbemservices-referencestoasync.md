---
description: Gibt alle Zuordnungsklassen oder -instanzen zurück, die auf eine bestimmte Quellklasse oder -instanz verweisen.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: SWbemServices.ReferencesToAsync-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 98b2ab6963bf547b3fbf8321fde37359264286f77da98697f5ef88cc145be2e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794390"
---
# <a name="swbemservicesreferencestoasync-method"></a>SWbemServices.ReferencesToAsync-Methode

Die **ReferencesToAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) gibt alle Zuordnungsklassen oder -instanzen zurück, die auf eine bestimmte Quellklasse oder Instanz verweisen. Diese Methode führt dieselbe Funktion aus wie die [REFERENCES OF](references-of-statement.md) WQL-Abfrage.

Weitere Informationen zum asynchronen Modus finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ObjWbemSink* 
</dt> <dd>

Erforderlich. Objektsenke, die die Objekte asynchron empfängt. Erstellen Sie [**ein SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Objektpfad der Quelle für diese Methode enthält. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> <dt>

*strResultClass* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte zu der in diesem Parameter angegebenen Klasse gehören oder von dieser abgeleitet werden müssen.

</dd> <dt>

*strRole* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Eigenschaftennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte auf diejenigen beschränkt werden müssen, in denen das Quellobjekt eine bestimmte Rolle spielt. Die Rolle wird durch den Namen einer angegebenen Verweiseigenschaft einer Zuordnung definiert.

</dd> <dt>

*bClassesOnly* \[ Optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob anstelle der tatsächlichen Instanzen der Klassen eine Liste von Klassennamen zurückgegeben werden soll. Dies sind die Klassen, zu denen die Zuordnungsobjekte gehören. Der Standardwert für diesen Parameter ist **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Optional\]
</dt> <dd>

Ein boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird. Der Standardwert für diesen Parameter ist **FALSE.** Sie kann nur auf **TRUE festgelegt werden,** wenn der *parameter strObjectPath* den Objektpfad einer Klasse angibt. Wenn auf **TRUE festgelegt,** stellt der Satz zurückgegebener Endpunkte Klassen dar, die der Quellklasse im Schema zugeordnet sind.

</dd> <dt>

*strRequiredQualifier* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungsobjekte den angegebenen Qualifizierer enthalten müssen.

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt. Der Standardwert für diesen Parameter ist **wbemFlagBidirectional.** Dieser Parameter kann die folgenden Werte akzeptieren.

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

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers** (131072 (0x20000))


</dt> <dd>

Bewirkt, Windows Management Instrumentation (WMI) Klassenänderungsdaten zusammen mit der Basisklassendefinition zurück gibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der Kontextinformationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ Optional\]
</dt> <dd>

Dies ist ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, um mehrere asynchrone Aufrufe mit derselben Objektsenke zu tätigen. Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie ausführen. Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode extrahiert**](swbemnamedvalueset-item.md) werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei Erfolg empfängt die Senke ein [**OnObjectReady-Ereignis**](swbemsink-onobjectready.md) pro Instanz. Nach der letzten Instanz empfängt die Objektsenke ein [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **ReferencesToAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

> [!Note]  
> Eine zurückgegebene Auflistung mit null Elementen ist kein Fehler.

 

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

Dieser Aufruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden an den Aufrufer über Rückrufe zurückgegeben, die an die in *objWbemSink* angegebene Senke übermittelt werden. Um jedes Objekt nach der Rückgabe zu verarbeiten, erstellen Sie *ein objWbemSink -Objekt.* [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md) Nachdem alle -Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in Ihrer Implementierung von *objWbemSink ausführen.* [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Informationen zum Beseitigen der Risiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

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

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-referencesto.md)
</dt> </dl>

 

