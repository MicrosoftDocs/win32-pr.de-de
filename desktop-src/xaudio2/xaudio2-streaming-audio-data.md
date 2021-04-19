---
description: Streaming ist der Prozess, bei dem nur ein kleiner Teil einer Wiedergabe-Audiodatei im Arbeitsspeicher beibehalten wird. Dadurch können große Audiodateien, z. b. Hintergrundmusik, abgespielt werden, und es ist nicht viel Arbeitsspeicher erforderlich.
ms.assetid: 7a938ea6-15ef-66b1-0276-88eabf9a722b
title: XAudio2 streamingaudiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1766b20f539f8bbe4d11204b681b7eddca58578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369819"
---
# <a name="xaudio2-streaming-audio-data"></a>XAudio2 streamingaudiodaten

Streaming ist der Prozess, bei dem nur ein kleiner Teil einer Wiedergabe-Audiodatei im Arbeitsspeicher beibehalten wird. Dadurch können große Audiodateien, z. b. Hintergrundmusik, abgespielt werden, und es ist nicht viel Arbeitsspeicher erforderlich.

Wenn eine Audiodatei gestreamt wird, werden die Daten in Blöcken aus dem Datenträger gelesen, anstatt die gesamte Datei auf einmal zu laden. Streaming wird durch asynchrones Lesen von Audiodaten in eine Warteschlange von Datenträger Puffern erreicht. Jeder Puffer wird aufgefüllt und dann an eine Quellsprache gesendet. Nachdem die Stimme für die Wiedergabe eines Puffers abgeschlossen ist, steht der Puffer wieder zum Lesen zur Verfügung. Durch das Durchlaufen der Datenträger Puffer auf diese Weise kann eine große Audiodatei abgespielt werden, während nur ein Teil der Daten geladen wird. Der streamingcode sollte in einem separaten Thread abgelegt werden, in dem er sich im Standbymodus befindet, während er darauf wartet, dass Datenträger-und audiovorgänge mit langer Ausführungszeit Eine Rückruf Klasse wird verwendet, um den Thread zu reaktivieren, indem Ereignisse ausgelöst werden, wenn audiovorgänge abgeschlossen sind.

Ein Beispiel dafür, wie das Streaming mit XAudio2 erreicht werden kann, finden Sie unter Gewusst [wie: Streamen eines Sounds von einem](how-to--stream-a-sound-from-disk.md)Datenträger.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streaming von Audiodaten](streaming-audio-data.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 



