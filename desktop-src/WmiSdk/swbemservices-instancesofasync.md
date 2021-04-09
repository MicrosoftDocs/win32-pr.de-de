---
description: Ruft Instanzen einer angegebenen Klasse entsprechend den vom Benutzer angegebenen Kriterien ab.
ms.assetid: 631cd749-9a39-4606-9a38-0b4bb5b4b2cd
ms.tgt_platform: multiple
title: Swap Services. instancesofasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
- ISWbemServices.InstancesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c518cb38a0ecb221f4fcb0d0e7f9ce6dfc226ba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863759"
---
# <a name="swbemservicesinstancesofasync-method"></a>Methode "Swap Services. instancesofasync"

Die **instancesofasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts Ruft die Instanzen einer angegebenen Klasse entsprechend den vom Benutzer angegebenen Kriterien ab.

Die-Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Die Syntax Erklärung finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemServices.InstancesOfAsync( _
  ByVal ObjWbemSink, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Objwbemsink* 
</dt> <dd>

Objekt Senke, die die Instanzen asynchron empfängt. Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.

</dd> <dt>

*Klasse* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Namen der Klasse für die gewünschten Instanzen enthält. Dieser Parameter darf nicht leer sein.

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Bestimmt die Tiefe der aufrufenumeration und gibt an, ob der Rückruf sofort zurückgegeben wird. Dieser Parameter kann die folgenden Werte annehmen.

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemqueryflagflache * * * * (1 (0x1))


</dt> <dd>

Erzwingt, dass die Enumeration nur unmittelbare Unterklassen der angegebenen übergeordneten Klasse einschließt.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemqueryflagdeep * * * * (0 (0x0))


</dt> <dd>

Der Standardwert für diesen Parameter. Dieser Wert erzwingt, dass die Enumeration alle Klassen in der Hierarchie einschließt.

</dd> <dt>

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

Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Dies ist in der Regel nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der Kontext Informations Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> <dt>

*objwbemasynccontext* \[ optionale\]
</dt> <dd>

Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen. Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert. Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis pro Instanz. Nach der letzten Instanz empfängt die Objekt Senke ein [**onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **instancesofasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Anzeigen von Instanzen der angegebenen Klasse.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Nicht angegebener Fehler.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse ist ungültig.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieser Rückruf wird sofort zurückgegeben. Die angeforderten Objekte und der Status werden an den Aufrufer zurückgegeben, wenn Rückrufe an die Senke gesendet werden, die in *objwbemsink* angegeben ist. Um jedes Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. [**Onobjectready**](swbemsink-onobjectready.md) -Ereignis Unterroutine. Nachdem alle Objekte zurückgegeben wurden, können Sie die endgültige Verarbeitung in ihrer Implementierung von *objwbemsink* ausführen. [**Onabgeschlossene**](swbemsink-oncompleted.md) -Ereignis.

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Informationen zur Vermeidung der Risiken finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md) -Befehl.

Die **instancesofasync** -Methode funktioniert nur für Klassen Objekte. Es ist kein Fehler, wenn der zurückgegebene Enumerator NULL (0) Elemente aufweist.

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

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

