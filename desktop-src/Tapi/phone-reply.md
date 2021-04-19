---
description: Die TAPI-Telefon \_ Antwortnachricht wird an eine Anwendung gesendet, um die Ergebnisse des Funktionsaufrufs zu melden, die asynchron abgeschlossen wurden.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: PHONE_REPLY Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367516"
---
# <a name="phone_reply-message"></a>Telefon \_ Antwortnachricht

Die TAPI- **Telefon \_ Antwort** Nachricht wird an eine Anwendung gesendet, um die Ergebnisse des Funktionsaufrufs zu melden, die asynchron abgeschlossen wurden.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hphone* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Gibt die Rückruf Instanz der Anwendung zurück.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Anforderungs Bezeichner, für den dies die Antwort ist.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Die Erfolgs-oder Fehlermeldung. Die Anwendung sollte diesen Parameter in einen Long-Typ umwandeln. NULL gibt den Erfolg an; eine negative Zahl gibt einen Fehler an.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Funktionen, die asynchron agieren, geben einen positiven Anforderungs-ID-Wert an die Anwendung zurück. Dieser Anforderungs Bezeichner wird mit der Antwortnachricht zurückgegeben, um die abgeschlossene Anforderung zu identifizieren. Der andere Parameter für die **Telefon \_ Antwort** Nachricht enthält die Erfolgs-oder Fehlermeldung. Mögliche Fehler sind identisch mit denen, die von der entsprechenden Funktion definiert werden. Diese Meldung kann nicht deaktiviert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




