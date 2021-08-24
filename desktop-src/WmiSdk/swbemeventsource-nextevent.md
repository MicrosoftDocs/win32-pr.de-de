---
description: Wenn ein Ereignis verfügbar ist, ruft die NextEvent-Methode des SWbemEventSource-Objekts das Ereignis aus einer Ereignisabfrage ab.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: SWbemEventSource.NextEvent-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6ce39d442b48f32c2aafcd6e24c1c214dce82a19435b6b36bce65d5426161859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050068"
---
# <a name="swbemeventsourcenextevent-method"></a>SWbemEventSource.NextEvent-Methode

Wenn ein Ereignis verfügbar ist, ruft die **NextEvent-Methode** des [**SWbemEventSource-Objekts**](swbemeventsource.md) das Ereignis aus einer Ereignisabfrage ab.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iTimeoutMs* \[ in, optional\]
</dt> <dd>

Anzahl von Millisekunden, die der Aufruf auf ein Ereignis wartet, bevor ein Time out-Fehler zurückgegeben wird. Der Standardwert für diesen Parameter ist **wbemTimeoutInfinite** (-1), der den Aufruf anleitet, unbegrenzt zu warten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die **NextEvent-Methode** erfolgreich ist, wird ein [**SWbemObject-Objekt**](swbemobject.md) zurückgegeben, das das angeforderte Ereignis enthält. Wenn für den Aufruf ein Zeitfehler auftritt, ist das zurückgegebene Objekt **NULL,** und es wird ein Fehler ausgelöst.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **NextEvent-Methode** kann das **Err-Objekt** den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrTimedOut** – 0x80043001
</dt> <dd>

Das angeforderte Ereignis ist nicht in der in *iTimeoutMs* angegebenen Zeitspanne eingetroffen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



 

 




