---
description: Die DeleteAsync-Methode von SWbemObject löscht entweder die aktuelle Klasse oder \_ die aktuelle Instanz asynchron.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: SWbemObject.DeleteAsync_ -Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 66b5b2492b73d880f356a3d581efb6ff75d9e3d811c25283ef481bc2e592ae93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732540"
---
# <a name="swbemobjectdeleteasync_-method"></a>SWbemObject.DeleteAsync-Methode \_

Die **DeleteAsync-Methode \_** von [**SWbemObject**](swbemobject.md) löscht entweder die aktuelle Klasse oder die aktuelle Instanz asynchron. Wenn ein dynamischer Anbieter die Klasse oder Instanz liefert, ist es manchmal nicht möglich, dieses Objekt zu löschen, es sei denn, der Anbieter unterstützt das Löschen von Klassen oder Instanzen.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objWbemSink* \[ In\]
</dt> <dd>

Objektsenke, die das Ergebnis des Löschvorgang zurückgibt.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Eine ganze Zahl, die das Verhalten des Aufrufs bestimmt. Dieser Parameter kann die folgenden Werte akzeptieren.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus** (128 (0x80))


</dt> <dd>

Bewirkt, dass asynchrone Aufrufe Statusupdates an den [**SWbemSink.OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus** ( 0 (0x0))


</dt> <dd>

Verhindert, dass asynchrone Aufrufe Statusupdates an den [**OnProgress-Ereignishandler**](swbemsink-onprogress.md) für die Objektsenke senden.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, optional\]
</dt> <dd>

Dieser Parameter ist in der Regel nicht definiert. Andernfalls ist dies ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) dessen Elemente die Kontextinformationen darstellen, die vom Anbieter verwendet werden können, der die Anforderung bedient. Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, die zulässigen Werte und die Semantik dokumentieren.

</dd> <dt>

*objWbemAsyncContext* \[ in, optional\]
</dt> <dd>

Dies ist ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das zur Objektsenke zurückkehrt, um die Quelle des ursprünglichen asynchronen Aufrufs zu identifizieren. Verwenden Sie diesen Parameter, wenn Sie mehrere asynchrone Aufrufe mit derselben Objektsenke ausführen. Um diesen Parameter zu verwenden, erstellen Sie ein **SWbemNamedValueSet-Objekt,** und verwenden Sie die [**SWbemNamedValueSet.Add-Methode,**](swbemnamedvalueset-add.md) um einen Wert hinzuzufügen, der den von Ihnen ausgeführten asynchronen Aufruf identifiziert. Dieses **SWbemNamedValueSet-Objekt** wird an die Objektsenke zurückgegeben, und die Quelle des Aufrufs kann mithilfe der [**SWbemNamedValueSet.Item-Methode extrahiert**](swbemnamedvalueset-item.md) werden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück. Wenn dieser Aufruf erfolgreich ist, wird das Ergebnis des Löschvorgang über die angegebene Objektsenke bereitgestellt.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **DeleteAsync-Methode \_** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

Der aktuelle Kontext verfügt nicht über ausreichende Sicherheitsrechte zum Löschen des Objekts.

</dd> <dt>

**wbemErrFailed** – 2147749890 (0x80041002)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidClass** – 2147749904 (0x80041010)
</dt> <dd>

Die angegebene Klasse ist nicht vorhanden.

</dd> <dt>

**wbemErrInvalidOperation** – 2147749910 (0x80041016)
</dt> <dd>

Das Objekt kann nicht gelöscht werden.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das Objekt war nicht vorhanden.

</dd> <dt>

**wbemErrOutOfMemory** : 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Abschließen des Vorgangs.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieser Aufruf wird sofort zurückgegeben. Der Status wird an den Aufrufer durch einen Rückruf zurückgegeben, der an die Senke übermittelt wird, die in *objWbemSink angegeben ist.*

Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken zu beseitigen, verwenden Sie entweder die semisynchrone Kommunikation oder die synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

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



 

