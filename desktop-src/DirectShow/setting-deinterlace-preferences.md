---
description: Einstellungen für deinterlace werden festgelegt
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Einstellungen für deinterlace werden festgelegt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745408"
---
# <a name="setting-deinterlace-preferences"></a><span data-ttu-id="e7cce-103">Einstellungen für deinterlace werden festgelegt</span><span class="sxs-lookup"><span data-stu-id="e7cce-103">Setting Deinterlace Preferences</span></span>

<span data-ttu-id="e7cce-104">Der Video Mischungs-Renderer (VMR) unterstützt die hardwarebeschleunigte Deinterlacing, wodurch die renderingqualität für Zeilen Sprung Video verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="e7cce-104">The Video Mixing Renderer (VMR) supports hardware-accelerated deinterlacing, which improves rendering quality for interlaced video.</span></span> <span data-ttu-id="e7cce-105">Welche Features genau verfügbar sind, hängt von der zugrunde liegenden Hardware ab.</span><span class="sxs-lookup"><span data-stu-id="e7cce-105">The exact features that are available depend on the underlying hardware.</span></span> <span data-ttu-id="e7cce-106">Die Anwendung kann die Deinterlacing-Hardwarefunktionen Abfragen und deinterlacingeinstellungen über die [**ivmrdeinterlacecontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) -Schnittstelle (VMR-7) oder die [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) -Schnittstelle (VMR-9) festlegen.</span><span class="sxs-lookup"><span data-stu-id="e7cce-106">The application can query for the hardware deinterlacing capabilities and set deinterlacing preferences through the [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) interface (VMR-7) or [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) interface (VMR-9).</span></span> <span data-ttu-id="e7cce-107">Deinterlacing wird pro Stream ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7cce-107">Deinterlacing is performed on a per-stream basis.</span></span>

<span data-ttu-id="e7cce-108">Es gibt einen wichtigen Unterschied beim interlacingverhalten zwischen VMR-7 und VMR-9.</span><span class="sxs-lookup"><span data-stu-id="e7cce-108">There is one important difference in interlacing behavior between the VMR-7 and the VMR-9.</span></span> <span data-ttu-id="e7cce-109">Auf Systemen, auf denen die Grafikhardware erweiterte Deinterlacing nicht unterstützt, kann VMR-7 auf die Hardware Überlagerung zurückgreifen und Sie anweisen, eine Bob-Formatvorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7cce-109">On systems where the graphics hardware doesn't support advanced deinterlacing, the VMR-7 can fall back to the hardware overlay and instruct it to use a BOB style deinterlace.</span></span> <span data-ttu-id="e7cce-110">In diesem Fall wird das Video tatsächlich bei 60 kippt pro Sekunde gerendert, obwohl der VMR 30 fps meldet.</span><span class="sxs-lookup"><span data-stu-id="e7cce-110">In this case, although the VMR is reporting 30fps the video is actually being rendered at 60 flips per second.</span></span>

<span data-ttu-id="e7cce-111">Außer im Fall von VMR-7 mit Hardware Überlagerung wird Deinterlacing vom Mixer von VMR ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7cce-111">Except in the case of the VMR-7 using hardware overlay, deinterlacing is performed by the VMR's mixer.</span></span> <span data-ttu-id="e7cce-112">Der Mixer verwendet die DXVA (DirectX Video Acceleration) Deinterlacing-Gerätetreiber Schnittstelle (DDI), um die Deinterlacing-Datei auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e7cce-112">The mixer uses the DirectX Video Acceleration (DXVA) deinterlacing device driver interface (DDI) to perform the deinterlacing.</span></span> <span data-ttu-id="e7cce-113">Dieser DDI kann von Anwendungen nicht aufgerufen werden, und Anwendungen können die Deinterlacing-Funktionalität von VMR nicht ersetzen.</span><span class="sxs-lookup"><span data-stu-id="e7cce-113">This DDI is not callable by applications, and applications cannot replace the VMR's deinterlacing functionality.</span></span> <span data-ttu-id="e7cce-114">Allerdings kann eine Anwendung den gewünschten Deinterlacing-Modus auswählen, wie in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e7cce-114">However, an application can select the desired deinterlacing mode, as described in this section.</span></span>

> [!Note]  
> <span data-ttu-id="e7cce-115">In diesem Abschnitt werden die **IVMRDeinterlaceControl9** -Methoden beschrieben, die Versionen von VMR-7 sind jedoch nahezu identisch.</span><span class="sxs-lookup"><span data-stu-id="e7cce-115">This section describes the **IVMRDeinterlaceControl9** methods, but the VMR-7 versions are almost identical.</span></span>

 

