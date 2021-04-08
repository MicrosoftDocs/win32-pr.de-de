---
description: MPEG-decodervorverarbeitungs Transformationen
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: MPEG-decodervorverarbeitungs Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70df51b26ec3fa25d67a03a4e494869a2f25760
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747056"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="4a3dc-103">MPEG-decodervorverarbeitungs Transformationen</span><span class="sxs-lookup"><span data-stu-id="4a3dc-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="4a3dc-104">**Letterbox und Panscan**</span><span class="sxs-lookup"><span data-stu-id="4a3dc-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="4a3dc-105">Das 4X3-Bild kann gebildet werden, indem der obere und untere Rand des Bilds (als Briefkasten Bild bezeichnet) oder ein 4X3-Teil des Bilds (als Panscan-Bild bezeichnet) gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="4a3dc-106">Die Menüs und subbildstreams werden oberhalb des letzten Video Bilds überlagert.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="4a3dc-107">Die Bilder mit dem Buch "16x9" werden in einem 4X3-anamorphen Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="4a3dc-108">Die Streckung des anamorphen 4X3-Seitenverhältnisses 720x480-Quellvideos auf ein 16x9-Seitenverhältnis bildet das ursprüngliche 16x9-aspektbild.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="4a3dc-109">Im folgenden finden Sie eine Beschreibung der ordnungsgemäßen Anzeige der einzelnen Modi und ihrer Highlights:</span><span class="sxs-lookup"><span data-stu-id="4a3dc-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="4a3dc-110">**Breitbild:** Das Quellvideo wurde in den größten 16x9-Bereich des Ausgabe Fensters gestreckt.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="4a3dc-111">Die Highlights sind relativ zum Inneren des Bereichs 16x9.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="4a3dc-112">Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 16x9-Bereich beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="4a3dc-113">**Pan-Scan:** Verwenden Sie aus dem 16x9-Video den horizontalen Offset, der im MPEG2-Stream bereitgestellt wird, um ein 4X3-Unterfenster zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="4a3dc-114">Platzieren Sie das 4X3-Unterfenster in den größten 4X3-Bereich des Ausgabe Client Fensters.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="4a3dc-115">Die Koordinaten der Hervorhebung sind relativ zum 4X3-Ausgabefenster und verfügen nicht über eine Beziehung zum 16x9-Quellvideo.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="4a3dc-116">Schwarze Balken sollten entweder am oberen und unteren Rand oder auf der Seite hinzugefügt werden, um einen Bereich von 4 x 3 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="4a3dc-117">**Letterbox:** Berechnen Sie den größten 4X3-Bereich des Ausgabe Fensters.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="4a3dc-118">Schwarze Balken sollten entweder am oberen und unteren Rand oder auf der Seite hinzugefügt werden, um einen Bereich von 4 x 3 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="4a3dc-119">Das Video mit der Quelle "anamorph 4X3" (das ein 16x9-Bild darstellt) wird in dem größten 16x9-Unterfenster innerhalb des 4X3-Bereichs platziert.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="4a3dc-120">Schwarze Balken sollten am oberen und unteren Rand des unter Fensters eingefügt werden, um einen Bereich von 16x9 beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="4a3dc-121">Die Koordinaten der Hervorhebung sind relativ zum 4X3-Bereich und verfügen nicht über eine Beziehung zu dem 16x9-Quellvideo.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="4a3dc-122">Ein Datenträger kann eine Hervorhebung angeben, die sich außerhalb des Bereichs 16x9 befindet (aber noch im Fenster 4X3).</span><span class="sxs-lookup"><span data-stu-id="4a3dc-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="4a3dc-123">Bei 4X3-Videos wird das Video in den größten 4X3-Ausgabebereich des Ausgabe Client Fensters eingefügt.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="4a3dc-124">Schwarze Balken sollten entweder am oberen und unteren Rand oder auf der Seite hinzugefügt werden, um einen Bereich von 4 x 3 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="4a3dc-125">**MPEG-Vorverarbeitung mit dem DVD-Navigator und VMR**</span><span class="sxs-lookup"><span data-stu-id="4a3dc-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="4a3dc-126">Derzeit wird dem Decoder ein Format- \_ \_ Video Medientyp vom Typ "MPEG2" (dessen Format Block auf eine [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur zeigt) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="4a3dc-127">Auf den Ausgabe Pins erzeugt der Decoder den \_ Medientyp Format VideoInfo2, dessen Format Block auf eine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur zeigt.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="4a3dc-128">Das **dwReserved** -Feld der Struktur wurde in **dwcontrols** -Flags umbenannt.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="4a3dc-129">Der **dwcontrolflags** -Member enthält jetzt die neuen Bits.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-129">The **dwControlFlags** member will now contain the new bits.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="4a3dc-130">verwendete amcontrol \_</span><span class="sxs-lookup"><span data-stu-id="4a3dc-130">AMCONTROL\_USED</span></span>          | <span data-ttu-id="4a3dc-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4a3dc-131">0x00000001</span></span> |
| <span data-ttu-id="4a3dc-132">Amcontrol- \_ Pad \_ bis \_ 4X3</span><span class="sxs-lookup"><span data-stu-id="4a3dc-132">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="4a3dc-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4a3dc-133">0x00000002</span></span> |
| <span data-ttu-id="4a3dc-134">Amcontrol- \_ Pad \_ bis \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="4a3dc-134">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="4a3dc-135">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4a3dc-135">0x00000004</span></span> |



 

<span data-ttu-id="4a3dc-136">Mithilfe von amcontrol \_ wird getestet, ob diese neuen Flags unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-136">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="4a3dc-137">Ein Quell Filter sollte das verwendete amcontrol \_ -Flag festlegen und prüfen, ob queryaccept (MediaType) auf dem Downstream-Pin erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-137">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="4a3dc-138">Wenn Sie abgelehnt wird, können die amcontrol-Flags nicht verwendet werden, und dwReserved1 muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-138">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="4a3dc-139">Amcontrol \_ Pad \_ zu \_ 4X3 gibt an, dass das Bild in einem Bereich von 4 x 3 aufgefüllt und angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-139">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="4a3dc-140">\_Der amcontrol \_ -Pad bis \_ 16x9 gibt an, dass das Bild in einem 16x9-Bereich aufgefüllt und angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-140">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="4a3dc-141">Der Decoder sollte die Bits entweder Blind kopieren oder verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-141">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="4a3dc-142">Wenn der Decoder das Letterbox selbst ausführt, muss er das Pixel Seitenverhältnis ändern, das Bild auffüllen und die entsprechenden amcontrol- \_ \* Bits entfernen.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-142">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="4a3dc-143">MPEG2VIDEOINFO. dwFlags enthält jetzt drei Flags, mit denen gesteuert werden kann, wie der Inhalt angezeigt werden soll:</span><span class="sxs-lookup"><span data-stu-id="4a3dc-143">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="4a3dc-144">`AMMPEG2_DoPanScan (0x00000001)`: Wenn dieses Flag festgelegt ist, sollte der MPEG-2-Video Decoder das Ausgabe Bild auf der Grundlage von Pan-Scan-Vektoren in der Bild \_ Anzeige Erweiterung Zuschneiden \_ und das Bildseiten Verhältnis in 4 x 3 ändern.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-144">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="4a3dc-145">Der VMR sollte kein 16x9-Beispiel mit diesem Flag erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-145">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="4a3dc-146">Eine einfache Implementierung kann das Quell Rechteck ändern, um einen 540-weiten Quellbereich mit einem linken Rand anzugeben, der gleich dem Anzeige Offset in der Bild \_ Anzeige \_ Erweiterung ist.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-146">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="4a3dc-147">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: Wenn ein Hardware Decoder diesen Stream einer Videoausgabe anzeigt (in der Regel ein SVideo-Connector auf der Karte), sollte er die Regeln zum Anzeigen eines 16x9-Beispiels in einer 4X3-Anzeige anwenden.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-147">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="4a3dc-148">Ein Software Decoder (oder ein Hardware Decoder, der die an die VMR gesendete Ausgabe erzeugt) verfügt bei der Verarbeitung von Images über zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="4a3dc-148">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="4a3dc-149">Ignorieren Sie dieses Flag, und übergeben Sie den VideoInfoHeader2-Inhalt an die VMR (das Flag "amcontrol \_ Pad \_ to \_ 4X3" wird bereits vom [DVD-Navigator](dvd-navigator-filter.md) im Beispiel festgelegt).</span><span class="sxs-lookup"><span data-stu-id="4a3dc-149">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="4a3dc-150">Die VMR findet ein 16x9-Video Beispiel, bei dem der amcontrol \_ \_ -Pad für das \_ 4X3-Flag und ein 4X3-teilbildstream festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-150">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="4a3dc-151">Die Anwendung muss die normalisierten Ausgabeziel Rechtecke der beiden Streams auf die gleiche Breite festlegen.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-151">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="4a3dc-152">Konvertieren Sie den anamorphen Datenstrom in ein 4X3-Bild, indem Sie den oberen und unteren Rand des Bilds auffüllen und das Bildseiten Verhältnis auf 4X3 festlegen (siehe Letterbox oben), und entfernen Sie das amcontrol- \_ Pad \_ \_ aus VIDEOINFOHEADER2.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-152">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="4a3dc-153">Directxva-decoderer, die die Video-und subbildstreams mischen, müssen dieses Flag verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-153">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="4a3dc-154">Wenn das gemischte subbild von der Hardware nicht skaliert werden kann, sollte der Decoder einen separaten teilbildstream für VMR für die Mischung mit dem Video entwickeln.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-154">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="4a3dc-155">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: Wenn ein Hardware Decoder diesen Stream einer Videoausgabe anzeigt (in der Regel ein SVideo-Connector auf der Karte), sollte er eine 16x9-Anzeige (anamorph) annehmen.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-155">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="4a3dc-156">Ein Software Decoder (oder ein Hardware Decoder, der die an die VMR gesendete Ausgabe erzeugt) verfügt bei der Verarbeitung eines anamorphen Bilds über zwei Optionen:</span><span class="sxs-lookup"><span data-stu-id="4a3dc-156">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="4a3dc-157">Ignorieren Sie dieses Flag, und kopieren Sie den Inhalt von VideoInfoHeader2 in den VMR.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-157">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="4a3dc-158">VMR füllt 4X3-Images auf 16x9 aus, wenn der amcontrol- \_ Pad \_ auf \_ 16x9 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-158">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="4a3dc-159">Auffüllen Sie das Ausgabe Bild in ein 16x9-Bild, und entfernen Sie das amcontrol- \_ Pad \_ auf \_ 16x9-Bit.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-159">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="4a3dc-160">Die meisten Decoder sollten **getmediatype** verwenden, um eine Medien Änderung an der Eingabe-PIN zu erkennen und den **VIDEOINFOHEADER2** -Inhalt (enthalten im **MPEG2INFOHEADER**) in die Ausgabepin zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-160">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="4a3dc-161">Sie verarbeiten wahrscheinlich nur das Panscan-Bit.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-161">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="4a3dc-162">Der folgende Beispielcode zeigt, wie der **VIDEOINFOHEADER2** -Inhalt aus einer Eingabe-PIN in eine Ausgabepin kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="4a3dc-162">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



