---
title: Wmpdvd-Protokoll
description: Wmpdvd-Protokoll
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows-Media Player, Protokolle
- Windows Media Player-Objektmodell, Protokolle
- Objektmodell, Protokolle
- Windows Media Player ActiveX-Steuerelement, Protokolle für das Objektmodell
- ActiveX-Steuerelement, Protokolle für Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Protokolle für das Objektmodell
- Windows Media Player Mobile, Protokolle für das Objektmodell
- Protokolle, Windows Media Player-Objektmodell
- Protokolle, wmpdvd
- Wmpdvd-Protokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309872"
---
# <a name="wmpdvd-protocol"></a>Wmpdvd-Protokoll

Mit dem wmpdvd-Protokoll können Sie mithilfe der URL-Syntax Medien von einer DVD angeben. Dies ist die allgemeine Form des Protokolls:


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



Das *Laufwerk* Segment ist der Buchstabe des DVD-Laufwerks. der Doppelpunkt, der normalerweise mit laufwerkspezifiken verwendet wird, ist nicht enthalten. Dieses Segment ist immer erforderlich.

Das *Titel* Segment ist die Nummer des zu Wiedergabe enden Titels. Es ist nicht erforderlich, es sei denn, Sie möchten die Wiedergabe an einem bestimmten Titel oder in einem bestimmten Kapitel eines bestimmten Titels starten.

Das *Kapitel* Segment ist die Nummer des zu Wiedergabe enden Kapitels. Es ist nicht erforderlich, es sei denn, Sie möchten die Wiedergabe in einem bestimmten Kapitel eines bestimmten Titels starten.

Das contentdir-Argument ist der Pfad zu einem Video \_ TS. Die IFO-Datei, die sich im lokalen Speicher oder auf einer Netzwerkfreigabe befinden kann. Wenn Sie dieses Segment einschließen, wird das *Laufwerk* Segment ignoriert, obwohl es noch erforderlich ist. Wenn Sie auch das *Titel* Segment oder die *Titel* -und *Kapitel* Segmente einschließen, sind Sie relativ zum im contentdir-Segment angegebenen DVD-Inhalt, nicht zum *Laufwerks* Segment.

Im folgenden Beispiel wird das wmpdvd-Protokoll verwendet, um die DVD von Anfang an wiederzugeben, als ob Sie automatisch gestartet wird.


```C++
player.url = "wmpdvd://F";
```



Im folgenden Beispiel wird das wmpdvd-Protokoll verwendet, um die DVD am Anfang des angegebenen Titels wiederzugeben.


```C++
player.url = "wmpdvd://F/2";
```



Im folgenden Beispiel wird das wmpdvd-Protokoll verwendet, um die DVD aus dem angegebenen Kapitel wiederzugeben.


```C++
player.url = "wmpdvd://F/2/4";
```



Im folgenden Beispiel wird das wmpdvd-Protokoll verwendet, um DVD-Inhalt aus lokalem Speicher wiederzugeben. Die *Pfad* Zeichenfolge endet mit dem Ordner, der die Video- \_ TS enthält. IFO-Datei; der Dateiname ist nicht enthalten. In diesem Beispiel hat der Wert des *Laufwerks* Segments keine Auswirkung, obwohl es erforderlich ist, und die Wiedergabe beginnt in Kapitel 4 von Titel 2.


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



Das Zuweisen einer wmpdvd-Zeichenfolge zur **URL** -Eigenschaft erfordert Windows Media Player 9 oder höher.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Unterstützte Protokolle und Dateitypen**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




