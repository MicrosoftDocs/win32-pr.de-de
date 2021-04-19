---
description: Die TAPI-Zeile \_ appnewcallnachricht wird gesendet, um eine Anwendung zu benachrichtigen, wenn ein neues-Rückruf Handle in seinem Auftrag spontan erstellt wurde.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: LINE_APPNEWCALL Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368672"
---
# <a name="line_appnewcall-message"></a>Zeile \_ appnewcallmeldung

Die TAPI- **Zeile \_ appnewcallnachricht** wird gesendet, um eine Anwendung zu benachrichtigen, wenn ein neues Rückruf Handle in seinem Namen (mit Ausnahme eines API-Aufrufes von der Anwendung) spontan erstellt wurde. in diesem Fall würde das Handle durch einen Zeiger Parameter zurückgegeben werden, der an die Funktion übergeben wurde.


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Das Handle der Anwendung für das liniengerät, für das der-Rückruf erstellt wurde.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Bezeichner der Adresse in der Zeile, für die der-Befehl angezeigt wird. Ein Adress Bezeichner ist dauerhaft einer Adresse zugeordnet. der Bezeichner bleibt bei Betriebssystem Upgrades konstant.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Das Handle der Anwendung für den neuen-Befehl.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die Anwendungs Berechtigung für den neuen-Befehl (linecallprivilege- \_ Besitzer oder linecallprivilege- \_ Monitor).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Anwendungen, die TAPI-Version 2,0 oder höher unterstützen, werden immer dann an eine **Zeile \_ appnewcallnachricht** gesendet, wenn der Anwendung ein Handle für einen neuen Aufruf übergeben wird. Da die Nachricht die Parameter " *hline* " und " *dwadressssid* " enthält, für die der-Befehl vorhanden ist, kann die Anwendung ein neues-Objekt im richtigen Kontext erstellen. Der **\_ appnewcallmessage-Zeile** folgt immer sofort eine [**Zeile \_ CallState**](line-callstate.md) -Meldung, die den ursprünglichen Status des Aufrufes angibt.

Ältere Anwendungen (die eine API-Version vor 2,0 ausgehandelt haben) werden nur als [**Zeilen- \_ CallState**](line-callstate.md) -Nachricht gesendet, wie in früheren Versionen der API dokumentiert. Solche Anwendungen würden beim Empfangen einer [**Zeile \_ CallState**](line-callstate.md) -Nachricht ein neues Aufruf Objekt erstellen, bei dem *dwParam3* auf einen Wert ungleich 0 (null) festgelegt ist und ein Aufruf Handle enthält, das von der Anwendung derzeit nicht bekannt ist. Der Nachteil ist, dass die Anwendung [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) aufrufen muss, um die dem Aufruf zugeordneten *hline* -und *dwadressssid* -Parameter zu bestimmen. (b) die Anwendung muss alle bekannten aufrufhandles Scannen, um zu bestimmen, ob der-Befehl ein neuer-Befehl ist. und (c) Es ist möglich, unter bestimmten Bedingungen kann die Anwendung annehmen, dass Sie ein neues Aufruf handle empfängt, wenn Sie in der Praxis gerade das zugehörige Handle für den Aufruf freigegeben hat (z. b. hat die Anwendung soeben die Zuordnung eines Aufruf Handles aufgehoben, aber eine [**Zeile \_ CallState**](line-callstate.md) -Nachricht, die den [](/windows/desktop/api/Tapi/nf-tapi-linehandoff) Anwendungs Besitz des Aufrufes in der TAPI-Nachrichten Warteschlange der Anwendung bereitstellt).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_liniencallstate**](line-callstate.md)
</dt> <dt>

[**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**linehandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




