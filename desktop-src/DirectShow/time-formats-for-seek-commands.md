---
description: Zeitformate für Seek-Befehle
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Zeitformate für Seek-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e585a7dda12b40e7f501e51aff6ffed50d647066f03804c82e5ffa236f8623a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078720"
---
# <a name="time-formats-for-seek-commands"></a>Zeitformate für Seek-Befehle

Viele der Methoden in der **IMediaSeeking-Schnittstelle** verfügen über Parameter, die Positionswerte ausdrücken, z. B. aktuelle Position oder Stoppposition. Standardmäßig werden diese Parameter in Einheiten von 100 Nanosekunden ausgedrückt, die auch als Verweiszeit bezeichnet werden. Jeder Filter, der suchen kann, muss suchunterstützung nach Referenzzeit haben. Einige Filter können auch andere Zeiteinheiten verwenden, z. B. das Suchen nach einer bestimmten Framenummer oder das Suchen nach einem angegebenen Byteoffset innerhalb eines Streams. Jede dieser Zeiteinheiten wird als Zeitformat bezeichnet und durch eine GUID (Globally Unique Identifier) definiert. Eine Liste der von DirectShow definierten Zeitformate finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md) Drittanbieter können auch GUIDs für benutzerdefinierte Zeitformate definieren.

Um zu bestimmen, ob die filter derzeit im Filterdiagramm ein bestimmtes Zeitformat unterstützen, rufen Sie die [**IMediaSeeking::IsFormatSupported-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) auf. Die Methode gibt S \_ OK zurück, wenn das Format unterstützt wird. Andernfalls wird S \_ FALSE oder ein Fehlercode zurückgegeben. Wenn ein Format unterstützt wird, können Sie zu diesem Format wechseln, indem Sie die [**IMediaSeeking::SetTimeFormat-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) aufrufen. Wenn die **SetTimeFormat-Methode** erfolgreich ist, werden nachfolgende Suchbefehle im neuen Zeitformat ausgedrückt.

Im folgenden Beispiel wird überprüft, ob das Diagramm Such- nach Framenummer unterstützt. Wenn ja, wird versucht, die Nummer 20 zu umrahmen:


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



Beachten Sie, dass Zeitformate nur für Suchbefehle gelten. Sie wirken sich nicht auf die Wiedergabe von Diagrammen oder andere Aktionen aus.

 

 



