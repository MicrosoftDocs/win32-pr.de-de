---
description: Das OnProgress-Ereignis von "slibemsink" wird ausgelöst, wenn ein asynchroner-Befehl den Status eines aktuell ausgeführten-Aufrufes zurückgibt.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Iswbemsinkevents:: OnProgress-Ereignis (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351117"
---
# <a name="iswbemsinkeventsonprogress-event"></a>Iswbemsinkevents:: OnProgress-Ereignis

Das **OnProgress** -Ereignis von " [**slibemsink**](swbemsink.md) " wird ausgelöst, wenn ein asynchroner-Befehl den Status eines aktuell ausgeführten-Aufrufes zurückgibt. Wenn die Ereignisse, Instanzen oder Klassen von einem Anbieter erzeugt werden, der Statusaktualisierungen unterstützt, können Sie Code in diesem Ereignis platzieren, um Benutzern Feedback zum Status eines asynchronen Vorgangs zu geben. Wenn Sie Statusaktualisierungen empfangen möchten, müssen Sie den *IFlags* -Parameter des asynchronen Aufrufes **wbemflagsendstatus** (128/0x80) festlegen. andernfalls wird dieses Ereignis nicht ausgelöst.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iupperbound* 
</dt> <dd>

Ganze Zahl, die die Gesamtzahl der zu erledigenden Aufgaben beschreibt.

</dd> <dt>

*icurrent* 
</dt> <dd>

Aktuelles Element, das gerade verarbeitet wird.

</dd> <dt>

*strMessage* 
</dt> <dd>

Meldung, in der der Status der aktuellen Aufgabe beschrieben wird.

</dd> <dt>

*objwbemasynccontext* 
</dt> <dd>

Ein " [**taubemnamedvalueset**](swbemnamedvalueset.md) "-Objekt, das an den ursprünglichen asynchronen-Befehl übergeben wird. Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mithilfe dieser Objekt Senke durchgeführt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss des **OnProgress** -Ereignisses kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der folgenden Fehlercodes enthalten.

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

Das **OnProgress** -Ereignis wird ausgelöst, wenn ein asynchroner-Rückruf den Status eines aktuell ausgeführten Aufrufs zurückgibt. Wenn die Ereignisse, Instanzen oder Klassen von einem Anbieter erzeugt werden, der Statusaktualisierungen unterstützt, können Sie Code in diesem Ereignis platzieren, um Benutzern Feedback zum Status eines asynchronen Vorgangs zu geben.

> [!Note]  
> Ein asynchroner Rückruf ermöglicht einem nicht authentifizierten Benutzer das Bereitstellen von Daten für die Senke. Dies birgt Sicherheitsrisiken für Ihre Skripts und Anwendungen. Um die Risiken auszuschließen, verwenden Sie die semisynchrone oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-Senke**](swbemsink.md)
</dt> </dl>

 

