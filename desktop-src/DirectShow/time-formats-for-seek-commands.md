---
description: Zeitformate für Such Befehle
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Zeitformate für Such Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530326"
---
# <a name="time-formats-for-seek-commands"></a>Zeitformate für Such Befehle

Viele der Methoden in der **imediaseeking** -Schnittstelle verfügen über Parameter, die Positionswerte Ausdrücken, wie z. b. die aktuelle Position oder die Position des Stopps. Standardmäßig werden diese Parameter in Einheiten von 100 Nanosekunden ausgedrückt, auch als Bezugszeit bezeichnet. Jeder Filter, der suchen kann, muss das Suchen nach Verweis Zeit unterstützen. Einige Filter können auch andere Zeiteinheiten suchen, wie z. b. das Suchen nach einer bestimmten Frame Nummer oder das Suchen eines bestimmten Byte Offsets innerhalb eines Streams. Jede dieser Zeiteinheiten wird als Zeitformat bezeichnet und durch einen Globally Unique Identifier (GUID) definiert. Eine Liste der von DirectShow definierten Zeitformaten finden Sie unter [**Zeit Format-GUIDs**](time-format-guids.md). Drittanbieter können auch GUIDs für benutzerdefinierte Zeitformate definieren.

Um zu ermitteln, ob die derzeit im Filter Diagramm verfüg enden Filter ein bestimmtes Zeitformat unterstützen, rufen Sie die [**imediaseeking:: isformatsupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) -Methode auf. Die Methode gibt "S OK" zurück, \_ Wenn das Format unterstützt wird. Andernfalls wird S false zurückgegeben, oder es wird \_ ein Fehlercode zurückgegeben. Wenn ein Format unterstützt wird, können Sie zu diesem Format wechseln, indem Sie die [**imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) -Methode aufrufen. Wenn die **settimeformat** -Methode erfolgreich ist, werden nachfolgende Seek-Befehle mit dem neuen Zeitformat ausgedrückt.

Im folgenden Beispiel wird überprüft, ob das Diagramm das Suchen nach Frame Nummer unterstützt. Wenn dies der Fall ist, wird eine Frame Nummer von 20 gesucht:


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



Beachten Sie, dass Zeitformate nur für Such Befehle gelten. Sie wirken sich nicht auf die Wiedergabe des Diagramms oder andere Aktionen aus.

 

 



