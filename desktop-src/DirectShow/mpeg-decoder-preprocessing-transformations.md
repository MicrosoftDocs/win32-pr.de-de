---
description: Vorverarbeitungstransformationen für MPEG-Decoder
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Vorverarbeitungstransformationen für MPEG-Decoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908898"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="10cab-103">Vorverarbeitungstransformationen für MPEG-Decoder</span><span class="sxs-lookup"><span data-stu-id="10cab-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="10cab-104">**Letterbox und PanScan**</span><span class="sxs-lookup"><span data-stu-id="10cab-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="10cab-105">Das 4x3-Bild kann entweder durch Aufhängen des oberen und unteren Rands des Bilds (als Letterbox-Bild bezeichnet) oder durch Extrahieren eines 4x3-Teils des Bilds (als PanScan-Bild bezeichnet) gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="10cab-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="10cab-106">Die Menüs und Unterbildstreams werden über dem endgültigen Videobild überlagert.</span><span class="sxs-lookup"><span data-stu-id="10cab-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="10cab-107">Die Bilder mit einem Verhältnis von 16 x 9 werden in einem anamorphen 4x3-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="10cab-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="10cab-108">Das ursprüngliche 16x9-Seitenbild bildet das anamorphe 4x3-Seitenverhältnis von 720 x 480 Quellvideo auf ein Seitenverhältnis von 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="10cab-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="10cab-109">Im Folgenden finden Sie eine Beschreibung der korrekten Anzeige der einzelnen Modi und ihrer Highlights:</span><span class="sxs-lookup"><span data-stu-id="10cab-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="10cab-110">**Widescreen:** Das Quellvideo wurde in den größten 16x9-Bereich des Ausgabefensters gestreckt.</span><span class="sxs-lookup"><span data-stu-id="10cab-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="10cab-111">Die Highlights sind relativ zum Inneren des Bereichs 16x9.</span><span class="sxs-lookup"><span data-stu-id="10cab-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="10cab-112">Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 16x9-Bereich zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="10cab-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="10cab-113">**Schwenkscan:** Verwenden Sie aus dem 16x9-Video den horizontalen Offset, der im MPEG2-Stream bereitgestellt wird, um ein 4x3-Unterfenster zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="10cab-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="10cab-114">Platzieren Sie das 4x3-Unterfenster im größten 4x3-Bereich des Ausgabeclientfensters.</span><span class="sxs-lookup"><span data-stu-id="10cab-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="10cab-115">Die Koordinaten der Hervorhebung sind relativ zum 4x3-Ausgabefenster und haben keine Beziehung zum 16x9-Quellvideo.</span><span class="sxs-lookup"><span data-stu-id="10cab-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="10cab-116">Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 4x3-Bereich zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="10cab-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="10cab-117">**Letterbox:** Berechnen Sie den größten 4x3-Bereich des Ausgabefensters.</span><span class="sxs-lookup"><span data-stu-id="10cab-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="10cab-118">Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 4x3-Bereich zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="10cab-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="10cab-119">Das anamorphe 4x3-Quellvideo (das ein 16x9-Bild darstellt) wird im größten 16x9-Unterfenster innerhalb des Bereichs 4x3 platziert.</span><span class="sxs-lookup"><span data-stu-id="10cab-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="10cab-120">Am oberen und unteren Rand des Unterfensters sollten schwarze Balken hinzugefügt werden, um einen 16x9-Bereich zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="10cab-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="10cab-121">Die Koordinaten der Hervorhebung sind relativ zum 4x3-Bereich und haben keine Beziehung zum 16x9-Quellvideo.</span><span class="sxs-lookup"><span data-stu-id="10cab-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="10cab-122">Es ist möglich, dass ein Datenträger eine Hervorhebung angibt, die sich außerhalb des Bereichs 16 x 9 befindet (aber immer noch im 4x3-Fenster).</span><span class="sxs-lookup"><span data-stu-id="10cab-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="10cab-123">Bei 4x3-Videos wird das Video im größten 4x3-Ausgabebereich des Ausgabeclientfensters platziert.</span><span class="sxs-lookup"><span data-stu-id="10cab-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="10cab-124">Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 4x3-Bereich beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="10cab-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="10cab-125">**MPEG-Vorverarbeitung mit dvd navigator und VMR**</span><span class="sxs-lookup"><span data-stu-id="10cab-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="10cab-126">Derzeit wird dem Decoder ein FORMAT \_ MPEG2 \_ VIDEO-Medientyp übergeben (dessen Formatblock auf eine [**MPEG2VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) zeigt).</span><span class="sxs-lookup"><span data-stu-id="10cab-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="10cab-127">An den Ausgabepins erzeugt der Decoder einen \_ Format VideoInfo2-Medientyp, dessen Formatblock auf eine [**VIDEOINFOHEADER2-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) zeigt.</span><span class="sxs-lookup"><span data-stu-id="10cab-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="10cab-128">Das **dwReserved-Feld** der Struktur wurde in **dwControls-Flags** umbenannt.</span><span class="sxs-lookup"><span data-stu-id="10cab-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="10cab-129">Der **dwControlFlags-Member** enthält jetzt die neuen Bits.</span><span class="sxs-lookup"><span data-stu-id="10cab-129">The **dwControlFlags** member will now contain the new bits.</span></span>



