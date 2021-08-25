---
description: Die TAPI LINE APPNEWCALL-Nachricht wird gesendet, um eine Anwendung zu informieren, wenn in ihrem Namen ein neues Aufrufhand \_ handle erstellt wurde.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: LINE_APPNEWCALL (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22efd93febad5e0199f2ff8897841fe57e8e637acfb8f9cd316386ed913876c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867130"
---
# <a name="line_appnewcall-message"></a>LINE \_ APPNEWCALL-Nachricht

Die TAPI **LINE \_ APPNEWCALL-Nachricht** wird gesendet, um eine Anwendung zu informieren, wenn in ihrem Namen ein neues Aufrufhand handle erstellt wurde (abgesehen von einem API-Aufruf der Anwendung. In diesem Fall wäre das Handle über einen Zeigerparameter zurückgegeben worden, der an die Funktion übergeben wurde).


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Das Handle der Anwendung für das Zeilengerät, auf dem der Aufruf erstellt wurde.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile des Aufrufs angegeben wurde.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Bezeichner der Adresse in der Zeile, in der der Aufruf angezeigt wird. Ein Adressbezeichner ist dauerhaft einer Adresse zugeordnet. der Bezeichner bleibt über Betriebssystemupgrades hinweg konstant.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Das Handle der Anwendung für den neuen Aufruf.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die Anwendungsberechtigung für den neuen Aufruf (LINECALLPRIVILEGE \_ OWNER oder LINECALLPRIVILEGE \_ MONITOR).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Anwendungen, die TAPI Version 2.0 oder höher unterstützen, erhalten immer dann eine **LINE \_ APPNEWCALL-Nachricht,** wenn der Anwendung ein Handle für einen neuen Aufruf erteilt wird. Da die Nachricht die *Parameter hLine* und *dwAddressID* enthält, für die der Aufruf vorhanden ist, kann die Anwendung problemlos ein neues Aufrufobjekt im richtigen Kontext erstellen. Auf **die LINE \_ APPNEWCALL-Nachricht** folgt immer sofort eine [**LINE \_ CALLSTATE-Meldung,**](line-callstate.md) die den Anfangszustand des Aufrufs angibt.

Ältere Anwendungen (die eine API-Version vor 2.0 ausgehandelt haben) werden nur eine [**LINE \_ CALLSTATE-Nachricht**](line-callstate.md) gesendet, wie in früheren Versionen der API dokumentiert. Solche Anwendungen würden ein neues Aufrufobjekt erstellen, wenn eine [**LINE \_ CALLSTATE-Nachricht**](line-callstate.md) empfangen wird, bei der *dwParam3* auf einen Wert ungleich 0 (null) festgelegt ist und ein Aufrufhand handle enthält, das der Anwendung derzeit nicht bekannt ist. Der Nachteil ist, dass (a) die Anwendung [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) aufrufen muss, um die *hLine-* und *dwAddressID-Parameter* zu bestimmen, die dem Aufruf zugeordnet sind. (b) Die Anwendung muss alle bekannten Aufrufhandles überprüfen, um zu ermitteln, dass der Aufruf ein neuer Aufruf ist. und (c) Es ist möglich, dass die Anwendung unter bestimmten Bedingungen davon aus geht, dass sie ein neues Aufrufhand handle empfängt, wenn sie in Wirklichkeit gerade ihr Handle für den Aufruf entfernt hat (z. B. hat die Anwendung gerade die Position eines Anrufhandpunkts entfernt, aber eine [**LINE \_ CALLSTATE-Nachricht,**](line-callstate.md) die der Anwendung den Besitz des Aufrufs aufgrund eines [**LineHandoffs**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) von einer anderen Anwendung gab, war bereits in der TAPI-Nachrichtenwarteschlange der Anwendung vorhanden).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