<span data-ttu-id="e7cce-116">Gehen Sie folgendermaßen vor, um die Deinterlacing-Funktionen für einen Videostream zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e7cce-116">To get the deinterlacing capabilities for a video stream, do the following:</span></span>

1.  <span data-ttu-id="e7cce-117">Füllen Sie eine [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) -Struktur mit einer Beschreibung des Videodaten Stroms aus.</span><span class="sxs-lookup"><span data-stu-id="e7cce-117">Fill in a [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) structure with a description of the video stream.</span></span> <span data-ttu-id="e7cce-118">Details zum Ausfüllen dieser Struktur werden später angegeben.</span><span class="sxs-lookup"><span data-stu-id="e7cce-118">Details of how to fill in this structure are given later.</span></span>
2.  <span data-ttu-id="e7cce-119">Übergeben Sie die Struktur an die [**IVMRDeinterlaceControl9:: getnumofdeinterlacemodes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e7cce-119">Pass the structure to the [**IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) method.</span></span> <span data-ttu-id="e7cce-120">Ruft die-Methode zweimal auf.</span><span class="sxs-lookup"><span data-stu-id="e7cce-120">Call the method twice.</span></span> <span data-ttu-id="e7cce-121">Der erste-Befehl gibt die Anzahl der Deinterlacing-Modi zurück, die von der Hardware für das angegebene Format unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e7cce-121">The first call returns the number of deinterlace modes the hardware supports for the specified format.</span></span> <span data-ttu-id="e7cce-122">Weisen Sie ein Array von GUIDs dieser Größe zu, und wenden Sie die-Methode erneut an, und übergeben Sie dabei die Adresse des-Arrays.</span><span class="sxs-lookup"><span data-stu-id="e7cce-122">Allocate an array of GUIDs of this size, and call the method again, passing in the address of the array.</span></span> <span data-ttu-id="e7cce-123">Der zweite-Befehl füllt das Array mit GUIDs.</span><span class="sxs-lookup"><span data-stu-id="e7cce-123">The second call fills the array with GUIDs.</span></span> <span data-ttu-id="e7cce-124">Jeder GUID identifiziert einen deinterlacingmodus.</span><span class="sxs-lookup"><span data-stu-id="e7cce-124">Each GUID identifies one deinterlacing mode.</span></span>
3.  <span data-ttu-id="e7cce-125">Um die Untertitel eines bestimmten Modus abzurufen, müssen Sie die [**IVMRDeinterlaceControl9:: getdeinterlacemodecaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7cce-125">To get the capabiltiies of a particular mode, call the [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) method.</span></span> <span data-ttu-id="e7cce-126">Übergeben Sie dieselbe **VMR9VideoDesc** -Struktur zusammen mit einer der GUIDs aus dem Array.</span><span class="sxs-lookup"><span data-stu-id="e7cce-126">Pass in the same **VMR9VideoDesc** structure, along with one of the GUIDs from the array.</span></span> <span data-ttu-id="e7cce-127">Die-Methode füllt eine [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) -Struktur mit den Funktionen des-Modus.</span><span class="sxs-lookup"><span data-stu-id="e7cce-127">The method fills a [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) structure with the mode capabilities.</span></span>

<span data-ttu-id="e7cce-128">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="e7cce-128">The following code shows these steps:</span></span>


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



<span data-ttu-id="e7cce-129">Nun kann die Anwendung den Deinterlacing-Modus für den Stream mit den folgenden Methoden festlegen:</span><span class="sxs-lookup"><span data-stu-id="e7cce-129">Now the application can set the deinterlacing mode for the stream, using the following methods:</span></span>

-   <span data-ttu-id="e7cce-130">Die [**setdeinterlacemode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) -Methode legt den bevorzugten Modus fest.</span><span class="sxs-lookup"><span data-stu-id="e7cce-130">The [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) method sets the preferred mode.</span></span> <span data-ttu-id="e7cce-131">Verwenden \_ Sie die GUID NULL, um Deinterlacing zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e7cce-131">Use GUID\_NULL to turn off deinterlacing.</span></span>
-   <span data-ttu-id="e7cce-132">Die [**setdeinterlaceprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) -Methode gibt das Verhalten an, wenn der angeforderte Modus nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e7cce-132">The [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) method specifies the behavior if the requested mode is not available.</span></span>
-   <span data-ttu-id="e7cce-133">Die [**getdeinterlacemode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) -Methode gibt den von Ihnen festgelegten bevorzugten Modus zurück.</span><span class="sxs-lookup"><span data-stu-id="e7cce-133">The [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) method returns the preferred mode that you set.</span></span>
-   <span data-ttu-id="e7cce-134">Die [**getactualdeinterlacemode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) -Methode gibt den tatsächlich verwendeten Modus zurück, bei dem es sich um einen Fall Back Modus handeln kann, wenn der bevorzugte Modus nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e7cce-134">The [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) method returns the actual mode in use, which might be a fallback mode, if the preferred mode is not available.</span></span>

<span data-ttu-id="e7cce-135">Weitere Informationen finden Sie auf den Referenzseiten der Methode.</span><span class="sxs-lookup"><span data-stu-id="e7cce-135">The method reference pages give more information.</span></span>

<span data-ttu-id="e7cce-136">**Verwenden der VMR9VideoDesc-Struktur**</span><span class="sxs-lookup"><span data-stu-id="e7cce-136">**Using the VMR9VideoDesc Structure**</span></span>

<span data-ttu-id="e7cce-137">Im zuvor beschriebenen Verfahren besteht der erste Schritt darin, eine **VMR9VideoDesc** -Struktur mit einer Beschreibung des Videodaten Stroms auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="e7cce-137">In the procedure given previously, the first step is to fill in a **VMR9VideoDesc** structure with a description of the video stream.</span></span> <span data-ttu-id="e7cce-138">Beginnen Sie, indem Sie den Medientyp des Videodaten Stroms erhalten.</span><span class="sxs-lookup"><span data-stu-id="e7cce-138">Start by getting the media type of the video stream.</span></span> <span data-ttu-id="e7cce-139">Hierzu können Sie [**IPin:: connectionmediatype**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) in der Eingabe-PIN des VMR-Filters aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7cce-139">You can do this by calling [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) on the VMR filter's input pin.</span></span> <span data-ttu-id="e7cce-140">Überprüfen Sie dann, ob der Videostream Zeilen Sprung ist.</span><span class="sxs-lookup"><span data-stu-id="e7cce-140">Then confirm whether the video stream is interlaced.</span></span> <span data-ttu-id="e7cce-141">Nur [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Formate können mit Zeilen Sprung verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="e7cce-141">Only [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats can be interlaced.</span></span> <span data-ttu-id="e7cce-142">Wenn der Formatierungstyp Format \_ videoinfo ist, muss es sich um einen progressiven Frame handeln.</span><span class="sxs-lookup"><span data-stu-id="e7cce-142">If the format type is FORMAT\_VideoInfo, it must be a progressive frame.</span></span> <span data-ttu-id="e7cce-143">Wenn der Formattyp Format \_ VideoInfo2 ist, überprüfen Sie das Feld **dwinterlaceflags** für das aminterlace- \_ Flag isinterlacing.</span><span class="sxs-lookup"><span data-stu-id="e7cce-143">If the format type is FORMAT\_VideoInfo2, check the **dwInterlaceFlags** field for the AMINTERLACE\_IsInterlaced flag.</span></span> <span data-ttu-id="e7cce-144">Das vorhanden sein dieses Flags gibt an, dass das Video mit Zeilen Sprung versehen ist.</span><span class="sxs-lookup"><span data-stu-id="e7cce-144">The presence of this flag indicates the video is interlaced.</span></span>

<span data-ttu-id="e7cce-145">Angenommen, die Variable **pbmi** ist ein Zeiger auf die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur im Format Block.</span><span class="sxs-lookup"><span data-stu-id="e7cce-145">Assume that the variable **pBMI** is a pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the format block.</span></span> <span data-ttu-id="e7cce-146">Legen Sie die folgenden Werte in der **VMR9VideoDesc** -Struktur fest:</span><span class="sxs-lookup"><span data-stu-id="e7cce-146">Set the following values in the **VMR9VideoDesc** structure:</span></span>

-   <span data-ttu-id="e7cce-147">**dwSize**: Legen Sie dieses Feld auf fest `sizeof(VMR9VideoDesc)` .</span><span class="sxs-lookup"><span data-stu-id="e7cce-147">**dwSize**: Set this field to `sizeof(VMR9VideoDesc)`.</span></span>
-   <span data-ttu-id="e7cce-148">**dwsamplewidth**: Legen Sie dieses Feld auf fest `pBMI->biWidth` .</span><span class="sxs-lookup"><span data-stu-id="e7cce-148">**dwSampleWidth**: Set this field to `pBMI->biWidth`.</span></span>
-   <span data-ttu-id="e7cce-149">**dwsampleheight**: Legen Sie dieses Feld auf fest `abs(pBMI->biHeight)` .</span><span class="sxs-lookup"><span data-stu-id="e7cce-149">**dwSampleHeight**: Set this field to `abs(pBMI->biHeight)`.</span></span>
-   <span data-ttu-id="e7cce-150">**Sample Format**: Dieses Feld beschreibt die damit-Eigenschaften des Medientyps.</span><span class="sxs-lookup"><span data-stu-id="e7cce-150">**SampleFormat**: This field describes the interlace characteristics of the media type.</span></span> <span data-ttu-id="e7cce-151">Überprüfen Sie das Feld **dwinterlaceflags** in der **VIDEOINFOHEADER2** -Struktur, und legen Sie **Sampleformat** auf das entsprechende [**VMR9 \_ Sampleformat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) -Flag fest.</span><span class="sxs-lookup"><span data-stu-id="e7cce-151">Check the **dwInterlaceFlags** field in the **VIDEOINFOHEADER2** structure, and set **SampleFormat** equal to the equivalent [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) flag.</span></span> <span data-ttu-id="e7cce-152">Eine Hilfsfunktion hierfür finden Sie unten.</span><span class="sxs-lookup"><span data-stu-id="e7cce-152">A helper function to do this is given below.</span></span>
-   <span data-ttu-id="e7cce-153">**Inputsamplefreq**: Dieses Feld gibt die Eingabe Häufigkeit an, die aus dem **avgtimeperframe** -Feld in der **VIDEOINFOHEADER2** -Struktur berechnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e7cce-153">**InputSampleFreq**: This field gives the input frequency, which can be calculated from the **AvgTimePerFrame** field in the **VIDEOINFOHEADER2** structure.</span></span> <span data-ttu-id="e7cce-154">Legen Sie im allgemeinen Fall **dwzähler** auf 10 Millionen fest, und legen Sie für **dwnenner** den Wert **avgtimeperframe** fest.</span><span class="sxs-lookup"><span data-stu-id="e7cce-154">In the general case, set **dwNumerator** to 10000000, and set **dwDenominator** to **AvgTimePerFrame**.</span></span> <span data-ttu-id="e7cce-155">Sie können jedoch auch nach einigen bekannten Frameraten suchen:</span><span class="sxs-lookup"><span data-stu-id="e7cce-155">However, you can also check for some well-known frame rates:</span></span>

    | <span data-ttu-id="e7cce-156">Durchschnittliche Zeit pro Frame</span><span class="sxs-lookup"><span data-stu-id="e7cce-156">Average time per frame</span></span> | <span data-ttu-id="e7cce-157">Frame Rate (fps)</span><span class="sxs-lookup"><span data-stu-id="e7cce-157">Frame rate (fps)</span></span> | <span data-ttu-id="e7cce-158">Zähler</span><span class="sxs-lookup"><span data-stu-id="e7cce-158">Numerator</span></span> | <span data-ttu-id="e7cce-159">Vorzuschlagen</span><span class="sxs-lookup"><span data-stu-id="e7cce-159">Denominator</span></span> |
    |------------------------|------------------|-----------|-------------|
    | <span data-ttu-id="e7cce-160">166833</span><span class="sxs-lookup"><span data-stu-id="e7cce-160">166833</span></span>                 | <span data-ttu-id="e7cce-161">59,94 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="e7cce-161">59.94 (NTSC)</span></span>     | <span data-ttu-id="e7cce-162">60000</span><span class="sxs-lookup"><span data-stu-id="e7cce-162">60000</span></span>     | <span data-ttu-id="e7cce-163">1001</span><span class="sxs-lookup"><span data-stu-id="e7cce-163">1001</span></span>        |
    | <span data-ttu-id="e7cce-164">333667</span><span class="sxs-lookup"><span data-stu-id="e7cce-164">333667</span></span>                 | <span data-ttu-id="e7cce-165">29,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="e7cce-165">29.97 (NTSC)</span></span>     | <span data-ttu-id="e7cce-166">30.000</span><span class="sxs-lookup"><span data-stu-id="e7cce-166">30000</span></span>     | <span data-ttu-id="e7cce-167">1001</span><span class="sxs-lookup"><span data-stu-id="e7cce-167">1001</span></span>        |
    | <span data-ttu-id="e7cce-168">417188</span><span class="sxs-lookup"><span data-stu-id="e7cce-168">417188</span></span>                 | <span data-ttu-id="e7cce-169">23,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="e7cce-169">23.97 (NTSC)</span></span>     | <span data-ttu-id="e7cce-170">24.000</span><span class="sxs-lookup"><span data-stu-id="e7cce-170">24000</span></span>     | <span data-ttu-id="e7cce-171">1001</span><span class="sxs-lookup"><span data-stu-id="e7cce-171">1001</span></span>        |
    | <span data-ttu-id="e7cce-172">200.000</span><span class="sxs-lookup"><span data-stu-id="e7cce-172">200000</span></span>                 | <span data-ttu-id="e7cce-173">50,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="e7cce-173">50.00 (PAL)</span></span>      | <span data-ttu-id="e7cce-174">50</span><span class="sxs-lookup"><span data-stu-id="e7cce-174">50</span></span>        | <span data-ttu-id="e7cce-175">1</span><span class="sxs-lookup"><span data-stu-id="e7cce-175">1</span></span>           |
    | <span data-ttu-id="e7cce-176">400000</span><span class="sxs-lookup"><span data-stu-id="e7cce-176">400000</span></span>                 | <span data-ttu-id="e7cce-177">25,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="e7cce-177">25.00 (PAL)</span></span>      | <span data-ttu-id="e7cce-178">25</span><span class="sxs-lookup"><span data-stu-id="e7cce-178">25</span></span>        | <span data-ttu-id="e7cce-179">1</span><span class="sxs-lookup"><span data-stu-id="e7cce-179">1</span></span>           |
    | <span data-ttu-id="e7cce-180">416667</span><span class="sxs-lookup"><span data-stu-id="e7cce-180">416667</span></span>                 | <span data-ttu-id="e7cce-181">24,00 (Film)</span><span class="sxs-lookup"><span data-stu-id="e7cce-181">24.00 (Film)</span></span>     | <span data-ttu-id="e7cce-182">24</span><span class="sxs-lookup"><span data-stu-id="e7cce-182">24</span></span>        | <span data-ttu-id="e7cce-183">1</span><span class="sxs-lookup"><span data-stu-id="e7cce-183">1</span></span>           |

    

     

-   <span data-ttu-id="e7cce-184">**Outputframefreq**: Dieses Feld gibt die Ausgabe Häufigkeit an, die anhand des **inputsamplefreq** -Werts und der überlappenden Merkmale des Eingabedaten Stroms berechnet werden kann:</span><span class="sxs-lookup"><span data-stu-id="e7cce-184">**OutputFrameFreq**: This field gives the output frequency, which can be calculated from the **InputSampleFreq** value and the interleaving characteristics of the input stream:</span></span>
    -   <span data-ttu-id="e7cce-185">Legen Sie **outputframefreq. dwnenner** auf **inputsamplefreq. dwnenner** fest.</span><span class="sxs-lookup"><span data-stu-id="e7cce-185">Set **OutputFrameFreq.dwDenominator** equal to **InputSampleFreq.dwDenominator**.</span></span>
    -   <span data-ttu-id="e7cce-186">Wenn das Eingabe Video verschachtelt ist, legen Sie **outputframefreq. dwnumerator** auf 2 x **inputsamplefreq. dwnumerator** fest.</span><span class="sxs-lookup"><span data-stu-id="e7cce-186">If the input video is interleaved, set **OutputFrameFreq.dwNumerator** to 2 x **InputSampleFreq.dwNumerator**.</span></span> <span data-ttu-id="e7cce-187">(Nach Deinterlacing wird die Framerate verdoppelt.) Legen Sie andernfalls den Wert auf **inputsamplefreq. dwnumerator** fest.</span><span class="sxs-lookup"><span data-stu-id="e7cce-187">(After deinterlacing, the frame rate is doubled.) Otherwise, set the value to **InputSampleFreq.dwNumerator**.</span></span>
-   <span data-ttu-id="e7cce-188">**dwfourcc**: Legen Sie dieses Feld auf fest `pBMI->biCompression` .</span><span class="sxs-lookup"><span data-stu-id="e7cce-188">**dwFourCC**: Set this field to `pBMI->biCompression`.</span></span>

<span data-ttu-id="e7cce-189">Die folgende Hilfsfunktion konvertiert aminterlace \_ *X* -Flags in [**VMR9 \_ Sampleformat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) -Werte:</span><span class="sxs-lookup"><span data-stu-id="e7cce-189">The following helper function converts AMINTERLACE\_*X* flags to [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) values:</span></span>


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