| <span data-ttu-id="10cab-130">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="10cab-130">Label</span></span> | <span data-ttu-id="10cab-131">Wert</span><span class="sxs-lookup"><span data-stu-id="10cab-131">Value</span></span> |
|--------------------------|------------|
| <span data-ttu-id="10cab-132">AMCONTROL \_ VERWENDET</span><span class="sxs-lookup"><span data-stu-id="10cab-132">AMCONTROL\_USED</span></span>          | <span data-ttu-id="10cab-133">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10cab-133">0x00000001</span></span> |
| <span data-ttu-id="10cab-134">AMCONTROL \_ PAD \_ TO \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="10cab-134">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="10cab-135">0x00000002</span><span class="sxs-lookup"><span data-stu-id="10cab-135">0x00000002</span></span> |
| <span data-ttu-id="10cab-136">AMCONTROL \_ PAD \_ TO \_ 16x9</span><span class="sxs-lookup"><span data-stu-id="10cab-136">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="10cab-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="10cab-137">0x00000004</span></span> |



 

<span data-ttu-id="10cab-138">AMCONTROL \_ USED wird verwendet, um zu testen, ob diese neuen Flags unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="10cab-138">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="10cab-139">Ein Quellfilter sollte das AMCONTROL \_ USED-Flag festlegen und prüfen, ob QueryAccept(MediaType) auf dem Downstreampin erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10cab-139">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="10cab-140">Wenn sie abgelehnt wird, können die AMCONTROL-Flags nicht verwendet werden, und dwReserved1 muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="10cab-140">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="10cab-141">AMCONTROL \_ PAD \_ TO \_ 4x3 gibt an, dass das Bild aufgefüllt und in einem 4x3-Bereich angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10cab-141">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="10cab-142">AMCONTROL \_ PAD \_ TO \_ 16x9 gibt an, dass das Bild aufgefüllt und in einem 16x9-Bereich angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10cab-142">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="10cab-143">Der Decoder sollte die Bits entweder blind kopieren oder verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="10cab-143">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="10cab-144">Wenn der Decoder das Letterboxing selbst ausführt, muss er das Pixelseitenverhältnis ändern, das Bild aufpadieren und die entsprechenden \_ \* AMCONTROL-Bits entfernen.</span><span class="sxs-lookup"><span data-stu-id="10cab-144">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="10cab-145">MPEG2VIDEOINFO.dwFlags enthält jetzt drei Flags zum Steuern der Anzeige des Inhalts:</span><span class="sxs-lookup"><span data-stu-id="10cab-145">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="10cab-146">`AMMPEG2_DoPanScan (0x00000001)`: Wenn dieses Flag festgelegt ist, sollte der MPEG-2-Videodecoder das Ausgabebild basierend auf Schwenkscanvektoren in der Bildanzeigeerweiterung zuschneiden und das Seitenverhältnis des Bilds in \_ \_ 4x3 ändern.</span><span class="sxs-lookup"><span data-stu-id="10cab-146">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="10cab-147">Die VMR sollte kein 16x9-Beispiel mit diesem Flag erhalten.</span><span class="sxs-lookup"><span data-stu-id="10cab-147">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="10cab-148">Eine einfache Implementierung kann das Quellrechteck ändern, um einen 540-breiten Quellbereich mit einem linken Rand anzugeben, der dem Anzeigeoffset in der \_ Bildanzeigeerweiterung \_ entspricht.</span><span class="sxs-lookup"><span data-stu-id="10cab-148">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="10cab-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: Wenn ein Hardwaredecoder diesen Stream in einer Videoausgabe anzeigt (in der Regel ein SVIDEO-Connector auf der Karte), sollte er die Regeln zum Anzeigen eines 16x9-Beispiels auf einem 4x3-Display anwenden.</span><span class="sxs-lookup"><span data-stu-id="10cab-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="10cab-150">Ein Softwaredecoder (oder ein Hardwaredecoder, der die Ausgabe erzeugt, die an die VMR gesendet wird) verfügt über zwei Optionen bei der Verarbeitung von Images:</span><span class="sxs-lookup"><span data-stu-id="10cab-150">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="10cab-151">Ignorieren Sie dieses Flag, und übergeben Sie den VideoInfoHeader2-Inhalt an die VMR (das AMCONTROL \_ PAD \_ TO 4x3-Flag wird bereits vom \_ [DVD-Navigator](dvd-navigator-filter.md) im Beispiel festgelegt).</span><span class="sxs-lookup"><span data-stu-id="10cab-151">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="10cab-152">VmR findet ein 16x9-Videobeispiel mit dem Flag AMCONTROL PAD TO 4x3 und einem \_ \_ \_ 4x3-Unterbildstream.</span><span class="sxs-lookup"><span data-stu-id="10cab-152">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="10cab-153">Die Anwendung muss festlegen, dass die ausgabenormierten Zielrechtecke der beiden Datenströme die gleiche Breite haben.</span><span class="sxs-lookup"><span data-stu-id="10cab-153">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="10cab-154">Konvertieren Sie den anamorphen Stream in ein 4x3-Bild, indem Sie den oberen und unteren Rand des Bilds aufpaddieren und das Seitenverhältnis des Bilds auf 4x3 festlegen (siehe Letterbox oben) und das AMCONTROL \_ PAD \_ TO \_ 4x3 Bit aus VIDEOINFOHEADER2 entfernen.</span><span class="sxs-lookup"><span data-stu-id="10cab-154">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="10cab-155">DirectXVA-Decoder, die video- und subpicture-Streams mischen, müssen dieses Flag verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="10cab-155">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="10cab-156">Wenn die Hardware das gemischten Unterbild nicht skalieren kann, sollte der Decoder einen separaten Unterbilddatenstrom erzeugen, damit die VMR mit dem Video kombiniert wird.</span><span class="sxs-lookup"><span data-stu-id="10cab-156">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="10cab-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: Wenn ein Hardwaredecoder diesen Datenstrom in einer Videoausgabe anzeigt (in der Regel ein SVIDEO-Connector auf der Karte), sollte ein 16x9-Display (anamorph) angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="10cab-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="10cab-158">Ein Softwaredecoder (oder ein Hardwaredecoder, der die Ausgabe erzeugt, die an die VMR gesendet wird) verfügt über zwei Optionen bei der Verarbeitung eines anamorphen Bilds:</span><span class="sxs-lookup"><span data-stu-id="10cab-158">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="10cab-159">Ignorieren Sie dieses Flag, und kopieren Sie den VideoInfoHeader2-Inhalt auf die VMR.</span><span class="sxs-lookup"><span data-stu-id="10cab-159">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="10cab-160">Die VMR padt 4x3-Images auf 16 x 9, wenn das \_ AMCONTROL-PAD \_ auf \_ 16 x 9 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="10cab-160">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="10cab-161">Auflisten des Ausgabebilds auf ein 16x9-Bild und Entfernen des \_ AMCONTROL-PAD \_ auf \_ 16 x 9 Bit.</span><span class="sxs-lookup"><span data-stu-id="10cab-161">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="10cab-162">Die meisten Decoder sollten **GetMediaType** verwenden, um eine Medienänderung am Eingabepin zu erkennen und den Inhalt von **VIDEOINFOHEADER2** (in **MPEG2INFOHEADER** enthalten) an den Ausgabepin zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="10cab-162">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="10cab-163">Sie verarbeiten wahrscheinlich nur das PanScan-Bit.</span><span class="sxs-lookup"><span data-stu-id="10cab-163">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="10cab-164">Der folgende Beispielcode zeigt, wie der **VIDEOINFOHEADER2-Inhalt** von einem Eingabepin in einen Ausgabepin kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="10cab-164">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


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



 

 



