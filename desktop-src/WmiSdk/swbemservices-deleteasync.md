---
description: Löscht die im Objektpfad angegebene Klasse oder Instanz.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: SWbemServices.DeleteAsync-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bcbdf4d930b2a67c56572a9788592b943748f6e41c30483728f3cc24732ffa18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897484"
---
# <a name="swbemservicesdeleteasync-method"></a>SWbemServices.DeleteAsync-Methode

Die **DeleteAsync-Methode** des [**SWbemServices-Objekts**](swbemservices.md) löscht die im Objektpfad angegebene Klasse oder Instanz. Der Aufruf von **DeleteAsync** wird sofort zurückgegeben, und die Ergebnisse und der Status werden an den Aufrufer über Ereignisse zurückgegeben, die an die in *objWbemSink* angegebene Senke übermittelt werden. Weitere Informationen zum Erstellen einer Senke finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md) Sie können nur Objekte in dem Namespace löschen, mit dem Sie verbunden sind.

Wenn ein dynamischer Anbieter die Klasse oder Instanz liefert, ist es manchmal nicht möglich, dieses Objekt zu löschen, es sei denn, der Anbieter unterstützt das Löschen von Klassen oder Instanzen.

Die -Methode wird im asynchronen Modus aufgerufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ObjWbemSink* \[ Optional\]
</dt> <dd>

Objektsenke, die die Ergebnisse des Löschvorgang empfängt. Erstellen Sie ein [**SWbemSink-Objekt,**](swbemsink.md) um die Objekte zu empfangen.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Erforderlich. Eine Zeichenfolge, die den Objektpfad zu dem Objekt enthält, das Sie löschen möchten. Weitere Informationen finden Sie unter [Beschreiben des Speicherorts eines WMI-Objekts.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*iFlags* \[ Optional\]
</dt> <dd>

Bestimmt, ob Statusupdates zurückgegeben werden. Dieser Parameter kann die folgenden Werte akzeptieren.

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

Diese Methode gibt keinen Wert zurück. Wenn der Aufruf erfolgreich ist, empfängt die Objektsenke eine Benachrichtigung über den Löschvorgang.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **DeleteAsync-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

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

**wbemErrTransportFailure** – 2147749909 (0x80041015)
</dt> <dd>

Netzwerkfehler, der den normalen Betrieb verhindert.

</dd> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle oder angegebene Benutzername und das Kennwort sind nicht gültig oder autorisiert, um die Verbindung herzustellen.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das angeforderte Element wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieser Aufruf wird sofort zurückgegeben. Der Status des Löschvorgang wird an den Aufrufer über einen Rückruf zurückgegeben, der an die in *objWbemSink* angegebene Senke übermittelt wird. Sie können die endgültige Verarbeitung in Ihrer Implementierung von *objWbemSink ausführen.* [**OnCompleted-Ereignis.**](swbemsink-oncompleted.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Swbemservices**](swbemservices.md)
</dt> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> </dl>

 

