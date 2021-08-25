---
description: Streaming ist der Prozess, bei dem nur ein kleiner Teil einer audiodatei im Arbeitsspeicher beibehalten wird. Dadurch können große Audiodateien wie Hintergrundaufnahmen abgespielt werden, und es wird keine große Menge an Arbeitsspeicher verwendet.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: XAudio2 Streaming Audio Data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df15420adce8f8807c3f969615a2cf6d5b51981e03fd7067e2c1c3348d1b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805390"
---
# <a name="xaudio2-streaming-audio-data"></a>XAudio2 Streaming Audio Data

Streaming ist der Prozess, bei dem nur ein kleiner Teil einer audiodatei im Arbeitsspeicher beibehalten wird. Dadurch können große Audiodateien wie Hintergrundaufnahmen abgespielt werden, und es wird keine große Menge an Arbeitsspeicher verwendet.

Wenn eine Audiodatei gestreamt wird, werden ihre Daten in Blocken vom Datenträger gelesen, anstatt die gesamte Datei gleichzeitig zu laden. Das Streaming erfolgt durch asynchrones Lesen von Audiodaten in eine Warteschlange von Datenträgerpuffern. Jeder Puffer wird gefüllt und dann an eine Quellstimme übermittelt. Nachdem die Stimme die Wiedergabe eines Puffers beendet hat, steht der Puffer wieder zum Lesen zur Verfügung. Wenn Sie die Datenträgerpuffer auf diese Weise durchschleifen, kann eine große Audiodatei abgespielt werden, während nur ein Teil der Daten geladen wird. Der Streamingcode sollte in einem separaten Thread platziert werden, in dem er während des Wartens auf den Abschluss von Datenträger- und Audiovorgängen mit langer Laufzeit in den Ruhezustand gebracht werden kann. Eine Rückrufklasse wird verwendet, um den Thread zu reaktivieren, indem Ereignisse ausgelöst werden, wenn Audiovorgänge abgeschlossen sind.

Ein Beispiel dafür, wie Streaming mit XAudio2 erreicht werden kann, finden Sie unter [How to: Stream a Sound from Disk](how-to--stream-a-sound-from-disk.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streaming von Audiodaten](streaming-audio-data.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 



