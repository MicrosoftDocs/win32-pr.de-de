---
description: Das OnObjectPut-Ereignis eines SWbemSink-Objekts wird ausgelöst, wenn ein asynchroner Put-Vorgang abgeschlossen ist. Dieses Ereignis gibt den Objektpfad der Instanz oder der gespeicherten Klasse zurück.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: ISWbemSinkEvents::OnObjectPut-Ereignis (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 81f012d6156e6ec17c609bec5be2bc355a0bd9bf197b139a7da2a494285a1c87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030400"
---
# <a name="iswbemsinkeventsonobjectput-event"></a>ISWbemSinkEvents::OnObjectPut-Ereignis

Das **OnObjectPut-Ereignis** eines [**SWbemSink-Objekts**](swbemsink.md) wird ausgelöst, wenn ein asynchroner Put-Vorgang abgeschlossen ist. Dieses Ereignis gibt den Objektpfad der Instanz oder der gespeicherten Klasse zurück.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*objWbemObjectPath* 
</dt> <dd>

Ein [**SWbemObjectPath-Objekt,**](swbemobjectpath.md) das den Objektpfad der Instanz oder Klasse enthält, die der Put-Vorgang in WMI schreibt.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Ein [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das an den ursprünglichen asynchronen Aufruf übergeben wird. Verwenden Sie diesen Parameter, um den Ursprung des asynchronen Aufrufs zu identifizieren, der dieses Ereignis auslöst, wenn mehrere asynchrone Aufrufe mit dieser Objektsenke erfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss des **OnObjectPut-Ereignisses** kann das [Err-Objekt](/previous-versions//sbf5ze0e(v=vs.85)) einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrTransportFailure** – 2147749909 (0x80041015)
</dt> <dd>

Netzwerkfehler, der den normalen Betrieb verhindert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> Ein asynchroner Rückruf ermöglicht es einem nicht authentifizierten Benutzer, Daten für die Senke bereitzustellen. Dies stellt Sicherheitsrisiken für Ihre Skripts und Anwendungen dar. Um die Risiken zu vermeiden, verwenden Sie entweder semisynchrone Kommunikation oder synchrone Kommunikation. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSinkEvents<br/>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

