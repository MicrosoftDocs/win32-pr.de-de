---
description: Wenn ein Ereignis verfügbar ist, ruft die NextEvent-Methode des Objekts "slibemeventsource" das Ereignis aus einer Ereignis Abfrage ab.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Errbemeventsource. NextEvent-Methode (wbemdisp. h)
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
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357046"
---
# <a name="swbemeventsourcenextevent-method"></a>Errbemeventsource. NextEvent-Methode

Wenn ein Ereignis verfügbar ist, ruft die **NextEvent** -Methode des Objekts " [**slibemeventsource**](swbemeventsource.md) " das Ereignis aus einer Ereignis Abfrage ab.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*itimeoutms* \[ in, optional\]
</dt> <dd>

Anzahl der Millisekunden, die der Aufruf auf ein Ereignis wartet, bevor ein Timeout Fehler zurückgegeben wird. Der Standardwert für diesen Parameter ist **wbemtimeoutinfinite** (-1), der den-Vorgang anweist, unbegrenzt zu warten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die **NextEvent** -Methode erfolgreich ist, gibt Sie ein " [**errbemujebject**](swbemobject.md) "-Objekt zurück, das das angeforderte Ereignis enthält. Wenn für den-Rückruf ein Timeout auftritt, ist das zurückgegebene-Objekt **null** , und es wird ein Fehler ausgelöst.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **NextEvent** -Methode kann das **Err** -Objekt den Fehlercode in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrTimedOut** -0x80043001
</dt> <dd>

Das angeforderte Ereignis wurde nicht in der in *itimeoutms* angegebenen Zeit erreicht.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID-austauschen von " \_ errbemeventsource"<br/>                                                      |
| IID<br/>                      | IID \_ iswbemeventsource<br/>                                                       |



 

 




