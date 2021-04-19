---
description: Festlegen der Wiedergabe Rate
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Festlegen der Wiedergabe Rate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106338849"
---
# <a name="setting-the-playback-rate"></a>Festlegen der Wiedergabe Rate

Um die Wiedergabe Rate zu ändern, rufen Sie die [**imediaseeking:: Server trate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) -Methode auf. Geben Sie die neue Rate als Bruchteil der ursprünglichen Rate an. Verwenden Sie z. b. Folgendes, um die Geschwindigkeit mit zweimal normaler Geschwindigkeit wiederzugeben:


```C++
pSeek->SetRate(2.0)
```



Die Sätze größer als 1 sind schneller als üblich. Die Raten zwischen null und eins sind langsamer als normal. Negative Raten werden als Rückwärts Wiedergabe definiert, aber in der Praxis wird Sie von den meisten Filtern nicht unterstützt. Zurzeit unterstützt keiner der standardmäßigen DirectShow-Filter die umgekehrte Wiedergabe.

Unabhängig von der Wiedergabe Rate werden die aktuelle Position und die Position des Stopps immer relativ zur ursprünglichen Quelle ausgedrückt. Wenn eine Quelldatei z. b. 20 Sekunden lang mit normaler Wiedergabe Rate ist, wird durch das Festlegen der aktuellen Position auf 10 Sekunden die Mitte der Datei gesucht. Wenn die Wiedergabe Rate den Wert 2,0 hat, die Endposition 20 Sekunden beträgt und Sie die 10-Sekunden-Position suchen, wird die Datei für 5 Sekunden der Echt Zeit wiedergegeben: 10 Sekunden, bei der doppelten Wiedergabe. Bei einer Wiedergabe Rate von 2,0 erhöht sich die aktuelle Position um die doppelte Geschwindigkeit der Referenzuhr.

 

 



