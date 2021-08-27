---
description: Die TAPI LINE REPLY-Nachricht wird gesendet, um die Ergebnisse von Funktionsaufrufen zu \_ melden, die asynchron abgeschlossen wurden.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: LINE_REPLY (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febe10c822a469465984b715c7b6f23d150f1f068730d4e92190b05ce50cd535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126240"
---
# <a name="line_reply-message"></a>LINE \_ REPLY-Nachricht

Die TAPI **LINE \_ REPLY-Nachricht** wird gesendet, um die Ergebnisse von Funktionsaufrufen zu melden, die asynchron abgeschlossen wurden.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Gibt die Rückrufinstanz der Anwendung zurück.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Anforderungsbezeichner, für den dies die Antwort ist.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Die Erfolgs- oder Fehleranzeige. Die Anwendung sollte diesen Parameter in einen LONG-Wert um casten. 0 (null) gibt den Erfolg an. Eine negative Zahl gibt einen Fehler an.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Funktionen, die asynchron arbeiten, geben einen positiven Anforderungsbezeichnerwert an die Anwendung zurück. Dieser Anforderungsbezeichner wird mit der Antwortnachricht zurückgegeben, um die abgeschlossene Anforderung zu identifizieren. Der andere Parameter für die **LINE \_ REPLY-Nachricht** enthält die Erfolgs- oder Fehleranzeige. Mögliche Fehler sind identisch mit denen, die von der entsprechenden Funktion definiert werden. Diese Meldung kann nicht deaktiviert werden.

In einigen Fällen kann es sein, dass eine Anwendung die **LINE \_ REPLY-Nachricht** nicht empfangen kann, die einem Aufruf einer asynchronen Funktion entspricht. Dies tritt auf, wenn das entsprechende Aufrufhand handle dieLociert, bevor die Nachricht empfangen wurde.

> [!Note]  
> Wenn eine Anwendung einen asynchronen Vorgang aufruft, der Daten zurück in den Anwendungsspeicher schreibt, muss die Anwendung diesen Arbeitsspeicher für das Schreiben verfügbar halten, bis eine **LINE \_ REPLY-** oder [**LINE \_ GATHERDIGITS-Nachricht**](line-gatherdigits.md) empfangen wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ GATHERDIGITS**](line-gatherdigits.md)
</dt> </dl>

 

 




