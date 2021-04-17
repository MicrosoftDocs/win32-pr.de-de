---
title: Anhalten oder Anhalten der Wiedergabe
description: Anhalten oder Anhalten der Wiedergabe
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Advanced Systems Format (ASF), Anhalten der Wiedergabe
- ASF (Advanced Systems Format), Anhalten der Wiedergabe
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Beenden der Wiedergabe
- ASF (Advanced Systems Format), Beenden der Wiedergabe
- Advanced Systems Format (ASF), Wiedergabe anhalten oder beenden
- ASF (Advanced Systems Format), Wiedergabe wird angehalten oder angehalten
- asynchrone Reader, Anhalten der Wiedergabe
- asynchrone Lesevorgänge, Beenden der Wiedergabe
- asynchrone Leser, Wiedergabe wird angehalten oder angehalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516598"
---
# <a name="to-pause-or-stop-playback"></a><span data-ttu-id="096d5-114">Anhalten oder Anhalten der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="096d5-114">To Pause or Stop Playback</span></span>

<span data-ttu-id="096d5-115">Wenn Sie [**iwmreader:: Start starten**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) , um mit der Wiedergabe einer Datei zu beginnen, wird der asynchrone Reader mit der Verarbeitung in seinen eigenen separaten Threads fortgesetzt, bis das Ende der Datei erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="096d5-115">When you call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) to begin playing a file, the asynchronous reader will continue processing in its own separate threads until the end of the file is reached.</span></span> <span data-ttu-id="096d5-116">Sie können die Übermittlung von Beispielen mithilfe der [**iwmreader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) -Methode oder der [**iwmreader::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) anhaltemethode anhalten oder stoppen.</span><span class="sxs-lookup"><span data-stu-id="096d5-116">You can pause or stop the delivery of samples using the [**IWMReader::Pause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) or [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) methods respectively.</span></span>

## <a name="pausing"></a><span data-ttu-id="096d5-117">Status „Wird angehalten“</span><span class="sxs-lookup"><span data-stu-id="096d5-117">Pausing</span></span>

<span data-ttu-id="096d5-118">Wenn Sie **iwmreader::P ause** aufzurufen, um die Wiedergabe einer Datei anzuhalten, verfolgt der Reader die aktuelle Position in der Datei.</span><span class="sxs-lookup"><span data-stu-id="096d5-118">When you call **IWMReader::Pause** to pause playback of a file, the reader keeps track of the current position in the file.</span></span> <span data-ttu-id="096d5-119">Um die Wiedergabe nach dem Anhalten fortzusetzen, nennen Sie [**iwmreader:: Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span><span class="sxs-lookup"><span data-stu-id="096d5-119">To resume playing after pausing, call [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span></span> <span data-ttu-id="096d5-120">Die Wiedergabe wird an dem Punkt fortgesetzt, an dem Sie angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="096d5-120">Playback will resume from the point at which it paused.</span></span>

## <a name="stopping"></a><span data-ttu-id="096d5-121">Wird beendet</span><span class="sxs-lookup"><span data-stu-id="096d5-121">Stopping</span></span>

<span data-ttu-id="096d5-122">Wenn Sie **iwmreader:: Stop** aufgerufen haben, um die Wiedergabe einer Datei anzuhalten, verfolgt der Reader keine Informationen über den Fortschritt der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="096d5-122">When you call **IWMReader::Stop** to halt playback of a file, the reader does not keep track of any information about the progress of playback.</span></span> <span data-ttu-id="096d5-123">Wenn Sie " **Stop** " und höher verwenden möchten, müssen Sie die Präsentationszeit des letzten übermittelten Beispiels speichern und in Ihrem Aufruf von " **iwmreader:: Start**" verwenden.</span><span class="sxs-lookup"><span data-stu-id="096d5-123">To use **Stop** and later return to the stopping point you must save the presentation time of the last sample delivered and use it in your call to **IWMReader::Start**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="096d5-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="096d5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="096d5-125">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="096d5-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="096d5-126">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="096d5-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




