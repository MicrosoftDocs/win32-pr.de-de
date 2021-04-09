---
description: Ruft ein Objekt ab, das eine Klassendefinition oder eine-Instanz ist, basierend auf dem Objekt Pfad.
ms.assetid: 8da46851-52b8-4b5a-8c9d-1d492f57f4b6
ms.tgt_platform: multiple
title: Swap Services. getasync-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.GetAsync
- ISWbemServices.GetAsync
- ISWbemServices.GetAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 451f13bde9458e7d57ec393f42b92a4092c99924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863760"
---
# <a name="swbemservicesgetasync-method"></a>Swap Services. getasync-Methode

Die **getasync** -Methode des [**Swap Services**](swbemservices.md) -Objekts Ruft ein Objekt ab, das eine Klassendefinition oder eine-Instanz ist, die auf dem Objekt Pfad basiert.

Diese Methode ruft nur Objekte aus dem Namespace ab, der dem aktuellen ' [**Swap Services**](swbemservices.md) '-Objekt zugeordnet ist.

Diese Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemServices.GetAsync( _
  ByVal objWbemSink, _
  [ ByVal strObjectPath ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objwbemsink* 
</dt> <dd>

Erforderlich. Objekt Senke, die Objekte asynchron abruft. Erstellen Sie ein " [**Swap**](swbemsink.md) "-Objekt, um die Objekte zu empfangen.

</dd> <dt>

*strobjectpath* \[ optionale\]
</dt> <dd>

Der Pfad des Objekts, das Sie abrufen möchten. Wenn dieser Wert leer ist, kann das leere Objekt, das zurückgegeben wird, eine neue Klasse werden. Weitere Informationen finden Sie unter [beschreiben des Speicher Orts eines WMI-Objekts](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten des Aufrufes bestimmt. Dieser Parameter kann die folgenden Werte annehmen.

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

Bewirkt, dass WMI Klassen Änderungs Daten mit der Basisklassen Definition zurückgibt. Weitere Informationen finden Sie unter [Lokalisieren von WMI-Klassen Informationen](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

In der Regel ist dieser Wert nicht definiert. Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.

</dd> <dt>

*objwbemasynccontext* \[ optionale\]
</dt> <dd>

Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das zur Objekt Senke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufes aufzurufen. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mithilfe derselben Objekt Senke durchführen. Um diesen Parameter zu verwenden, erstellen Sie ein Objekt vom Typ " **Swap namedvalueset** ", und verwenden Sie die Methode " [**taubemnamedvalueset. Add**](swbemnamedvalueset-add.md) ", um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Befehl identifiziert. Dieses Objekt vom Typ " **Swap namedvalueset** " wird an die Objekt Senke zurückgegeben, und die Quelle des Aufrufes kann mithilfe der Methode " [**Swap Name. Item**](swbemnamedvalueset-item.md) " extrahiert werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Bei erfolgreicher Ausführung empfängt die Senke ein [**onobjectready**](swbemsink-onobjectready.md) -Ereignis, wenn das Objekt verfügbar ist.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **getasync** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Benutzer verfügt nicht über die Berechtigung für den Zugriff auf das Objekt.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrInvalidObjectPath** -2147749946 (0x8004103a)
</dt> <dd>

Der angegebene Pfad war ungültig.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das angeforderte Objekt wurde nicht gefunden.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieser Rückruf wird sofort zurückgegeben. Das angeforderte Objekt und der Status werden mithilfe eines Rückrufs an den Aufrufer zurückgegeben, der an die in *objwbemsink* angegebene Senke gesendet wird. Um das Objekt zu verarbeiten, wenn es zurückgegeben wird, erstellen Sie eine *objwbemsink*. " [**Onobjectready**](swbemsink-onobjectready.md)" oder " *objwbemsink*". [**Onabgeschlossene**](swbemsink-oncompleted.md) Ereignis Unterroutine.

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

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

[**Austausch Objekt**](swbemobject.md)
</dt> </dl>

 

