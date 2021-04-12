---
description: Die Cancel-Methode des Swap-Objekts bricht alle ausstehenden asynchronen Vorgänge ab, die dieser Objekt Senke zugeordnet sind.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'Iswbemsink:: Cancel-Methode (wbemdisp. h)'
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
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218481"
---
# <a name="iswbemsinkcancel-method"></a>Iswbemsink:: Cancel-Methode

Die **Cancel** -Methode des [**Swap**](swbemsink.md) -Objekts bricht alle ausstehenden asynchronen Vorgänge ab, die dieser Objekt Senke zugeordnet sind.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **Cancel** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015)
</dt> <dd>

Netzwerkfehler. der normale Betrieb wird verhindert.

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Der aktuelle oder der angegebene Benutzername und das Kennwort sind ungültig oder sind zum Herstellen der Verbindung autorisiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es ist nicht möglich, nur einen asynchronen-Befehl abzubrechen. Wenn mehrere asynchrone Aufrufe ausstehen, die diese Objekt Senke verwenden, bricht diese Methode alle asynchronen Aufrufe mithilfe dieser Objekt Senke ab. Asynchrone Aufrufe, die anderen Objekt senken zugeordnet sind, bleiben unverändert.

Diese Senke kann **nichts** zugewiesen werden, um einen asynchronen Vorgang abzubrechen. Sie müssen die **Cancel** -Methode aufzurufen, damit WMI den Vorgang abbricht und die zugeordneten Ressourcen freigibt. Dies ist sehr wichtig bei langwierigen asynchronen Vorgängen wie z. b. Abfragen oder Vorgängen, die nicht vollständig ausgeführt werden, wie z. b. [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).

> [!Note]  
> Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

Im folgenden Beispiel wird gezeigt, wie ein asynchroner-Befehl abgebrochen wird.


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-senbemsink<br/>                                                             |
| IID<br/>                      | IID \_ iswbemsink<br/>                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-Senke**](swbemsink.md)
</dt> </dl>

 

