---
description: Das OnComplete-Ereignis eines slibemsink-Objekts wird ausgelöst, wenn ein asynchroner-Befehl abgeschlossen ist. Dieses Ereignis gibt für die Client Anwendung das Ergebnis eines asynchronen Vorgangs an und stellt Fehlerinformationen bereit, wenn der asynchrone-Befehl fehlschlägt.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'Iswbemsinkevents:: onabgeschlossene-Ereignis (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130965"
---
# <a name="iswbemsinkeventsoncompleted-event"></a>Iswbemsinkevents:: onabgeschlossene-Ereignis

Das **OnComplete** -Ereignis eines [**slibemsink**](swbemsink.md) -Objekts wird ausgelöst, wenn ein asynchroner-Befehl abgeschlossen ist. Dieses Ereignis gibt für die Client Anwendung das Ergebnis eines asynchronen Vorgangs an und stellt Fehlerinformationen bereit, wenn der asynchrone-Befehl fehlschlägt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ihresult* 
</dt> <dd>

Das HRESULT der abgeschlossenen asynchronen Methode. Das HRESULT ist mit dem Wert identisch, der von einem entsprechenden com- [API für WMI](com-api-for-wmi.md) -Methodenaufrufe zurückgegeben wird. Überprüfen Sie diesen Wert, um zu bestimmen, ob der asynchrone-Befehl erfolgreich ausgeführt wurde. Wenn der asynchrone-Aufrufvorgang erfolgreich ist, enthält dieser Parameter WBEM \_ S \_ No \_ Error (0). Wenn der asynchrone-Rückruf fehlschlägt, enthält dieser Parameter einen Fehlercode.

</dd> <dt>

*objWbemErrorObject* 
</dt> <dd>

Enthält ein " [**taubemlasterror**](swbemlasterror.md) "-Objekt, wenn die asynchrone Methode fehlschlägt.

</dd> <dt>

*objwbemasynccontext* 
</dt> <dd>

Dabei handelt es sich um ein-Objekt, das an den ursprünglichen asynchronen- [**Befehl**](swbemnamedvalueset.md) übergeben wird. Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mithilfe dieser Objekt Senke durchgeführt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss des **oncompletion** -Ereignisses kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.

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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-senbemsink<br/>                                                             |
| IID<br/>                      | IID \_ iswbemsinkevents<br/>                                                        |



 

