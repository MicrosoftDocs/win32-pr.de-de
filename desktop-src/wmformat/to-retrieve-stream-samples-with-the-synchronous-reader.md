---
title: So rufen Sie streambeispiele mit dem synchronen Reader ab
description: So rufen Sie streambeispiele mit dem synchronen Reader ab
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Advanced Systems Format (ASF), Abrufen von streambeispielen
- ASF (Advanced Systems Format), Abrufen von streambeispielen
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, Abrufen von streambeispielen
- Streams, Abrufen von Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101254"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a><span data-ttu-id="872a3-109">So rufen Sie streambeispiele mit dem synchronen Reader ab</span><span class="sxs-lookup"><span data-stu-id="872a3-109">To Retrieve Stream Samples with the Synchronous Reader</span></span>

<span data-ttu-id="872a3-110">Wie der asynchrone Reader kann der synchrone Reader Beispiele nach streamnummer abrufen.</span><span class="sxs-lookup"><span data-stu-id="872a3-110">Like the asynchronous reader, the synchronous reader can retrieve samples by stream number.</span></span> <span data-ttu-id="872a3-111">Im Gegensatz zum asynchronen Reader kann der synchrone Reader sowohl komprimierte als auch unkomprimierte streambeispiele bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="872a3-111">Unlike the asynchronous reader, the synchronous reader can deliver stream samples either compressed or uncompressed.</span></span>

<span data-ttu-id="872a3-112">Um streambeispiele zu erhalten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="872a3-112">To receive stream samples, perform the following steps.</span></span>

1.  <span data-ttu-id="872a3-113">Geben Sie in einem beliebigen Zeitraum vor oder während der Wiedergabe [**iwmsynkreader:: abtreadstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) an, und übergeben Sie die gewünschte streamnummer.</span><span class="sxs-lookup"><span data-stu-id="872a3-113">Any time before or during playback, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passing the desired stream number.</span></span>
2.  <span data-ttu-id="872a3-114">Rufen Sie Beispiele mit fortgesetzten Aufrufen von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)ab.</span><span class="sxs-lookup"><span data-stu-id="872a3-114">Retrieve samples with continued calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span>

<span data-ttu-id="872a3-115">Sie können überprüfen, ob ein Datenstrom für die Beispiel Übermittlung ausgewählt ist, indem Sie [**iwmsyncreader:: getreadstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="872a3-115">You can check whether a stream is selected for sample delivery by calling [**IWMSyncReader::GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span></span>

## <a name="related-topics"></a><span data-ttu-id="872a3-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="872a3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="872a3-117">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="872a3-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="872a3-118">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="872a3-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




