---
description: Festlegen der Wiedergaberate
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Festlegen der Wiedergaberate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0404e67d716616a4c383c134a4fb4e75060e3094023abec52df1d38099b92b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583320"
---
# <a name="setting-the-playback-rate"></a>Festlegen der Wiedergaberate

Um die Wiedergaberate zu ändern, rufen Sie die [**IMediaSeeking::SetRate-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) auf. Geben Sie die neue Rate als Bruchteil der ursprünglichen Rate an. Um beispielsweise mit doppelt normaler Geschwindigkeit zu spielen, verwenden Sie Folgendes:


```C++
pSeek->SetRate(2.0)
```



Raten größer als eins sind schneller als normal. Die Raten zwischen 0 und 1 sind langsamer als normal. Negative Raten werden als Rückwärtswiedergabe definiert, aber in der Praxis unterstützen die meisten Filter sie nicht. Derzeit unterstützt keiner der DirectShow-Standardfilter die umgekehrte Wiedergabe.

Unabhängig von der Wiedergaberate werden die aktuelle Position und die Stoppposition immer relativ zur ursprünglichen Quelle ausgedrückt. Wenn eine Quelldatei beispielsweise bei normaler Wiedergaberate 20 Sekunden lang ist, wird durch Festlegen der aktuellen Position auf 10 Sekunden die Mitte der Datei gesucht. Wenn die Wiedergaberate 2,0 beträgt, die Stoppposition 20 Sekunden beträgt und Sie die 10-Sekunden-Position erreichen, wird die Datei 5 Sekunden lang in Echtzeit wiedergegeben: 10 Sekunden lang, bei doppelt so normaler Wiedergabegeschwindigkeit. Bei einer Wiedergaberate von 2,0 erhöht sich die aktuelle Position um das Doppelte der Rate der Referenzuhr.

 

 



