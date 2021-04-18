---
title: So verwenden Sie einen Skript Datenstrom
description: So verwenden Sie einen Skript Datenstrom
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media-Format-SDK, Skript Datenströme
- Advanced Systems Format (ASF), Skript Datenströme
- ASF (Advanced Systems Format), Skript Datenströme
- Skript Datenströme, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311447"
---
# <a name="to-use-a-script-stream"></a>So verwenden Sie einen Skript Datenstrom

In diesem Abschnitt wird beschrieben, wie Skript Daten für die Einbindung in eine Datei an den Writer gesendet werden. Informationen zum Einschließen von Skript Datenströmen in Profile finden Sie unter [Konfigurieren beliebiger Streamtypen](configuring-arbitrary-stream-types.md).

Jedes Skript besteht aus zwei Zeichen folgen, einer *Typzeichenfolge* und einer *Argument* Zeichenfolge.

Die Skript Daten müssen formatiert werden, bevor Sie an den Writer gesendet werden. Die Zeichen folgen müssen verkettet werden, durch ein **null** -Zeichen getrennt und mit einem **null** -Zeichen beendet werden. Das folgende Beispiel zeigt ein legitimer Skript:



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | \\0 | h.   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | a   | d   | a   | t   | u   | m   | .   | c   | o   | m   | \\0 |



 

Jedes Paar von Skript Befehlen sollte als Beispiel für den Writer geschrieben werden. Weitere Informationen zum Schreiben von Beispielen finden [Sie unter so schreiben Sie Beispiele](to-write-samples.md).

Beim Wiedergeben der ASF-Datei werden die Skript Befehle vom Reader (oder synchronen Reader) in der Präsentationszeit Reihenfolge übermittelt. Es liegt in der Verantwortung der Anwendung, die beiden Zeichen folgen zu analysieren und auf den Skript Befehl zu reagieren.

> [!Note]  
> Wenn Sie DRM zum Verschlüsseln einer Datei verwenden, kann kein Skript Befehl eine Präsentationszeit von 0 aufweisen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Skript Befehlen**](using-script-commands.md)
</dt> </dl>

 

 




