---
description: 'SWbemServices.AssociatorsOfAsync-Methode: Gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die Endpunkte genannt werden, die einem angegebenen Objekt zugeordnet sind.'
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: SWbemServices.AssociatorsOfAsync-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebc607bf10be8b94fa5274e5539953344c99c263db13dec6f8982146f60f4551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991790"
---
# <a name="swbemservicesassociatorsofasync-method"></a>SWbemServices.AssociatorsOfAsync-Methode

Die **AssociatorsOfAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die als Endpunkte bezeichnet werden, die einem angegebenen Objekt zugeordnet sind. Der Aufruf von **AssociatorsOfAsync** wird sofort zurückgegeben, und die Ergebnisse und der Status werden an den Aufrufer zurückgegeben, indem Ereignisse an die Senke übermittelt werden, die in *objWbemSink angegeben ist.* Um jedes zurückgegebene Objekt zu verarbeiten, erstellen Sie *ein objWbemSink -Objekt.* [**OnObjectReady-Ereignishandler.**](swbemsink-onobjectready.md)

Nachdem alle Objekte eintreffen, wird die Verarbeitung im *objWbemSink-Objekt durchgeführt.* [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md) Diese Methode führt dieselbe Funktion aus wie die ASSOCIATORS OF WQL-Abfrage. Weitere Informationen zum Erstellen einer Senke finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md)

Die -Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Erforderlich. Objektsenke, die die Objekte asynchron empfängt. Erstellen Sie ein [**SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Objektpfad der Quellklasse oder -instanz enthält. Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*strAssocClass* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die eine Zuordnungsklasse enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte der Quelle über die angegebene Zuordnungsklasse oder eine von dieser Zuordnungsklasse abgeleitete Klasse zugeordnet werden müssen.

</dd> <dt>

*strResultClass* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser optionale Parameter an, dass die zurückgegebenen Endpunkte zu der in diesem Parameter angegebenen Klasse gehören oder von ihr abgeleitet werden müssen.

</dd> <dt>

*strResultRole* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Eigenschaftennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte in ihrer Zuordnung zum Quellobjekt eine bestimmte Rolle spielen müssen. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*strRole* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Eigenschaftennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung zum Quellobjekt teilnehmen müssen, in dem das Quellobjekt eine bestimmte Rolle spielt. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweiseigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*bClassesOnly* \[ Optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob anstelle der tatsächlichen Instanzen der Klassen eine Liste von Klassennamen zurückgegeben werden soll. Dies sind die Klassen, zu denen die Endpunktinstanzen gehören. Der Standardwert für diesen Parameter ist **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Abfrage für das Schema und nicht für die Daten gilt. Der Standardwert für diesen Parameter ist **FALSE.** Sie kann nur auf **TRUE festgelegt werden,** wenn der *parameter strObjectPath* den Objektpfad einer Klasse angibt. Bei True **stellen die** zurückgegebenen Endpunkte Klassen dar, die der Quellklasse im Schema entsprechend zugeordnet sind.

</dd> <dt>

*strRequiredAssocQualifier* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte dem Quellobjekt über eine Zuordnungsklasse zugeordnet werden müssen, die den angegebenen Qualifizierer enthält.

</dd> <dt>

*strRequiredQualifier* \[ Optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer enthalten müssen.

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Eine ganze Zahl, die die zusätzlichen Flags für den Vorgang angibt. Der Standardwert für diesen Parameter ist **wbemFlagDontSendStatus.** Dieser Parameter kann die folgenden Werte akzeptieren.

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

Bewirkt, dass WMI Klassenänderungsdaten zusammen mit der Basisklassendefinition zurück gibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ Optional\]
</dt> <dd>

Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mit derselben Objektsenke ausführen. Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Aufruf identifiziert. Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode extrahiert**](swbemnamedvalueset-item.md) werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei Erfolg empfängt die Senke ein [**OnObjectReady-Ereignis**](swbemsink-onobjectready.md) pro Instanz. Nach der letzten Instanz empfängt die Objektsenke ein [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **AssociatorsOfAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

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

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das angeforderte Element wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieser Aufruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden an den Aufrufer über Rückrufe zurückgegeben, die an die in *objWbemSink* angegebene Senke übermittelt werden. Um jedes Objekt nach der Rückgabe zu verarbeiten, erstellen Sie *ein objWbemSink -Objekt.* [**OnObjectReady-Ereignisunterroutine.**](swbemsink-onobjectready.md) Nachdem alle -Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in Ihrer Implementierung von *objWbemSink ausführen.* [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Informationen zum Beseitigen der Risiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

Verwenden Sie *den parameter objWbemAsyncContext* in Skripts, um die Quelle eines Aufrufs zu überprüfen.

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

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.AssociatorsAsync\_**](swbemobject-associatorsasync-.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemObject.ReferencesAsync\_**](swbemobject-referencesasync-.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices.ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

