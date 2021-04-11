---
title: Verwalten von Waveform-Audio Aufzeichnung
description: Verwalten von Waveform-Audio Aufzeichnung
ms.assetid: a44f7c33-54d6-4ba7-bc57-b63c8b205392
keywords:
- Wellenform-Audiodaten, aufzeichnen
- Waveform-Audioschnittstelle, aufzeichnen
- Aufzeichnen von Wellenform-Audiodaten, Info
- Wavehdr-Struktur
- waveinaddbuffer-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539f722a705d489064d38eccdf6d89e80ccb1518
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314774"
---
# <a name="managing-waveform-audio-recording"></a><span data-ttu-id="8f7dd-108">Verwalten von Waveform-Audio Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="8f7dd-108">Managing Waveform-Audio Recording</span></span>

<span data-ttu-id="8f7dd-109">Nachdem Sie ein Waveform-Audioeingabegerät geöffnet haben, können Sie mit dem Aufzeichnen von Waveform-Audiodaten beginnen.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-109">After you open a waveform-audio input device, you can begin recording waveform-audio data.</span></span> <span data-ttu-id="8f7dd-110">Waveform-Audiodaten werden in von der Anwendung bereitgestellten Puffern aufgezeichnet, die durch eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-110">Waveform-audio data is recorded into application-supplied buffers specified by a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure.</span></span> <span data-ttu-id="8f7dd-111">Diese Datenblöcke müssen vorbereitet werden, bevor Sie verwendet werden. Weitere Informationen finden Sie unter [Audiodatenblöcke](audio-data-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="8f7dd-111">These data blocks must be prepared before they are used; for more information, see [Audio Data Blocks](audio-data-blocks.md).</span></span>

<span data-ttu-id="8f7dd-112">Windows stellt die folgenden Funktionen zum Verwalten der Waveform-Audioaufzeichnung bereit.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-112">Windows provides the following functions to manage waveform-audio recording.</span></span>



| <span data-ttu-id="8f7dd-113">Funktion</span><span class="sxs-lookup"><span data-stu-id="8f7dd-113">Function</span></span>                                   | <span data-ttu-id="8f7dd-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f7dd-114">Description</span></span>                                                                                |
|--------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f7dd-115">**waveinaddbuffer**</span><span class="sxs-lookup"><span data-stu-id="8f7dd-115">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) | <span data-ttu-id="8f7dd-116">Sendet einen Puffer an den Gerätetreiber, damit er mit aufgezeichneten Wellenform-Audiodaten gefüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-116">Sends a buffer to the device driver so it can be filled with recorded waveform-audio data.</span></span> |
| [<span data-ttu-id="8f7dd-117">**waveingereset**</span><span class="sxs-lookup"><span data-stu-id="8f7dd-117">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)         | <span data-ttu-id="8f7dd-118">Hält die Wellenform-Audioaufzeichnung an und markiert alle ausstehenden Puffer als abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-118">Stops waveform-audio recording and marks all pending buffers as done.</span></span>                      |
| [<span data-ttu-id="8f7dd-119">**wavanstart**</span><span class="sxs-lookup"><span data-stu-id="8f7dd-119">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)         | <span data-ttu-id="8f7dd-120">Startet die Waveform-Audioaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-120">Starts waveform-audio recording.</span></span>                                                           |
| [<span data-ttu-id="8f7dd-121">**WaveIn-Ende**</span><span class="sxs-lookup"><span data-stu-id="8f7dd-121">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)           | <span data-ttu-id="8f7dd-122">Beendet die Wellenform-Audioaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-122">Stops waveform-audio recording.</span></span>                                                            |



 

<span data-ttu-id="8f7dd-123">Verwenden Sie die Funktion [**waveinaddbuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) , um Puffer an den Gerätetreiber zu senden.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-123">Use the [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer) function to send buffers to the device driver.</span></span> <span data-ttu-id="8f7dd-124">Wenn die Puffer mit aufgezeichneten Wellenform-Audiodaten gefüllt sind, wird die Anwendung in Abhängigkeit von dem Flag, das beim Öffnen des Geräts angegeben wurde, mit einer Fenster Meldung, einer Rückruf Meldung, einer Thread Nachricht oder einem Ereignis benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-124">As the buffers are filled with recorded waveform-audio data, the application is notified with a window message, callback message, thread message, or event, depending on the flag specified when the device was opened.</span></span>

<span data-ttu-id="8f7dd-125">Bevor Sie mit der Aufzeichnung mit [**waveinstart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)beginnen, sollten Sie mindestens einen Puffer an den Treiber senden, oder es können eingehende Daten verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-125">Before you begin recording by using [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart), you should send at least one buffer to the driver, or incoming data could be lost.</span></span>

<span data-ttu-id="8f7dd-126">Bevor Sie das Gerät mithilfe von [**waveinclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)schließen, wenden Sie [**waveinreset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) an, um alle ausstehenden Datenblöcke als abgeschlossen zu markieren.</span><span class="sxs-lookup"><span data-stu-id="8f7dd-126">Before closing the device using [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose), call [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) to mark any pending data blocks as being done.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f7dd-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8f7dd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f7dd-128">Aufzeichnen von Waveform-Audiodaten</span><span class="sxs-lookup"><span data-stu-id="8f7dd-128">Recording Waveform Audio</span></span>](recording-waveform-audio.md)
</dt> </dl>

 

 