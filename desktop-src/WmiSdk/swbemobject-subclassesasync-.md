---
description: Die SubclassesAsync-Methode von SWbemObject stellt asynchron die Unterklassen des aktuellen Objekts zur Anwendung, das \_ eine Klasse sein muss.
ms.assetid: 14d4a609-3aa4-49bd-bea4-6a71bc24d9dd
ms.tgt_platform: multiple
title: SWbemObject.SubclassesAsync_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
- ISWbemObject.SubclassesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1b8c9879d203c3a099177e9748cd1410d60c228f5d47ab2e5305bbeaf858eb76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568380"
---
# <a name="swbemobjectsubclassesasync_-method"></a>SWbemObject.SubclassesAsync-Methode \_

Die **\_ SubclassesAsync-Methode** von [**SWbemObject**](swbemobject.md) stellt asynchron die Unterklassen des aktuellen Objekts zur Anwendung, das eine Klasse sein muss.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemObject.SubclassesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objWbemSink* \[ In\]
</dt> <dd>

Erforderlich. Objektsenke, die die Objekte asynchron empfängt.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Bestimmt, wie detailliert der Aufruf aufzählt. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep** (0 (0x0))


</dt> <dd>

Erzwingt eine rekursive Enumeration in alle Unterklassen, die von der angegebenen übergeordneten Klasse abgeleitet werden. Die übergeordnete Klasse selbst wird in der -Enumeration nicht zurückgegeben.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow** (1 (0x1))


</dt> <dd>

Der Standardwert für diesen Parameter. Er erzwingt, dass die -Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse enthält.

</dd> <dt>

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

Bewirkt, dass WMI Klassenänderungsdaten mit der Basisklassendefinition zurück gibt. Weitere Informationen zu geänderten Qualifizierern finden Sie unter [Lokalisieren von WMI-Klasseninformationen.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ in, optional\]
</dt> <dd>

In der Regel ist dies nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ in, optional\]
</dt> <dd>

Dies ist ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mit derselben Objektsenke ausführen. Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den asynchronen Aufruf identifiziert, den Sie ausführen. Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode extrahiert**](swbemnamedvalueset-item.md) werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei Erfolg empfängt die Senke für jede Instanz ein [**OnObjectReady-Ereignis.**](swbemsink-onobjectready.md) Nach der letzten Instanz empfängt die Objektsenke ein [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Methode SubclassesAsync \_** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung, eine oder mehrere der vom Aufruf zurückgegebenen Klassen anzeigen zu können.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidClass** – 2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse ist nicht vorhanden.

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

Es wird empfohlen, dass Skripts die Quelle des Aufrufs mithilfe eines *objWbemAsyncContext-Parameters* überprüfen.

Es ist kein Fehler für die zurückgegebene Auflistung, null Elemente zu haben, wenn keine Unterklassen des aktuellen -Objekts enthalten sind. Die **Methode SubclassesAsync \_** funktioniert nur für Klassenobjekte.

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

[**SWbemObjectSet**](swbemobjectset.md)
</dt> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> </dl>

 

