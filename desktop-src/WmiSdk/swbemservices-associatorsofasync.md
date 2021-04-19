---
description: Gibt eine Auflistung von-Objekten (Klassen oder Instanzen) zurück, die als Endpunkte bezeichnet werden, die einem angegebenen Objekt zugeordnet sind.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Swap Services. associatorsofasync-Methode (wbemdisp. h)
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
ms.openlocfilehash: d83f2eb33b7cd2d6ce6345d9b40a2367539dfec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356615"
---
# <a name="swbemservicesassociatorsofasync-method"></a>Methode "Swap Services. associatorsofasync"

Die **associatorsofasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts gibt eine Auflistung von Objekten (Klassen oder Instanzen) zurück, die als Endpunkte bezeichnet werden, die einem angegebenen Objekt zugeordnet sind. Der Aufruf von **associatorsofasync** wird sofort zurückgegeben, und die Ergebnisse und der Status werden an den Aufrufer über Ereignisse gesendet, die an die in *objwbemsink* angegebene Senke gesendet werden. Um jedes zurückgegebene Objekt zu verarbeiten, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignishandler.

Nachdem alle Objekte eintreffen, erfolgt die Verarbeitung in der *objwbemsink*. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis. Diese Methode führt die gleiche Funktion aus, die die assoziatoren der WQL-Abfrage ausführen. Weitere Informationen zum Erstellen einer Senke finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).

Die-Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

*objwbemsink* 
</dt> <dd>

Erforderlich. Objekt Senke, die die-Objekte asynchron empfängt. Erstellen Sie ein " [**taubemsink**](swbemsink.md) "-Objekt zum Empfangen der Objekte.

</dd> <dt>

*strobjectpath* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Objekt Pfad der Quell Klasse oder-Instanz enthält. Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strassocclass* \[ optionale\]
</dt> <dd>

Eine Zeichenfolge, die eine Association-Klasse enthält. Wenn dieser Parameter angegeben wird, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte mit der Quelle über die angegebene Zuordnungs Klasse oder eine von dieser Zuordnungs Klasse abgeleitete Klasse verknüpft werden müssen.

</dd> <dt>

" *strautclass* \[ " optionale\]
</dt> <dd>

Eine Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser optionale Parameter an, dass die zurückgegebenen Endpunkte zu der in diesem Parameter angegebenen Klasse gehören bzw. davon abgeleitet werden müssen.

</dd> <dt>

" *stringetrole* \[ " optionale\]
</dt> <dd>

Eine Zeichenfolge, die einen Eigenschaftsnamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte eine bestimmte Rolle in ihrer Zuordnung zum Quell Objekt spielen müssen. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*Rolle "Rolle* \[ " optionale\]
</dt> <dd>

Eine Zeichenfolge, die einen Eigenschaftsnamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte an einer Zuordnung mit dem Quell Objekt teilnehmen müssen, in dem das Quell Objekt eine bestimmte Rolle spielt. Die Rolle wird durch den Namen einer angegebenen Eigenschaft (die eine Verweis Eigenschaft sein muss) einer Zuordnung definiert.

</dd> <dt>

*bclassesonly* \[ optionale\]
</dt> <dd>

Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll. Dabei handelt es sich um die Klassen, zu denen die Endpunkt Instanzen gehören. Der Standardwert für diesen Parameter ist **false**.

</dd> <dt>

*bschemaonly* \[ optionale\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird. Der Standardwert für diesen Parameter ist **false**. Sie kann nur auf " **true** " festgelegt werden, wenn der *strobjectpath* -Parameter den Objekt Pfad einer Klasse angibt. Wenn der Wert auf **true** festgelegt ist, stellen die zurückgegebenen Endpunkte Klassen dar, die entsprechend der Quell Klasse im Schema zugeordnet sind.

</dd> <dt>

"otrequirements *dassocqualifizierer* \[ " optionale\]
</dt> <dd>

Eine Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte über eine Association-Klasse, die den angegebenen Qualifizierer enthält, dem Quell Objekt zugeordnet werden müssen.

</dd> <dt>

" *stringdqualifier* \[ " optionale\]
</dt> <dd>

Eine Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Endpunkte den angegebenen Qualifizierer einschließen müssen.

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Eine ganze Zahl, die die zusätzlichen Flags für den Vorgang angibt. Der Standardwert für diesen Parameter ist **wbemflagdontsendstatus**. Dieser Parameter kann die folgenden Werte annehmen.

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

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer * * * * (131072 (0x20000))


</dt> <dd>

Bewirkt, dass WMI zusammen mit der Basisklassen Definition Klassen Änderungs Daten zurückgibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> <dt>

*objwbemasynccontext* \[ optionale\]
</dt> <dd>

Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen. Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert. Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz. Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **associatorsofasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen einer oder mehrerer Klassen, die durch den-Befehl zurückgegeben werden.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das angeforderte Element wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieser Rückruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist. Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine. Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, finden Sie weitere Informationen unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

Verwenden Sie den *objwbemasynccontext* -Parameter in Skripts, um die Quelle eines Aufrufes zu überprüfen.

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

[**"Errbemujeject. ASSOCIATORS"\_**](swbemobject-associators-.md)
</dt> <dt>

[**"Errbemubject. associatorsasync"\_**](swbemobject-associatorsasync-.md)
</dt> <dt>

[**"Errbemubject. References"\_**](swbemobject-references-.md)
</dt> <dt>

[**Austauschen von "errbemubject. referencesasync"\_**](swbemobject-referencesasync-.md)
</dt> <dt>

[**"Swap Services. referencesto"**](swbemservices-referencesto.md)
</dt> <dt>

[**"Swap Services. referencestoasync"**](swbemservices-referencestoasync.md)
</dt> </dl>

 

