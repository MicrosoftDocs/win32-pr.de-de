---
title: So verwenden Sie einen Skriptstream
description: So verwenden Sie einen Skriptstream
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, Skriptstreams
- Advanced Systems Format (ASF), Skriptstreams
- ASF (Advanced Systems Format), Skriptstreams
- Skriptstreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444731"
---
# <a name="to-use-a-script-stream"></a>So verwenden Sie einen Skriptstream

In diesem Abschnitt wird beschrieben, wie Skriptdaten zur Aufnahme in eine Datei an den Writer gesendet werden. Informationen zum Verwenden von Skriptstreams in Profile finden Sie unter Configuring Arbitrary Stream Types (Konfigurieren [beliebiger Streamtypen).](configuring-arbitrary-stream-types.md)

Jedes Skript besteht aus zwei Zeichenfolgen, einer *Typzeichenfolge* und einer *Argumentzeichenfolge.*

Die Skriptdaten müssen formatiert werden, bevor sie an den Writer gesendet werden. Die Zeichenfolgen sollten verkettet, durch ein **NULL-Zeichen** getrennt und mit einem **NULL-Zeichen beendet** werden. Das folgende Beispiel zeigt ein legitimes Skript:



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | &nbsp; | h   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | a   | d   | a   | t   | u   | m   | .   | c   | o   | m   | &nbsp; |



 

Jedes Skriptbefehlspaar sollte als Beispiel in den Writer geschrieben werden. Weitere Informationen zum Schreiben von Beispielen finden Sie unter [To Write Samples](to-write-samples.md).

Wenn die ASF-Datei abgespielt wird, werden die Skriptbefehle vom Reader (oder synchronen Reader) in der Reihenfolge der Präsentationszeit übermittelt. Die Anwendung ist dafür verantwortlich, die beiden Zeichenfolgen zu analysieren und auf den Skriptbefehl zu reagieren.

> [!Note]  
> Bei Verwendung von DRM zum Verschlüsseln einer Datei kann kein Skriptbefehl eine Präsentationszeit von 0 haben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Skriptbefehlen**](using-script-commands.md)
</dt> </dl>

 

 




