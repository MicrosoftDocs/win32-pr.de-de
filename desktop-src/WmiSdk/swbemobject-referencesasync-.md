---
description: Die referencesasync-Methode von Swap-Objekten stellt eine Auflistung aller Zuordnungs \_ Klassen oder-Instanzen bereit, die auf das aktuelle-Objekt verweisen. Diese Methode führt die gleiche Funktion aus, die die WQL-Verweise der Abfrage ausführen.
ms.assetid: 44989726-3f68-453b-b9f5-e76fb0fbb152
ms.tgt_platform: multiple
title: SWbemObject.ReferencesAsync_-Methode (wbemdisp. h)
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
ms.openlocfilehash: aa4b85475a0dc9f736254c8f207469a52897b7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356617"
---
# <a name="swbemobjectreferencesasync_-method"></a>Errbemubject. referencesasync- \_ Methode

Die **referencesasync \_** -Methode von [**Swap**](swbemobject.md) -Objekten stellt eine Auflistung aller Zuordnungs Klassen oder-Instanzen bereit, die auf das aktuelle-Objekt verweisen. Diese Methode führt die gleiche Funktion aus, die die WQL- [Verweise der](references-of-statement.md) Abfrage ausführen.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

*objwbemsink* \[ in\]
</dt> <dd>

Erforderlich. Objekt Senke, die die-Objekte asynchron empfängt.

</dd> <dt>

" *strautclass* \[ " in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Klassennamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte der in diesem Parameter angegebenen Klasse angehören oder von dieser abgeleitet werden müssen.

</dd> <dt>

*Rolle "Rolle* \[ " in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Eigenschaftsnamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte auf diejenigen beschränkt werden müssen, in denen das Quell Objekt eine bestimmte Rolle spielt. Der Name einer angegebenen Verweis Eigenschaft definiert die Rolle einer Zuordnung.

</dd> <dt>

*bclassesonly* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob eine Liste von Klassennamen anstelle tatsächlicher Instanzen der Klassen zurückgegeben werden soll. Dabei handelt es sich um die Klassen, zu denen die Zuordnungs Objekte gehören. Der Standardwert für diesen Parameter ist **false**.

</dd> <dt>

*bschemaonly* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob die Abfrage auf das Schema und nicht auf die Daten angewendet wird. Der Standardwert für diesen Parameter ist **false**. Sie kann nur auf " **true** " festgelegt werden, wenn das Objekt, für das diese Methode aufgerufen wird, eine Klasse ist. Wenn der Wert auf **true** festgelegt ist, stellt der Satz der zurückgegebenen Endpunkte Klassen dar, die der Quell Klasse im Schema entsprechend zugeordnet sind.

</dd> <dt>

" *stringdqualifier* \[ " in, optional\]
</dt> <dd>

Eine Zeichenfolge, die einen Qualifizierernamen enthält. Wenn angegeben, gibt dieser Parameter an, dass die zurückgegebenen Zuordnungs Objekte den angegebenen Qualifizierer einschließen müssen.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemflagsendstatus * * * * (128 (0x80))


</dt> <dd>

Bewirkt, dass asynchrone Aufrufe Statusaktualisierungen an den " [**slibemsink. OnProgress**](swbemsink-onprogress.md) "-Ereignishandler für die Objekt Senke senden.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemflagdontsendstatus * * * * (0 (0x0))


</dt> <dd>

Verhindert, dass asynchrone Aufrufe Statusaktualisierungen an den [**OnProgress**](swbemsink-onprogress.md) -Ereignishandler für die Objekt Senke senden.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemflaguseamendedqualifizierer * * * * (131072 (0x20000))


</dt> <dd>

Bewirkt, dass Windows-Verwaltungsinstrumentation (WMI) Klassen Zusatzdaten mit der Basisklassen Definition zurückgibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ in, optional\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [typswap namedvalueset](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> <dt>

*objwbemasynccontext* \[ in, optional\]
</dt> <dd>

Dabei handelt es sich um ein Objekt vom Typ " [taubemnamedvalueset](swbemnamedvalueset.md) ", das zur Objekt Senke zurückkehrt, um die Quelle für den ursprünglichen asynchronen aufzurufen. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen. Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ "Swap namedvalueset", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen-Befehl identifiziert. Dieses Objekt vom Typ "Swap namedvalueset" wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz. Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **referencesasync \_** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieser Rückruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist. Um jedes Objekt zu verarbeiten, sobald es eintrifft, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine. Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* durchführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Weitere Informationen zu den verweisen der zugeordneten WQL-Abfrage, Quell Instanzen und Zuordnungs Objekte finden Sie unter [ASSOCIATORS of Statement](associators-of-statement.md).

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

[**"Errbemujeject. ASSOCIATORS"\_**](swbemobject-associators-.md)
</dt> <dt>

[**"Taubemservices. associatorsof"**](swbemservices-associatorsof.md)
</dt> <dt>

[**"Swap Services. referencesto"**](swbemservices-referencesto.md)
</dt> <dt>

[**"Swap Services. referencestoasync"**](swbemservices-referencestoasync.md)
</dt> </dl>

 

