---
title: So konfigurieren Sie Quality-Based VBR
description: So konfigurieren Sie Quality-Based VBR
ms.assetid: 077a18c5-1895-4241-8c31-5f7caf38b22e
keywords:
- Streams, Konfigurieren von VBR-Streams
- Streams, Variable Bitrate (VBR)
- variablenbitrate (VBR), Streams
- VBR (Variable Bitrate), Streams
- Streams, Konfigurieren der Qualitäts basierten VBR
- variablenbitrate (VBR), Konfigurieren von Qualitäts basierter
- VBR (Variable Bitrate), Konfigurieren von Qualitäts basierter
- Profile, Konfigurieren von Qualitäts basiertem VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0b7a6ecb83c7242f82f5626a086c8aba23881f
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103948506"
---
# <a name="to-configure-quality-based-vbr"></a><span data-ttu-id="6e2c6-111">So konfigurieren Sie Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="6e2c6-111">To Configure Quality-Based VBR</span></span>

<span data-ttu-id="6e2c6-112">Mit der Qualitäts basierten VBR-Codierung (Variable Bitrate) in einem Stream können Sie eine Qualitätsstufe angeben, die für den gesamten Datenstrom beibehalten wird, unabhängig von den Anforderungen für die Bitrate.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-112">You can use quality-based variable bit rate (VBR) encoding on a stream to specify a quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>

<span data-ttu-id="6e2c6-113">Bei Qualitäts basierten VBR-Videostreams müssen Sie eine Qualitätsstufe von 1 bis 100 angeben, wobei 100 die höchste Qualität darstellt.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-113">For quality-based VBR video streams, you must specify a quality level from 1 to 100, with 100 representing the highest quality.</span></span> <span data-ttu-id="6e2c6-114">Zurzeit sind nur 30 diskrete Qualitätseinstellungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-114">At present there are only 30 discrete quality settings.</span></span> <span data-ttu-id="6e2c6-115">Die folgenden Qualitätsstufen entsprechen den diskreten Qualitätseinstellungen: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100,,,,.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-115">The following quality levels equate to discrete quality settings: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97, 100.</span></span> <span data-ttu-id="6e2c6-116">Zahlen zwischen zwei aufeinander folgenden Werten in der vorangehenden Liste entsprechen der gleichen Qualitätseinstellung wie die niedrigere Zahl.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-116">Numbers between two consecutive values in the preceding list equate to the same quality setting as the lower number.</span></span> <span data-ttu-id="6e2c6-117">Beispielsweise werden 1 und 4 aufgelistet, sodass 2 und 3 die gleiche Qualitätseinstellung wie 1 ergeben.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-117">For example, 1 and 4 are listed, so 2 and 3 both result in the same quality setting as 1.</span></span>

<span data-ttu-id="6e2c6-118">Für Audiostreams können Sie die verfügbaren Modi auflisten und ein streamkonfigurationsobjekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-118">For audio streams, you can enumerate the available modes and retrieve a stream configuration object.</span></span> <span data-ttu-id="6e2c6-119">Weitere Informationen finden [Sie unter to Enumerate Codec Formats](to-enumerate-codec-formats.md).</span><span class="sxs-lookup"><span data-stu-id="6e2c6-119">For more information, see [To Enumerate Codec Formats](to-enumerate-codec-formats.md).</span></span>

<span data-ttu-id="6e2c6-120">Wenn Sie ein Qualitäts basiertes VBR-Video verwenden, müssen Sie den **dwbitrate** -Member der [**wmvideoinfoheader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) -Struktur auf einen positiven Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-120">When using quality-based VBR video, you must set the **dwBitrate** member of the [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) structure to a positive value.</span></span> <span data-ttu-id="6e2c6-121">Dieser Wert wird vom Writer nicht verwendet, aber das Übergeben von 0 (null) oder einer negativen Zahl kann beim Schreiben zu Fehlern führen.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-121">This value is not used by the writer, but passing zero or a negative number can cause errors when writing.</span></span>

<span data-ttu-id="6e2c6-122">Führen Sie die folgenden Schritte aus, um einen Datenstrom in einem Profil zu konfigurieren, der mit einem Qualitäts basierten VBR codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-122">To configure a stream in a profile to be encoded with quality-based VBR, perform the following steps.</span></span>

1.  <span data-ttu-id="6e2c6-123">Erstellen Sie ein Profil-Manager-Objekt, indem Sie die [**wmcreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-123">Create a profile manager object by calling the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>
2.  <span data-ttu-id="6e2c6-124">Öffnen Sie ein vorhandenes Profil, dem Sie die VBR-Unterstützung hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-124">Open an existing profile to which you want to add VBR support.</span></span> <span data-ttu-id="6e2c6-125">Weitere Informationen zum Öffnen von Profilen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6e2c6-125">For more information about opening profiles, see [Working with Profiles](working-with-profiles.md).</span></span>
3.  <span data-ttu-id="6e2c6-126">Rufen Sie ein streamkonfigurationsobjekt für den Stream ab, den Sie verwenden möchten, indem Sie entweder [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) oder [**iwmprofile:: getstreambynumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-126">Get a stream configuration object for the stream you want to use by calling either [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) or [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber).</span></span>
4.  <span data-ttu-id="6e2c6-127">Abrufen eines Zeigers auf die [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle des Stream-Konfigurations Objekts durch Aufrufen von **iwmstreamconfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-127">Get a pointer to the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
5.  <span data-ttu-id="6e2c6-128">Aktivieren Sie VBR für den Datenstrom, indem Sie [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) für die Eigenschaft **g \_ wszvbrenabled** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-128">Enable VBR for the stream by calling [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) for the **g\_wszVBREnabled** property.</span></span>
6.  <span data-ttu-id="6e2c6-129">Legen Sie die Qualitätsstufe für den VBR-Stream fest, indem Sie **iwmpropertyvault:: SetProperty** für die Eigenschaft **g \_ wszvbrquality** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-129">Set the quality level for the VBR stream by calling **IWMPropertyVault::SetProperty** for the **g\_wszVBRQuality** property.</span></span>
7.  <span data-ttu-id="6e2c6-130">Legen Sie **g \_ wszvbrbitratemax** und **g \_ wszvbrbufferwindowmax** mit **iwmpropertyvault:: SetProperty** auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-130">Set **g\_wszVBRBitrateMax** and **g\_wszVBRBufferWindowMax** both to zero with **IWMPropertyVault::SetProperty**.</span></span>
8.  <span data-ttu-id="6e2c6-131">Speichern Sie die am Stream vorgenommenen Änderungen, indem Sie [**iwmprofile:: reconfigstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-131">Save the changes made to the stream by calling [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream).</span></span>
9.  <span data-ttu-id="6e2c6-132">Speichern Sie das Profil, oder übergeben Sie es an das Writer-Objekt, und beginnen Sie mit dem Schreiben.</span><span class="sxs-lookup"><span data-stu-id="6e2c6-132">Save the profile, or pass it to the writer object and start writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e2c6-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e2c6-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e2c6-134">**Konfigurieren von VBR-Streams**</span><span class="sxs-lookup"><span data-stu-id="6e2c6-134">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> </dl>

 

 




