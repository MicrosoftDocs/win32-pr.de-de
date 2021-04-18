---
title: Beliebige und vorkomprimierte streameingaben
description: Beliebige und vorkomprimierte streameingaben
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- Advanced Systems Format (ASF), beliebige streameingaben
- ASF (Advanced Systems Format), beliebige streameingaben
- Profile, beliebige streameingaben
- Codecs, beliebige streameingaben
- Advanced Systems Format (ASF), vorkomprimierte streameingaben
- ASF (Advanced Systems Format), vorkomprimierte streameingaben
- Profile, vorkomprimierte streameingaben
- Codecs, vorkomprimierte streameingaben
- vorkomprimierte streameingaben
- beliebige Datenstrom Eingaben
- Streams, beliebige streameingaben
- Streams, vorkomprimierte streameingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106338445"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a><span data-ttu-id="1c8fd-115">Beliebige und vorkomprimierte streameingaben</span><span class="sxs-lookup"><span data-stu-id="1c8fd-115">Arbitrary and Precompressed Stream Inputs</span></span>

<span data-ttu-id="1c8fd-116">Nur Eingaben, die von einem der Windows Media-Codecs komprimiert werden, verfügen über mehrere mögliche Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-116">Only inputs that are to be compressed by one of the Windows Media codecs have multiple possible inputs.</span></span> <span data-ttu-id="1c8fd-117">Die anderen Typen möglicher Eingaben sind willkürliche Eingaben und vorkomprimierte Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-117">The other types of possible inputs are arbitrary inputs and precompressed inputs.</span></span> <span data-ttu-id="1c8fd-118">Die Anforderungen für die Eingabeformate für diese Typen werden in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-118">The requirements for input formats for these types are described in this section.</span></span>

## <a name="arbitrary-stream-inputs"></a><span data-ttu-id="1c8fd-119">Beliebige Datenstrom Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c8fd-119">Arbitrary Stream Inputs</span></span>

<span data-ttu-id="1c8fd-120">Eingaben für beliebige Streamtypen sind identisch mit den im Profil beschriebenen Datenstrom Formaten.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-120">Inputs for arbitrary stream types are the same as the stream formats described in the profile.</span></span> <span data-ttu-id="1c8fd-121">Sie sollten keine Eingabeformate für diese Typen festlegen.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-121">You should not have to set input formats for these types.</span></span>

## <a name="precompressed-stream-inputs"></a><span data-ttu-id="1c8fd-122">Vorkomprimierte streameingaben</span><span class="sxs-lookup"><span data-stu-id="1c8fd-122">Precompressed Stream Inputs</span></span>

<span data-ttu-id="1c8fd-123">Wenn Sie einen Stream aus einer Datei in eine andere kopieren, übergeben Sie bereits komprimierte Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-123">When copying a stream from one file to another, you pass samples that are already compressed.</span></span> <span data-ttu-id="1c8fd-124">In diesem Fall müssen Sie das Eingabe Eigenschafts Objekt auf **null** festlegen, um den Writer darüber zu informieren, dass die übergebenen Daten nicht überprüft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-124">In this case, you must set the input properties object to **NULL** to inform the writer that it does not need to validate the data you are passing in.</span></span> <span data-ttu-id="1c8fd-125">Um das Eingabeformat auf **null** festzulegen, nennen Sie [**iwmwriter:: SetInput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) Eigenschaften, und übergeben Sie **null** als zweiten Parameter.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-125">To set the input format to **NULL**, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and pass **NULL** as the second parameter.</span></span> <span data-ttu-id="1c8fd-126">Wenn Sie diese Methode mit einem **null** -Parameter aufrufen, müssen Sie den Aufruf vor dem Aufrufen von [**beginwriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)durchführen.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-126">When calling this method with a **NULL** parameter, you must make the call before calling [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="1c8fd-127">Wenn Sie vorkomprimierte Streams verwenden, müssen Sie vor dem Schreiben manuell Codec-Informationen in den Dateiheader kopieren.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-127">When using precompressed streams, you must manually copy codec information to the file header before writing.</span></span> <span data-ttu-id="1c8fd-128">Rufen Sie zum Abrufen der Codec-Informationen [**IWMHeaderInfo2:: getcodecinfocount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) und [**IWMHeaderInfo2:: getcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) auf, um die Codecs aufzulisten, die der Datei im Reader zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-128">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="1c8fd-129">Wählen Sie die Codec-Informationen aus, die der Datenstrom Konfiguration des vorkomprimierten Streams entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-129">Select the codec information that matches the stream configuration of the precompressed stream.</span></span> <span data-ttu-id="1c8fd-130">Legen Sie dann die Codec-Informationen im Writer durch Aufrufen von [**IWMHeaderInfo3:: addcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)fest, und übergeben Sie dabei die Informationen, die vom Reader abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1c8fd-130">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c8fd-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c8fd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c8fd-132">**Arbeiten mit Eingaben**</span><span class="sxs-lookup"><span data-stu-id="1c8fd-132">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




