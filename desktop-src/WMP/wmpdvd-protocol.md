---
title: WMPDVD-Protokoll
description: WMPDVD-Protokoll
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player,Protokolle
- Windows Media Player Objektmodell, Protokolle
- Objektmodell, Protokolle
- Windows Media Player ActiveX-Steuerelement, Protokolle für das Objektmodell
- ActiveX-Steuerelement, Protokolle für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Protokolle für objektmodell
- Windows Media Player Mobil, Protokolle für Objektmodell
- protocols,Windows Media Player-Objektmodell
- protocols,WMPDVD
- WMPDVD-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca67f3cdee6f040aeb266e02493425ca76715ade2e3269f4377ba340af89cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761290"
---
# <a name="wmpdvd-protocol"></a>WMPDVD-Protokoll

Mit dem WMPDVD-Protokoll können Sie Medien von einer DVD mit url-Syntax angeben. Dies ist die allgemeine Form des Protokolls:


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



Das *Laufwerksegment* ist der Buchstabe des DVD-Laufwerks. sie enthält nicht den Doppelpunkt, der normalerweise mit Laufwerksspezifizierern verwendet wird. Dieses Segment ist immer erforderlich.

Das *Titelsegment* ist die Nummer des titels, der wiedergegeben werden soll. Dies ist nur erforderlich, wenn Sie mit der Wiedergabe an einem bestimmten Titel oder an einem bestimmten Kapitel eines bestimmten Titels beginnen möchten.

Das *Kapitelsegment* ist die Nummer des zu spielende Kapitels. Dies ist nur erforderlich, wenn Sie mit der Wiedergabe in einem bestimmten Kapitel eines bestimmten Titels beginnen möchten.

Das contentdir-Argument ist der Pfad zu einem VIDEO \_ TS. IFO-Datei, die sich möglicherweise im lokalen Speicher oder auf einer Netzwerkfreigabe befindet. Wenn Sie dieses Segment einschließen, wird das *Laufwerksegment* ignoriert, obwohl es weiterhin erforderlich ist. Wenn Sie auch das *Titelsegment* oder die *Titel-* und *Kapitelsegmente* einschließen, sind sie relativ zum DVD-Inhalt, der im contentdir-Segment angegeben ist, und nicht zum *Laufwerksegment.*

Im folgenden Beispiel wird das WMPDVD-Protokoll verwendet, um die DVD von Anfang an wiederzuspielen, als würde sie automatisch gestartet.


```C++
player.url = "wmpdvd://F";
```



Im folgenden Beispiel wird das WMPDVD-Protokoll verwendet, um die DVD vom Anfang des angegebenen Titels wiederzuspielen.


```C++
player.url = "wmpdvd://F/2";
```



Im folgenden Beispiel wird das WMPDVD-Protokoll verwendet, um die DVD aus dem angegebenen Kapitel wiederzuspielen.


```C++
player.url = "wmpdvd://F/2/4";
```



Im folgenden Beispiel wird das WMPDVD-Protokoll verwendet, um DVD-Inhalte aus dem lokalen Speicher wiederzuspielen. Die *Pfadzeichenfolge* endet mit dem Ordner, der video \_ TS enthält. IFO-Datei; der Dateiname ist nicht enthalten. In diesem Beispiel hat der Wert des *Laufwerksegments* keine Auswirkungen, obwohl er erforderlich ist, und die Wiedergabe beginnt in Kapitel 4 von Titel 2.


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



Das Zuweisen einer WMPDVD-Zeichenfolge zur **URL-Eigenschaft** erfordert Windows Media Player 9er Serie oder höher.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Unterstützte Protokolle und Dateitypen**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




