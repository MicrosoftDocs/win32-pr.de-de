---
description: Die TAPI-Zeilen \_ Antwortnachricht wird gesendet, um die Ergebnisse von Funktionsaufrufen zu melden, die asynchron abgeschlossen wurden.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: LINE_REPLY Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371769"
---
# <a name="line_reply-message"></a>Zeilen \_ Antwortnachricht

Die TAPI- **Zeilen \_ Antwort** Nachricht wird gesendet, um die Ergebnisse von Funktionsaufrufen zu melden, die asynchron abgeschlossen wurden.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
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

Funktionen, die asynchron agieren, geben einen positiven Anforderungs-ID-Wert an die Anwendung zurück. Dieser Anforderungs Bezeichner wird mit der Antwortnachricht zurückgegeben, um die abgeschlossene Anforderung zu identifizieren. Der andere Parameter für die **Zeilen \_ Antwort** Nachricht enthält die Erfolgs-oder Fehlermeldung. Mögliche Fehler sind identisch mit denen, die von der entsprechenden Funktion definiert werden. Diese Meldung kann nicht deaktiviert werden.

In einigen Fällen kann es vorkommen, dass eine Anwendung die **Zeilen \_ Antwort** Nachricht nicht empfängt, die einem Rückruf einer asynchronen Funktion entspricht. Dies tritt auf, wenn die Zuordnung des entsprechenden Telefon Handles aufgehoben wird, bevor die Nachricht empfangen wurde.

> [!Note]  
> Wenn eine Anwendung einen asynchronen Vorgang aufruft, mit dem Daten in den Anwendungs Speicher geschrieben werden, muss die Anwendung diesen Arbeitsspeicher für das Schreiben verfügbar halten, bis eine **Zeilen \_ Antwort** oder eine [**Zeile \_ gatherdigits**](line-gatherdigits.md) -Nachricht empfangen wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeilen \_ gatherziffern**](line-gatherdigits.md)
</dt> </dl>

 

 




