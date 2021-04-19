---
title: Verwenden von Inverse Telecine
description: Verwenden von Inverse Telecine
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- SDK für Windows Media-Format, Inverse Telecine
- Windows Media-Format-SDK, telecine
- Advanced Systems Format (ASF), Inverse Telecine
- ASF (Advanced Systems Format), Inverse Telecine
- Advanced Systems Format (ASF), telecine
- ASF (Advanced Systems Format), telecine
- Inverse Telecine
- Telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106341510"
---
# <a name="to-use-inverse-telecine"></a><span data-ttu-id="20699-111">Verwenden von Inverse Telecine</span><span class="sxs-lookup"><span data-stu-id="20699-111">To Use Inverse Telecine</span></span>

<span data-ttu-id="20699-112">Telecine ist der Prozess der Umstellung von Film, der über 24 Frames pro Sekunde verfügt, in Video, das 60 Felder (halbframes) pro Sekunde enthält.</span><span class="sxs-lookup"><span data-stu-id="20699-112">Telecine is the process of converting film, which has 24 frames per second, to video, which has 60 fields (half frames) per second.</span></span> <span data-ttu-id="20699-113">Bei diesem Prozess werden Bilder aus jedem Filmframe in mehreren Video Feldern abgelegt.</span><span class="sxs-lookup"><span data-stu-id="20699-113">This process puts images from each film frame in multiple video fields.</span></span>

<span data-ttu-id="20699-114">Wenn Sie ein Video, das aus einem Film mithilfe von telecine erstellt wurde, Digital codieren, kann der Komprimierungs Vorgang Bewegungsartefakte und andere Beeinträchtigungen der Qualität verursachen.</span><span class="sxs-lookup"><span data-stu-id="20699-114">When you digitally encode a video that was created from film by using telecine, the compression process can cause motion artifacts and other degradations in quality.</span></span> <span data-ttu-id="20699-115">Um zu vermeiden, dass die Qualität der digitalen Ausgabe beeinträchtigt wird, unterstützt der Windows Media Video 9-Codec Inverse Telecine.</span><span class="sxs-lookup"><span data-stu-id="20699-115">To avoid affecting the quality of the digital output, the Windows Media Video 9 codec supports inverse telecine.</span></span> <span data-ttu-id="20699-116">Wenn Sie Inverse Telecine verwenden, rekonstruiert der Codec die ursprünglichen 24 Filmframes pro Sekunde aus dem Eingabe Video, bevor der Inhalt codiert wird.</span><span class="sxs-lookup"><span data-stu-id="20699-116">When using inverse telecine, the codec reconstructs the original 24 film frames per second from the input video before encoding the content.</span></span>

<span data-ttu-id="20699-117">Um Inverse Telecine verwenden zu können, müssen Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="20699-117">To use inverse telecine, you must:</span></span>

-   <span data-ttu-id="20699-118">Verwenden Sie ein Profil mit einem Videostream, der auf 24 Frames pro Sekunde festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="20699-118">Use a profile with a video stream set to 24 frames per second.</span></span>
-   <span data-ttu-id="20699-119">Informieren Sie sich über die Feld Konfiguration des Eingangs Videos.</span><span class="sxs-lookup"><span data-stu-id="20699-119">Know the field configuration of the input video.</span></span>

<span data-ttu-id="20699-120">Führen Sie die folgenden Schritte aus, um Inverse Telecine für eine Eingabe für den Writer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="20699-120">To use inverse telecine for an input to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="20699-121">Richten Sie den Writer wie gewohnt ein.</span><span class="sxs-lookup"><span data-stu-id="20699-121">Set up the writer as usual.</span></span> <span data-ttu-id="20699-122">Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="20699-122">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="20699-123">Bevor Sie mit dem Schreiben von Beispielen beginnen, erhalten Sie einen Zeiger auf die [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) -Schnittstelle, indem Sie **iwmwriter:: QueryInterface** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="20699-123">Before beginning to write samples, obtain a pointer to the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface by calling **IWMWriter::QueryInterface**.</span></span>
3.  <span data-ttu-id="20699-124">Identifizieren Sie den zu rekonstruierenden Stream, indem Sie für die gewünschte Eingabe Nummer [**IWMWriterAdvanced2:: \* tinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="20699-124">Identify the stream to be reconstructed by calling [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) for the desired input number.</span></span> <span data-ttu-id="20699-125">Übergeben Sie g \_ wszdeinterlacemode als Einstellung und WM \_ DM \_ deinterlace \_ invertartelecine als Wert.</span><span class="sxs-lookup"><span data-stu-id="20699-125">Pass g\_wszDeinterlaceMode as the setting and WM\_DM\_DEINTERLACE\_INVERSETELECINE as the value.</span></span>
4.  <span data-ttu-id="20699-126">**Setinputsetting** wird erneut aufgerufen, um g \_ wszinitialpatternforinversetelecine festzulegen.</span><span class="sxs-lookup"><span data-stu-id="20699-126">Call **SetInputSetting** again to set g\_wszInitialPatternForInverseTelecine.</span></span>
5.  <span data-ttu-id="20699-127">Schreiben Sie die Datei wie gewohnt.</span><span class="sxs-lookup"><span data-stu-id="20699-127">Write the file as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20699-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20699-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20699-129">**Erweiterte Themen**</span><span class="sxs-lookup"><span data-stu-id="20699-129">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="20699-130">**Iwmwriter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="20699-130">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="20699-131">**IWMWriterAdvanced2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="20699-131">**IWMWriterAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




