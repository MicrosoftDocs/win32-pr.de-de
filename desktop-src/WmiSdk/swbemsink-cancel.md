---
description: Die Cancel-Methode des SWbemSink-Objekts bricht alle ausstehenden asynchronen Vorgänge ab, die dieser Objektsenke zugeordnet sind.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: ISWbemSink::Cancel-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe2d8e8c0c5663adee0d6545e32f63cb5e8334269be99192122a2a66ac83159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107858"
---
# <a name="iswbemsinkcancel-method"></a>ISWbemSink::Cancel-Methode

Die **Cancel-Methode** des [**SWbemSink-Objekts bricht**](swbemsink.md) alle ausstehenden asynchronen Vorgänge ab, die dieser Objektsenke zugeordnet sind.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Cancel-Methode** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

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

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können nicht nur einen asynchronen Aufruf abbrechen. Wenn mehrere asynchrone Aufrufe ausstehen, die diese Objektsenke verwenden, bricht diese Methode alle asynchronen Aufrufe mithilfe dieser Objektsenke ab. Asynchrone Aufrufe, die anderen Objektsenken zugeordnet sind, bleiben unverändert.

Sie können diese Senke nothing **nicht zuweisen,** um einen asynchronen Vorgang abzubricht. Sie müssen die **Cancel-Methode aufrufen,** damit WMI den Vorgang beendet und die zugeordneten Ressourcen frei gibt. Dies ist bei längeren asynchronen Vorgängen wie Abfragen oder Vorgängen, die nie abgeschlossen werden, sehr wichtig, z. B. [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).

> [!Note]  
> Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke zur Verfügung zu stellen. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken zu beseitigen, verwenden Sie die semisynchrone oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

Das folgende Beispiel zeigt, wie Sie einen asynchronen Aufruf abbrechen.


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSink<br/>                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

