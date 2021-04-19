---
description: Ändert die Größe eines Videodaten Stroms.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Video Resizer DSP (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355561"
---
# <a name="video-resizer-dsp"></a><span data-ttu-id="de808-103">Video Resizer DSP</span><span class="sxs-lookup"><span data-stu-id="de808-103">Video Resizer DSP</span></span>

<span data-ttu-id="de808-104">Ändert die Größe eines Videodaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="de808-104">Resizes a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="de808-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="de808-105">CLSID</span></span>

<span data-ttu-id="de808-106">CLSID- \_ Erweiterung</span><span class="sxs-lookup"><span data-stu-id="de808-106">CLSID\_CResizerDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="de808-107">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="de808-107">Interfaces</span></span>

-   [<span data-ttu-id="de808-108">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="de808-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="de808-109">**Imfrealtimeclient**</span><span class="sxs-lookup"><span data-stu-id="de808-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="de808-110">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="de808-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="de808-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="de808-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="de808-112">**Iwmresizer-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="de808-112">**IWMResizerProps**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a><span data-ttu-id="de808-113">Formate</span><span class="sxs-lookup"><span data-stu-id="de808-113">Formats</span></span>

<span data-ttu-id="de808-114">Das Video Resizer DSP unterstützt die folgenden Eingabe-/ausgabemedienuntertypen, wenn diese als DirectX-Medienobjekt (DMO) fungieren.</span><span class="sxs-lookup"><span data-stu-id="de808-114">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="de808-115">mediasubtype \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="de808-115">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="de808-116">Mediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="de808-116">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="de808-117">mediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="de808-117">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="de808-118">Mediasubtype \_ I420</span><span class="sxs-lookup"><span data-stu-id="de808-118">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="de808-119">Mediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="de808-119">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="de808-120">Mediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="de808-120">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="de808-121">Mediasubtype \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="de808-121">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="de808-122">Mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="de808-122">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="de808-123">Mediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="de808-123">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="de808-124">mediasubtype \_ ayuv</span><span class="sxs-lookup"><span data-stu-id="de808-124">MEDIASUBTYPE\_AYUV</span></span>
-   <span data-ttu-id="de808-125">Mediasubtype \_ V216</span><span class="sxs-lookup"><span data-stu-id="de808-125">MEDIASUBTYPE\_V216</span></span>
-   <span data-ttu-id="de808-126">Mediasubtype \_ YV12</span><span class="sxs-lookup"><span data-stu-id="de808-126">MEDIASUBTYPE\_YV12</span></span>

<span data-ttu-id="de808-127">Das Video Resizer DSP unterstützt die folgenden Eingabe-/ausgabemedienuntertypen, wenn diese als Media Foundation Transform (MFT) fungieren.</span><span class="sxs-lookup"><span data-stu-id="de808-127">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="de808-128">MF-Format ( \_ IYUV)</span><span class="sxs-lookup"><span data-stu-id="de808-128">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="de808-129">MF-Format \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="de808-129">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="de808-130">MF-Format ( \_ UYVY)</span><span class="sxs-lookup"><span data-stu-id="de808-130">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="de808-131">MF-Format \_ I420</span><span class="sxs-lookup"><span data-stu-id="de808-131">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="de808-132">MF-Format \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="de808-132">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="de808-133">MF-Format \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="de808-133">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="de808-134">MF-Format \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="de808-134">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="de808-135">MF-Format \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="de808-135">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="de808-136">MF-Format \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="de808-136">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="de808-137">MF-Format ( \_ ayuv)</span><span class="sxs-lookup"><span data-stu-id="de808-137">MFVideoFormat\_AYUV</span></span>
-   <span data-ttu-id="de808-138">MF-Format \_ V216</span><span class="sxs-lookup"><span data-stu-id="de808-138">MFVideoFormat\_V216</span></span>
-   <span data-ttu-id="de808-139">MF-Format \_ YV12</span><span class="sxs-lookup"><span data-stu-id="de808-139">MFVideoFormat\_YV12</span></span>

## <a name="properties"></a><span data-ttu-id="de808-140">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de808-140">Properties</span></span>

-   [<span data-ttu-id="de808-141">mfpkey- \_ Größenänderung für \_ src \_ left</span><span class="sxs-lookup"><span data-stu-id="de808-141">MFPKEY\_RESIZE\_SRC\_LEFT</span></span>](mfpkey-resize-src-left.md)
-   [<span data-ttu-id="de808-142">mfpkey- \_ Größenänderung, \_ \_ oben</span><span class="sxs-lookup"><span data-stu-id="de808-142">MFPKEY\_RESIZE\_SRC\_TOP</span></span>](mfpkey-resize-src-top.md)
-   [<span data-ttu-id="de808-143">mfpkey- \_ Größe für \_ src- \_ Breite</span><span class="sxs-lookup"><span data-stu-id="de808-143">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span>](mfpkey-resize-src-width.md)
-   [<span data-ttu-id="de808-144">mfpkey- \_ Größenänderung für \_ src- \_ Höhe</span><span class="sxs-lookup"><span data-stu-id="de808-144">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span>](mfpkey-resize-src-height.md)
-   [<span data-ttu-id="de808-145">mfpkey- \_ Größe nach \_ \_ Links ändern</span><span class="sxs-lookup"><span data-stu-id="de808-145">MFPKEY\_RESIZE\_DST\_LEFT</span></span>](mfpkey-resize-dst-left.md)
-   [<span data-ttu-id="de808-146">mfpkey \_ Größenänderung nach \_ \_ oben</span><span class="sxs-lookup"><span data-stu-id="de808-146">MFPKEY\_RESIZE\_DST\_TOP</span></span>](mfpkey-resize-dst-top.md)
-   [<span data-ttu-id="de808-147">mfpkey- \_ \_ DST- \_ Breite ändern</span><span class="sxs-lookup"><span data-stu-id="de808-147">MFPKEY\_RESIZE\_DST\_WIDTH</span></span>](mfpkey-resize-dst-width.md)
-   [<span data-ttu-id="de808-148">mfpkey- \_ \_ DST- \_ Höhe ändern</span><span class="sxs-lookup"><span data-stu-id="de808-148">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span>](mfpkey-resize-dst-height.md)
-   [<span data-ttu-id="de808-149">mfpkey- \_ Qualität der Größenänderung \_</span><span class="sxs-lookup"><span data-stu-id="de808-149">MFPKEY\_RESIZE\_QUALITY</span></span>](mfpkey-resize-quality.md)
-   [<span data-ttu-id="de808-150">mfpkey- \_ interspitze für die Größenänderung \_</span><span class="sxs-lookup"><span data-stu-id="de808-150">MFPKEY\_RESIZE\_INTERLACE</span></span>](mfpkey-resize-interlace.md)
-   [<span data-ttu-id="de808-151">mfpkey \_ Ändern von \_ geomapx</span><span class="sxs-lookup"><span data-stu-id="de808-151">MFPKEY\_RESIZE\_GEOMAPX</span></span>](mfpkey-resize-geomapx.md)
-   [<span data-ttu-id="de808-152">mfpkey \_ Ändern der \_ geomapy</span><span class="sxs-lookup"><span data-stu-id="de808-152">MFPKEY\_RESIZE\_GEOMAPY</span></span>](mfpkey-resize-geomapy.md)
-   [<span data-ttu-id="de808-153">mfpkey \_ Ändern von \_ geomapwidth</span><span class="sxs-lookup"><span data-stu-id="de808-153">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span>](mfpkey-resize-geomapwidth.md)
-   [<span data-ttu-id="de808-154">mfpkey- \_ Größe für \_ geomapheight ändern</span><span class="sxs-lookup"><span data-stu-id="de808-154">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span>](mfpkey-resize-geomapheight.md)
-   [<span data-ttu-id="de808-155">mfpkey- \_ Größe ändern \_ minapx</span><span class="sxs-lookup"><span data-stu-id="de808-155">MFPKEY\_RESIZE\_MINAPX</span></span>](mfpkey-resize-minapx.md)
-   [<span data-ttu-id="de808-156">mfpkey- \_ Größe ändern \_</span><span class="sxs-lookup"><span data-stu-id="de808-156">MFPKEY\_RESIZE\_MINAPY</span></span>](mfpkey-resize-minapy.md)
-   [<span data-ttu-id="de808-157">mfpkey- \_ Größe ändern \_ minapwidth</span><span class="sxs-lookup"><span data-stu-id="de808-157">MFPKEY\_RESIZE\_MINAPWIDTH</span></span>](mfpkey-resize-minapwidth.md)
-   [<span data-ttu-id="de808-158">mfpkey-Wert für \_ \_ minapheight ändern</span><span class="sxs-lookup"><span data-stu-id="de808-158">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span>](mfpkey-resize-minapheight.md)
-   [<span data-ttu-id="de808-159">mfpkey- \_ Größe ändern von \_ panscanapx</span><span class="sxs-lookup"><span data-stu-id="de808-159">MFPKEY\_RESIZE\_PANSCANAPX</span></span>](mfpkey-resize-panscanapx.md)
-   [<span data-ttu-id="de808-160">mfpkey \_ Resize \_ panscanapy</span><span class="sxs-lookup"><span data-stu-id="de808-160">MFPKEY\_RESIZE\_PANSCANAPY</span></span>](mfpkey-resize-panscanapy.md)
-   [<span data-ttu-id="de808-161">mfpkey- \_ Größe ändern von \_ panscanapwidth</span><span class="sxs-lookup"><span data-stu-id="de808-161">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span>](mfpkey-resize-panscanapwidth.md)
-   [<span data-ttu-id="de808-162">mfpkey- \_ Größe ändern von \_ panscanapheight</span><span class="sxs-lookup"><span data-stu-id="de808-162">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span>](mfpkey-resize-panscanapheight.md)
-   [<span data-ttu-id="de808-163">mfpkey \_ pixelaspectratio</span><span class="sxs-lookup"><span data-stu-id="de808-163">MFPKEY\_PIXELASPECTRATIO</span></span>](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a><span data-ttu-id="de808-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de808-164">Remarks</span></span>

<span data-ttu-id="de808-165">Das Video Resizer DSP ist als COM-Objekt implementiert, das als DMO oder MFT fungieren kann.</span><span class="sxs-lookup"><span data-stu-id="de808-165">The Video Resizer DSP is implemented as a COM object that can act as a DMO or an MFT.</span></span> <span data-ttu-id="de808-166">Das-Objekt verfügt über einen einzelnen Klassen Bezeichner (CLSID), unabhängig davon, ob er als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="de808-166">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="de808-167">Informationen dazu, wann ein DSP als DMO oder MFT fungiert, finden Sie unter [digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="de808-167">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="de808-168">Die global eindeutigen Bezeichner (GUIDs) für RGB-Medien Untertypen unterscheiden sich abhängig davon, ob ein DSP als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="de808-168">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="de808-169">Die GUIDs für nicht-RGB-Medien Untertypen sind identisch, unabhängig davon, ob ein DSP als DMO oder MFT fungiert.</span><span class="sxs-lookup"><span data-stu-id="de808-169">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="de808-170">Informationen zu den GUIDs, die Medien Untertypen darstellen, finden Sie [unter Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="de808-170">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="de808-171">Dieser DSP kann sowohl das Zuschneiden als auch das Skalieren des Video Bilds durchführen.</span><span class="sxs-lookup"><span data-stu-id="de808-171">This DSP can perform both cropping and scaling on the video image.</span></span> <span data-ttu-id="de808-172">Das Format des Ausgabe Typs muss mit dem Format des Eingabetyps identisch sein.</span><span class="sxs-lookup"><span data-stu-id="de808-172">The format of the output type must match the format of the input type.</span></span> <span data-ttu-id="de808-173">Der DSP führt keine Farb Raum Konvertierungen aus.</span><span class="sxs-lookup"><span data-stu-id="de808-173">The DSP does not perform color-space conversions.</span></span>

<span data-ttu-id="de808-174">Bevor Sie den Ausgabetyp festlegen können, können Sie mithilfe der in dieser Tabelle aufgeführten Eigenschaften eine beliebige der folgenden Regionen definieren.</span><span class="sxs-lookup"><span data-stu-id="de808-174">Before setting the output type, you can define any of the following regions by using the properties listed in this table.</span></span>



| <span data-ttu-id="de808-175">Region</span><span class="sxs-lookup"><span data-stu-id="de808-175">Region</span></span>                   | <span data-ttu-id="de808-176">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de808-176">Properties</span></span>                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de808-177">Quell Rechteck</span><span class="sxs-lookup"><span data-stu-id="de808-177">Source rectangle</span></span>         | <span data-ttu-id="de808-178">mfpkey- \_ Größenänderung für \_ src \_ left</span><span class="sxs-lookup"><span data-stu-id="de808-178">MFPKEY\_RESIZE\_SRC\_LEFT</span></span><br/> <span data-ttu-id="de808-179">mfpkey- \_ Größenänderung, \_ \_ oben</span><span class="sxs-lookup"><span data-stu-id="de808-179">MFPKEY\_RESIZE\_SRC\_TOP</span></span><br/> <span data-ttu-id="de808-180">mfpkey- \_ Größe für \_ src- \_ Breite</span><span class="sxs-lookup"><span data-stu-id="de808-180">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span><br/> <span data-ttu-id="de808-181">mfpkey- \_ Größenänderung für \_ src- \_ Höhe</span><span class="sxs-lookup"><span data-stu-id="de808-181">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="de808-182">Ziel Rechteck</span><span class="sxs-lookup"><span data-stu-id="de808-182">Destination rectangle</span></span>    | <span data-ttu-id="de808-183">mfpkey- \_ Größe nach \_ \_ Links ändern</span><span class="sxs-lookup"><span data-stu-id="de808-183">MFPKEY\_RESIZE\_DST\_LEFT</span></span><br/> <span data-ttu-id="de808-184">mfpkey \_ Größenänderung nach \_ \_ oben</span><span class="sxs-lookup"><span data-stu-id="de808-184">MFPKEY\_RESIZE\_DST\_TOP</span></span><br/> <span data-ttu-id="de808-185">mfpkey- \_ \_ DST- \_ Breite ändern</span><span class="sxs-lookup"><span data-stu-id="de808-185">MFPKEY\_RESIZE\_DST\_WIDTH</span></span><br/> <span data-ttu-id="de808-186">mfpkey- \_ \_ DST- \_ Höhe ändern</span><span class="sxs-lookup"><span data-stu-id="de808-186">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="de808-187">Geometrische Öffnung</span><span class="sxs-lookup"><span data-stu-id="de808-187">Geometric aperture</span></span>       | <span data-ttu-id="de808-188">mfpkey \_ Ändern von \_ geomapx</span><span class="sxs-lookup"><span data-stu-id="de808-188">MFPKEY\_RESIZE\_GEOMAPX</span></span><br/> <span data-ttu-id="de808-189">mfpkey \_ Ändern der \_ geomapy</span><span class="sxs-lookup"><span data-stu-id="de808-189">MFPKEY\_RESIZE\_GEOMAPY</span></span><br/> <span data-ttu-id="de808-190">mfpkey \_ Ändern von \_ geomapwidth</span><span class="sxs-lookup"><span data-stu-id="de808-190">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span><br/> <span data-ttu-id="de808-191">mfpkey- \_ Größe für \_ geomapheight ändern</span><span class="sxs-lookup"><span data-stu-id="de808-191">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span><br/>             |
| <span data-ttu-id="de808-192">Minimale Anzeige Öffnung</span><span class="sxs-lookup"><span data-stu-id="de808-192">Minimum display aperture</span></span> | <span data-ttu-id="de808-193">mfpkey- \_ Größe ändern \_ minapx</span><span class="sxs-lookup"><span data-stu-id="de808-193">MFPKEY\_RESIZE\_MINAPX</span></span><br/> <span data-ttu-id="de808-194">mfpkey- \_ Größe ändern \_</span><span class="sxs-lookup"><span data-stu-id="de808-194">MFPKEY\_RESIZE\_MINAPY</span></span><br/> <span data-ttu-id="de808-195">mfpkey- \_ Größe ändern \_ minapwidth</span><span class="sxs-lookup"><span data-stu-id="de808-195">MFPKEY\_RESIZE\_MINAPWIDTH</span></span><br/> <span data-ttu-id="de808-196">mfpkey-Wert für \_ \_ minapheight ändern</span><span class="sxs-lookup"><span data-stu-id="de808-196">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span><br/>                 |
| <span data-ttu-id="de808-197">Bereich schwenken/Scannen</span><span class="sxs-lookup"><span data-stu-id="de808-197">Pan/scan region</span></span>          | <span data-ttu-id="de808-198">mfpkey- \_ Größe ändern von \_ panscanapx</span><span class="sxs-lookup"><span data-stu-id="de808-198">MFPKEY\_RESIZE\_PANSCANAPX</span></span><br/> <span data-ttu-id="de808-199">mfpkey \_ Resize \_ panscanapy</span><span class="sxs-lookup"><span data-stu-id="de808-199">MFPKEY\_RESIZE\_PANSCANAPY</span></span><br/> <span data-ttu-id="de808-200">mfpkey- \_ Größe ändern von \_ panscanapwidth</span><span class="sxs-lookup"><span data-stu-id="de808-200">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span><br/> <span data-ttu-id="de808-201">mfpkey- \_ Größe ändern von \_ panscanapheight</span><span class="sxs-lookup"><span data-stu-id="de808-201">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span><br/> |



 

<span data-ttu-id="de808-202">In jedem Fall müssen Sie alle zugeordneten Eigenschaften festlegen, damit die Einstellung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="de808-202">In each case, you must set all of the associated properties for the setting to take effect.</span></span>

<span data-ttu-id="de808-203">Der DSP kopiert den Teil des Quell Bilds, der durch das Quell Rechteck definiert ist, und streckt oder komprimiert ihn auf das Ziel Rechteck im Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="de808-203">The DSP copies the portion of the source image defined by source rectangle, and stretches or compresses it onto the destination rectangle on the output buffer.</span></span> <span data-ttu-id="de808-204">Die Quell-und Ziel Rechtecke müssen nicht die gleiche Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="de808-204">The source and destination rectangles do not need to be the same size.</span></span> <span data-ttu-id="de808-205">Die Frame Größe im Ausgabe Medientyp muss groß genug sein, um das Ziel Rechteck aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="de808-205">The frame size in the output media type must be large enough to hold the destination rectangle.</span></span>

<span data-ttu-id="de808-206">Die geometrische Öffnung, die minimale Anzeige Öffnung und der Pan/Scan-Bereich haben keine Auswirkung darauf, wie die Größe des Videos von DSP geändert wird.</span><span class="sxs-lookup"><span data-stu-id="de808-206">The geometric aperture, minimum display aperture, and pan/scan region do not affect how the DSP resizes the video.</span></span> <span data-ttu-id="de808-207">Sie können sich jedoch darauf auswirken, wie die Downstreamkomponente den Videoframe interpretiert.</span><span class="sxs-lookup"><span data-stu-id="de808-207">However, they might affect how the downstream component interprets the video frame.</span></span> <span data-ttu-id="de808-208">Insbesondere verwendet der Enhanced Video Renderer (EVR) diese Werte, wenn er das Bildseiten Verhältnis und den Anzeigebereich berechnet.</span><span class="sxs-lookup"><span data-stu-id="de808-208">In particular, the enhanced video renderer (EVR) uses these values when it calculates the picture aspect ratio and the display area.</span></span>

<span data-ttu-id="de808-209">Wenn Sie Media Foundation Medientypen verwenden, können Sie die geometrische Öffnung, die minimale Anzeige Öffnung und die Pan/Scan-Bereiche direkt im Ausgabe Medientyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="de808-209">If you are using Media Foundation media types, you can set the geometric aperture, minimum display aperture, and pan/scan regions directly in the output media type.</span></span> <span data-ttu-id="de808-210">Wenn Sie DMO-Medientypen verwenden, legen Sie diese mithilfe der Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="de808-210">Otherwise, if you are using DMO media types, set them using the properties.</span></span>

<span data-ttu-id="de808-211">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="de808-211">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="de808-212">**\_geometrische Monte-MT- \_ \_ Öffnung**</span><span class="sxs-lookup"><span data-stu-id="de808-212">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
-   [<span data-ttu-id="de808-213">**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**</span><span class="sxs-lookup"><span data-stu-id="de808-213">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="de808-214">**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**</span><span class="sxs-lookup"><span data-stu-id="de808-214">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a><span data-ttu-id="de808-215">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de808-215">Requirements</span></span>



| <span data-ttu-id="de808-216">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de808-216">Requirement</span></span> | <span data-ttu-id="de808-217">Wert</span><span class="sxs-lookup"><span data-stu-id="de808-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de808-218">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de808-218">Minimum supported client</span></span><br/> | <span data-ttu-id="de808-219">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de808-219">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="de808-220">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de808-220">Minimum supported server</span></span><br/> | <span data-ttu-id="de808-221">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de808-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de808-222">Header</span><span class="sxs-lookup"><span data-stu-id="de808-222">Header</span></span><br/>                   | <dl> <span data-ttu-id="de808-223"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de808-223"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="de808-224">DLL</span><span class="sxs-lookup"><span data-stu-id="de808-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de808-225"><dt>Vidreszr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de808-225"><dt>Vidreszr.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de808-226">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de808-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de808-227">Digitale Signal Prozessoren</span><span class="sxs-lookup"><span data-stu-id="de808-227">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
