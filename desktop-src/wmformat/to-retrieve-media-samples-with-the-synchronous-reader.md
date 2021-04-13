---
title: So rufen Sie Medien Beispiele mit dem synchronen Reader ab
description: So rufen Sie Medien Beispiele mit dem synchronen Reader ab
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Advanced Systems Format (ASF), Abrufen von Medien Beispielen
- ASF (Advanced Systems Format), Abrufen von Medien Beispielen
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, Abrufen von Medien Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389875"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a><span data-ttu-id="41eaa-108">So rufen Sie Medien Beispiele mit dem synchronen Reader ab</span><span class="sxs-lookup"><span data-stu-id="41eaa-108">To Retrieve Media Samples with the Synchronous Reader</span></span>

<span data-ttu-id="41eaa-109">Sie müssen jede Stichprobe einzeln vom synchronen Reader anfordern.</span><span class="sxs-lookup"><span data-stu-id="41eaa-109">You must request each sample one at a time from the synchronous reader.</span></span> <span data-ttu-id="41eaa-110">Dadurch erhalten Sie mehr Kontrolle über die Beispiele, die Sie erhalten und wann Sie empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="41eaa-110">This gives you more control over the samples you receive and when you receive them.</span></span>

<span data-ttu-id="41eaa-111">Verwenden Sie die [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) -Methode, um ein Beispiel abzurufen.</span><span class="sxs-lookup"><span data-stu-id="41eaa-111">Use the [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) method to retrieve a sample.</span></span> <span data-ttu-id="41eaa-112">Sie müssen hauptsächlich Zeiger auf Variablen übergeben, die mit Informationen zu dem Beispiel gefüllt werden, das als Parameter abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="41eaa-112">You need to pass mostly pointers to variables that will be filled with information about the sample retrieved as parameters.</span></span> <span data-ttu-id="41eaa-113">Der einzige Eingabeparameter ist *wstreamnum*.</span><span class="sxs-lookup"><span data-stu-id="41eaa-113">The only input parameter is *wStreamNum*.</span></span> <span data-ttu-id="41eaa-114">Wenn Sie eine streamnummer übergeben, ruft **getnextsample** das nächste Beispiel mit der angegebenen streamnummer ab.</span><span class="sxs-lookup"><span data-stu-id="41eaa-114">If you pass a stream number, **GetNextSample** will retrieve the next sample with the specified stream number.</span></span> <span data-ttu-id="41eaa-115">Wenn Sie 0 (null) für *wstreamnum* übergeben, wird das nächste Beispiel, das in der Datei chronologisch vorkommt, abgerufen.</span><span class="sxs-lookup"><span data-stu-id="41eaa-115">If you pass zero for *wStreamNum*, the next sample that occurs chronologically in the file is retrieved.</span></span>

<span data-ttu-id="41eaa-116">Standardmäßig ruft der synchrone Reader alle Beispiele aus den Ausgaben in einer Datei in chronologischer Reihenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="41eaa-116">By default, the synchronous reader retrieves all of the samples from the outputs in a file in chronological order.</span></span> <span data-ttu-id="41eaa-117">Wenn Sie **getnextsample** aufrufen und keine weiteren abzurufenden Beispiele vorhanden sind, werden keine weiteren Beispiele zurückgegeben, bei denen es sich um \_ \_ \_ \_ einen Fehlercode handelt.</span><span class="sxs-lookup"><span data-stu-id="41eaa-117">If you call **GetNextSample** and there are no more samples to get, it will return NS\_E\_NO\_MORE\_SAMPLES, which is a failed error code.</span></span> <span data-ttu-id="41eaa-118">Wenn Sie daher codieren, können Sie einfach Beispiele durchlaufen, bis die Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="41eaa-118">When coding therefore, you can simply loop through samples until the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="41eaa-119">Um sicherzustellen, dass der synchrone Reader korrekte Beispiel dauern für Videostreams bereitstellt, müssen Sie zuerst die Datenstrom Ausgabe konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="41eaa-119">To ensure that the synchronous reader delivers correct sample durations for video streams, you must first configure the stream output.</span></span> <span data-ttu-id="41eaa-120">Nennen Sie die [**iwmsyncreader:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) -Methode, um die g \_ wszvideosampledurations-Einstellung auf " **true**" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="41eaa-120">Call the [**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) method to set the g\_wszVideoSampleDurations setting to **TRUE**.</span></span>

 

<span data-ttu-id="41eaa-121">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="41eaa-121">Example Code</span></span>

<span data-ttu-id="41eaa-122">Im folgenden Beispielcode wird gezeigt, wie **getnextsample** zum Abrufen aller Beispiele in einer Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41eaa-122">The following example code shows how to use **GetNextSample** to retrieve all samples in a file.</span></span>


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a><span data-ttu-id="41eaa-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41eaa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41eaa-124">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="41eaa-124">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="41eaa-125">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="41eaa-125">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




