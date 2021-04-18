---
description: Tragbare Windows-Geräte unterstützen die folgenden Videoeigenschaften.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Video Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358015"
---
# <a name="video-properties"></a><span data-ttu-id="24a21-103">Video Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24a21-103">Video Properties</span></span>

<span data-ttu-id="24a21-104">Tragbare Windows-Geräte unterstützen die folgenden Videoeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="24a21-104">Windows Portable Devices supports the following video properties.</span></span>



| <span data-ttu-id="24a21-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24a21-105">Property</span></span>                                         | <span data-ttu-id="24a21-106">VarType</span><span class="sxs-lookup"><span data-stu-id="24a21-106">VarType</span></span>        | <span data-ttu-id="24a21-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="24a21-107">Description</span></span>                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a21-108">**WPD- \_ Video \_ Autor**</span><span class="sxs-lookup"><span data-stu-id="24a21-108">**WPD\_VIDEO\_AUTHOR**</span></span>                           | <span data-ttu-id="24a21-109">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="24a21-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="24a21-110">Der Autor der Videodatei.</span><span class="sxs-lookup"><span data-stu-id="24a21-110">The author of the video file.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="24a21-111">**WPD- \_ Video \_ Bitrate**</span><span class="sxs-lookup"><span data-stu-id="24a21-111">**WPD\_VIDEO\_BITRATE**</span></span>                          | <span data-ttu-id="24a21-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="24a21-112">**VT\_UI4**</span></span>    | <span data-ttu-id="24a21-113">Die Bitrate der Videodatei.</span><span class="sxs-lookup"><span data-stu-id="24a21-113">The bit rate of the video file.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="24a21-114">**WPD- \_ Video \_ Puffer \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="24a21-114">**WPD\_VIDEO\_BUFFER\_SIZE**</span></span>                     | <span data-ttu-id="24a21-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="24a21-115">**VT\_UI4**</span></span>    | <span data-ttu-id="24a21-116">Ein-Wert, der die erforderliche Video Puffergröße zum Rendering dieser Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="24a21-116">A value that specifies the required video buffer size to render this file.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="24a21-117">**WPD- \_ Video \_ Gutschriften**</span><span class="sxs-lookup"><span data-stu-id="24a21-117">**WPD\_VIDEO\_CREDITS**</span></span>                          | <span data-ttu-id="24a21-118">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="24a21-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="24a21-119">Das Guthaben, das die Umwandlung und die Gruppe für das Video auflistet.</span><span class="sxs-lookup"><span data-stu-id="24a21-119">The credits listing the cast and crew for the video.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="24a21-120">**WPD- \_ Video- \_ FourCC- \_ Code**</span><span class="sxs-lookup"><span data-stu-id="24a21-120">**WPD\_VIDEO\_FOURCC\_CODE**</span></span>                     | <span data-ttu-id="24a21-121">**VT \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="24a21-121">**VT\_DWORD**</span></span>  | <span data-ttu-id="24a21-122">Der registrierte FourCC-Code, der den Codec angibt, der für die Videodatei verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="24a21-122">The registered FourCC code that indicates the codec that was used for the video file.</span></span> <span data-ttu-id="24a21-123">Eine Auflistung von FourCC-Formaten finden Sie im Artikel [registrierte FOURCC Codes und Wave Formats](https://msdn2.microsoft.com/library/ms867195.aspx) auf der MSDN-Website.</span><span class="sxs-lookup"><span data-stu-id="24a21-123">For a listing of FourCC formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |
| <span data-ttu-id="24a21-124">**WPD- \_ Video \_ Framerate**</span><span class="sxs-lookup"><span data-stu-id="24a21-124">**WPD\_VIDEO\_FRAMERATE**</span></span>                        | <span data-ttu-id="24a21-125">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="24a21-125">**VT\_UI4**</span></span>    | <span data-ttu-id="24a21-126">Die Frame Rate der Videodatei in Frames/Sekunde x 1.000.</span><span class="sxs-lookup"><span data-stu-id="24a21-126">The frame rate of the video file, in frames/second x 1,000.</span></span> <span data-ttu-id="24a21-127">Beispielsweise wird eine Frame Rate von 29,97 als 29970 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="24a21-127">For example, a frame rate of 29.97 is represented as 29970.</span></span>                                                                                                                                 |
| <span data-ttu-id="24a21-128">**WPD- \_ Video \_ Genre**</span><span class="sxs-lookup"><span data-stu-id="24a21-128">**WPD\_VIDEO\_GENRE**</span></span>                            | <span data-ttu-id="24a21-129">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="24a21-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="24a21-130">Das Genre dieser Videodatei.</span><span class="sxs-lookup"><span data-stu-id="24a21-130">The genre of this video file.</span></span> <span data-ttu-id="24a21-131">Es sind keine Standard Genre Definitionen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="24a21-131">There are no standard genre definitions.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="24a21-132">**WPD \_ - \_ Video \_ schlüsselframe- \_ Abstand**</span><span class="sxs-lookup"><span data-stu-id="24a21-132">**WPD\_VIDEO\_KEY\_FRAME\_DISTANCE**</span></span>             | <span data-ttu-id="24a21-133">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="24a21-133">**VT\_UI4**</span></span>    | <span data-ttu-id="24a21-134">Das Intervall zwischen Keyframes in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="24a21-134">The interval between key frames, in milliseconds.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="24a21-135">**WPD- \_ Video \_ Qualitäts \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="24a21-135">**WPD\_VIDEO\_QUALITY\_SETTING**</span></span>                 | <span data-ttu-id="24a21-136">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="24a21-136">**VT\_UI4**</span></span>    | <span data-ttu-id="24a21-137">Die Qualitätseinstellung für die Videodatei.</span><span class="sxs-lookup"><span data-stu-id="24a21-137">The quality setting for the video file.</span></span> <span data-ttu-id="24a21-138">Dies ist Codec-abhängig.</span><span class="sxs-lookup"><span data-stu-id="24a21-138">This is codec-dependent.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="24a21-139">**WPD-Video recorddebug- \_ \_ \_ Kanal \_ Nummer**</span><span class="sxs-lookup"><span data-stu-id="24a21-139">**WPD\_VIDEO\_RECORDEDTV\_CHANNEL\_NUMBER**</span></span>      | <span data-ttu-id="24a21-140">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="24a21-140">**VT\_UI4**</span></span>    | <span data-ttu-id="24a21-141">Die Nummer des Fernsehkanals, von dem das Video aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="24a21-141">The television channel number the video was recorded from.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="24a21-142">**WPD-Video recorddebug- \_ \_ \_ Programm \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24a21-142">**WPD\_VIDEO\_RECORDEDTV\_PROGRAM\_DESCRIPTION**</span></span> | <span data-ttu-id="24a21-143">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="24a21-143">**VT\_LPWSTR**</span></span> | <span data-ttu-id="24a21-144">Eine Beschreibung des aufgezeichneten Fernsehprogramms.</span><span class="sxs-lookup"><span data-stu-id="24a21-144">A description of the recorded television program.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="24a21-145">**WPD- \_ Video \_ recordebug \_ Wiederholen**</span><span class="sxs-lookup"><span data-stu-id="24a21-145">**WPD\_VIDEO\_RECORDEDTV\_REPEAT**</span></span>               | <span data-ttu-id="24a21-146">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="24a21-146">**VT\_BOOL**</span></span>   | <span data-ttu-id="24a21-147">Ein boolescher Wert, der angibt, ob das Fernsehprogramm eine Wiederholung anzeigt.</span><span class="sxs-lookup"><span data-stu-id="24a21-147">A Boolean value that specifies whether the television program was a repeat showing.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="24a21-148">**WPD-Video recorddebug- \_ \_ \_ Stations \_ Name**</span><span class="sxs-lookup"><span data-stu-id="24a21-148">**WPD\_VIDEO\_RECORDEDTV\_STATION\_NAME**</span></span>        | <span data-ttu-id="24a21-149">**VT \_ LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="24a21-149">**VT\_LPWSTR**</span></span> | <span data-ttu-id="24a21-150">Die Fernsehstation, von der das Video aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="24a21-150">The television station that the video was recorded from.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="24a21-151">**WPD- \_ Video \_ Überprüfungstyp \_**</span><span class="sxs-lookup"><span data-stu-id="24a21-151">**WPD\_VIDEO\_SCAN\_TYPE**</span></span>                       | <span data-ttu-id="24a21-152">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="24a21-152">**VT\_UI4**</span></span>    | <span data-ttu-id="24a21-153">Ein [**WPD \_ - \_ \_ videoscantypes**](wpd-video-scan-types.md) -Enumerator, der das Zeilen Sprung der Video Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="24a21-153">A [**WPD\_VIDEO\_SCAN\_TYPES**](wpd-video-scan-types.md) enumerator that specifies the interlacing of the video file.</span></span>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="24a21-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24a21-154">Requirements</span></span>



| <span data-ttu-id="24a21-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24a21-155">Requirement</span></span> | <span data-ttu-id="24a21-156">Wert</span><span class="sxs-lookup"><span data-stu-id="24a21-156">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a21-157">Header</span><span class="sxs-lookup"><span data-stu-id="24a21-157">Header</span></span><br/> | <dl> <span data-ttu-id="24a21-158"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a21-158"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24a21-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24a21-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a21-160">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="24a21-160">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




