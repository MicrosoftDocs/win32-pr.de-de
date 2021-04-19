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
# <a name="xaudio2-streaming-audio-data"></a><span data-ttu-id="95b8b-104">XAudio2 streamingaudiodaten</span><span class="sxs-lookup"><span data-stu-id="95b8b-104">XAudio2 Streaming Audio Data</span></span>

<span data-ttu-id="95b8b-105">Streaming ist der Prozess, bei dem nur ein kleiner Teil einer Wiedergabe-Audiodatei im Arbeitsspeicher beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="95b8b-105">Streaming is the process of maintaining only a small portion of a playing audio file in memory.</span></span> <span data-ttu-id="95b8b-106">Dadurch können große Audiodateien, z. b. Hintergrundmusik, abgespielt werden, und es ist nicht viel Arbeitsspeicher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="95b8b-106">This allows large audio files such as background music to be played, and not take up a large amount of memory.</span></span>

<span data-ttu-id="95b8b-107">Wenn eine Audiodatei gestreamt wird, werden die Daten in Blöcken aus dem Datenträger gelesen, anstatt die gesamte Datei auf einmal zu laden.</span><span class="sxs-lookup"><span data-stu-id="95b8b-107">When an audio file is streamed, its data is read from disk in chunks rather than loading the entire file at once.</span></span> <span data-ttu-id="95b8b-108">Streaming wird durch asynchrones Lesen von Audiodaten in eine Warteschlange von Datenträger Puffern erreicht.</span><span class="sxs-lookup"><span data-stu-id="95b8b-108">Streaming is accomplished by asynchronously reading audio data into a queue of disk buffers.</span></span> <span data-ttu-id="95b8b-109">Jeder Puffer wird aufgefüllt und dann an eine Quellsprache gesendet.</span><span class="sxs-lookup"><span data-stu-id="95b8b-109">Each buffer is filled, and then submitted to a source voice.</span></span> <span data-ttu-id="95b8b-110">Nachdem die Stimme für die Wiedergabe eines Puffers abgeschlossen ist, steht der Puffer wieder zum Lesen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="95b8b-110">After the voice finishes playing a buffer, the buffer becomes available for reading again.</span></span> <span data-ttu-id="95b8b-111">Durch das Durchlaufen der Datenträger Puffer auf diese Weise kann eine große Audiodatei abgespielt werden, während nur ein Teil der Daten geladen wird.</span><span class="sxs-lookup"><span data-stu-id="95b8b-111">Looping through the disk buffers in this manner allows a large audio file to be played while only a portion of its data is loaded.</span></span> <span data-ttu-id="95b8b-112">Der streamingcode sollte in einem separaten Thread abgelegt werden, in dem er sich im Standbymodus befindet, während er darauf wartet, dass Datenträger-und audiovorgänge mit langer Ausführungszeit</span><span class="sxs-lookup"><span data-stu-id="95b8b-112">The streaming code should be placed in a separate thread, where it can sleep while waiting for long-running disk and audio operations to finish.</span></span> <span data-ttu-id="95b8b-113">Eine Rückruf Klasse wird verwendet, um den Thread zu reaktivieren, indem Ereignisse ausgelöst werden, wenn audiovorgänge abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="95b8b-113">A callback class is used to wake the thread by triggering events when audio operations have finished.</span></span>

<span data-ttu-id="95b8b-114">Ein Beispiel dafür, wie das Streaming mit XAudio2 erreicht werden kann, finden Sie unter Gewusst [wie: Streamen eines Sounds von einem](how-to--stream-a-sound-from-disk.md)Datenträger.</span><span class="sxs-lookup"><span data-stu-id="95b8b-114">For an example of how streaming can be accomplished with XAudio2, see [How to: Stream a Sound from Disk](how-to--stream-a-sound-from-disk.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95b8b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95b8b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95b8b-116">Streaming von Audiodaten</span><span class="sxs-lookup"><span data-stu-id="95b8b-116">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="95b8b-117">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="95b8b-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 



