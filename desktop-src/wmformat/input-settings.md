---
title: Eingabeeinstellungen
description: Eingabeeinstellungen
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media-Format-SDK, globale Konstanten
- Advanced Systems Format (ASF), globale Konstanten
- ASF (Advanced Systems Format), globale Konstanten
- Globale Konstanten, Liste der
- Windows Media-Format-SDK, Konstanten
- Advanced Systems Format (ASF), Konstanten
- ASF (Advanced Systems Format), Konstanten
- Konstanten, Liste der
- Windows Media-Format-SDK, Eingabeeinstellungen
- Advanced Systems Format (ASF), Eingabeeinstellungen
- ASF (Advanced Systems Format), Eingabeeinstellungen
- Eingabeeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038523"
---
# <a name="input-settings"></a><span data-ttu-id="a27ff-115">Eingabeeinstellungen</span><span class="sxs-lookup"><span data-stu-id="a27ff-115">Input Settings</span></span>

<span data-ttu-id="a27ff-116">Die folgenden globalen Konstanten werden verwendet, um Eingabeeinstellungen für den Writer zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a27ff-116">The following global constants are used to identify input settings for the writer.</span></span>



| <span data-ttu-id="a27ff-117">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="a27ff-117">Global constant</span></span>                        | <span data-ttu-id="a27ff-118">WMT \_ attr- \_ DataType</span><span class="sxs-lookup"><span data-stu-id="a27ff-118">WMT\_ATTR\_DATATYPE</span></span>                                                                                                                       | <span data-ttu-id="a27ff-119">Beschreibung von *pValue*</span><span class="sxs-lookup"><span data-stu-id="a27ff-119">Description of *pValue*</span></span>                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a27ff-120">g \_ wszdeinterlacemode</span><span class="sxs-lookup"><span data-stu-id="a27ff-120">g\_wszDeinterlaceMode</span></span>                  | <span data-ttu-id="a27ff-121">**WMT \_ Geben Sie \_ DWORD** auf einen der Werte in der Mode-Tabelle im Thema [zu deinterlace-Video](to-deinterlace-video.md)ein.</span><span class="sxs-lookup"><span data-stu-id="a27ff-121">**WMT\_TYPE\_DWORD** set to one of the values in the mode table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span>            | <span data-ttu-id="a27ff-122">Gibt bei Festlegung den Typ von Zeilen Sprung Inhalt der Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="a27ff-122">When set, specifies the type of interlaced content of the input.</span></span> <span data-ttu-id="a27ff-123">Weitere Informationen finden [Sie unter dem deinterlace-Video](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="a27ff-123">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>                                                                                                                            |
| <span data-ttu-id="a27ff-124">g \_ wszfixedframerate</span><span class="sxs-lookup"><span data-stu-id="a27ff-124">g\_wszFixedFrameRate</span></span>                   | <span data-ttu-id="a27ff-125">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a27ff-125">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="a27ff-126">Wenn der Wert auf true festgelegt ist, wird der Codec angewiesen, während der Codierung keine Frames abzulegen.</span><span class="sxs-lookup"><span data-stu-id="a27ff-126">When set to True, instructs the codec not to drop any frames during encoding.</span></span> <span data-ttu-id="a27ff-127">Dies führt dazu, dass die [*Framerate*](wmformat-glossary.md) des Ausgabevideo Datenstroms konstant ist.</span><span class="sxs-lookup"><span data-stu-id="a27ff-127">This will cause the [*frame rate*](wmformat-glossary.md) of the output video stream to be constant.</span></span> <span data-ttu-id="a27ff-128">Die Framerate des Eingabestreams muss nicht konstant sein.</span><span class="sxs-lookup"><span data-stu-id="a27ff-128">The frame rate of the input stream does not need to be constant.</span></span> |
| <span data-ttu-id="a27ff-129">g \_ wszinitialpatternforinvertartelecine</span><span class="sxs-lookup"><span data-stu-id="a27ff-129">g\_wszInitialPatternForInverseTelecine</span></span> | <span data-ttu-id="a27ff-130">**WMT \_ Geben Sie \_ DWORD** auf einen der Werte in der ursprünglichen Muster Tabelle im Thema [zu deinterlace-Video](to-deinterlace-video.md)ein.</span><span class="sxs-lookup"><span data-stu-id="a27ff-130">**WMT\_TYPE\_DWORD** set to one of the values in the initial pattern table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span> | <span data-ttu-id="a27ff-131">Wenn der Deinterlacing-Modus auf WM \_ DM \_ Deinterlacing \_ inversetelecine festgelegt ist, kann dieser so festgelegt werden, dass er das Muster der [*telecine*](wmformat-glossary.md) -Eingabe angibt.</span><span class="sxs-lookup"><span data-stu-id="a27ff-131">When the deinterlace mode is set to WM\_DM\_DEINTERLACE\_INVERSETELECINE, this can be set to specify the pattern of the [*telecine*](wmformat-glossary.md) input.</span></span> <span data-ttu-id="a27ff-132">Weitere Informationen finden [Sie unter dem deinterlace-Video](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="a27ff-132">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>        |
| <span data-ttu-id="a27ff-133">g \_ wszinterlacedcoding</span><span class="sxs-lookup"><span data-stu-id="a27ff-133">g\_wszInterlacedCoding</span></span>                 | <span data-ttu-id="a27ff-134">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="a27ff-134">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="a27ff-135">Wenn der Wert auf true festgelegt ist, wird angegeben, dass der Codec den Stream als Zeilen Sprung-Inhalt codieren soll.</span><span class="sxs-lookup"><span data-stu-id="a27ff-135">When set to True, specifies that that the codec should encode the stream as interlaced content.</span></span> <span data-ttu-id="a27ff-136">Weitere Informationen finden [Sie unter So verwenden Sie](to-use-interlaced-video.md)ein Zeilen Sprung Video.</span><span class="sxs-lookup"><span data-stu-id="a27ff-136">For more information, see [To Use Interlaced Video](to-use-interlaced-video.md).</span></span>                                                                                       |
| <span data-ttu-id="a27ff-137">g \_ wszjpgcompressionquality</span><span class="sxs-lookup"><span data-stu-id="a27ff-137">g\_wszJPEGCompressionQuality</span></span>           | <span data-ttu-id="a27ff-138">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a27ff-138">**WMT\_TYPE\_DWORD**</span></span>                                                                                                                      | <span data-ttu-id="a27ff-139">Gibt die JPEG-Qualitätsstufe (von 1 bis 100) an, die für die Eingabe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a27ff-139">Specifies the JPEG quality level (from 1 to 100) to be used on the input.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="a27ff-140">g \_ wszwatermarkclsid</span><span class="sxs-lookup"><span data-stu-id="a27ff-140">g\_wszWatermarkCLSID</span></span>                   | <span data-ttu-id="a27ff-141">**WMT- \_ Typ- \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="a27ff-141">**WMT\_TYPE\_GUID**</span></span>                                                                                                                       | <span data-ttu-id="a27ff-142">Der Wert wird auf die Wasserzeichen-GUID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a27ff-142">The value is set to the watermark GUID.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="a27ff-143">g \_ wszwatermarkconfig</span><span class="sxs-lookup"><span data-stu-id="a27ff-143">g\_wszWatermarkConfig</span></span>                  | <span data-ttu-id="a27ff-144">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a27ff-144">**WMT\_TYPE\_STRING**</span></span>                                                                                                                     | <span data-ttu-id="a27ff-145">Der Wert wird auf die Wasserzeichen Konfiguration festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a27ff-145">The value is set to the watermark configuration.</span></span> <span data-ttu-id="a27ff-146">Dieser Wert variiert je nach dem Wasserzeichen DMO.</span><span class="sxs-lookup"><span data-stu-id="a27ff-146">This value will vary depending upon the watermarking DMO.</span></span> <span data-ttu-id="a27ff-147">Weitere Informationen finden Sie in der Dokumentation des Wasserzeichen Systems.</span><span class="sxs-lookup"><span data-stu-id="a27ff-147">Consult the documentation of the watermarking system for more information.</span></span>                                                                                   |



 

> [!Note]  
> <span data-ttu-id="a27ff-148">Die für einen Stream konfigurierten Eingabeeinstellungen werden in der geschriebenen Datei nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a27ff-148">The input settings configured for a stream are not persisted in the written file.</span></span> <span data-ttu-id="a27ff-149">Wenn Sie möchten, dass Ihr benutzerdefinierter Reader Zugriff auf diese Codierungs Parameter hat, müssen Sie benutzerdefinierte Attribute erstellen, um Sie im Dateiheader zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a27ff-149">If you want your custom reader to have access to these encoding parameters, you must create custom attributes to store them in the file header.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a27ff-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a27ff-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a27ff-151">**IWMWriterAdvanced2:: getinputsetting**</span><span class="sxs-lookup"><span data-stu-id="a27ff-151">**IWMWriterAdvanced2::GetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[<span data-ttu-id="a27ff-152">**IWMWriterAdvanced2:: abputsetting**</span><span class="sxs-lookup"><span data-stu-id="a27ff-152">**IWMWriterAdvanced2::SetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




