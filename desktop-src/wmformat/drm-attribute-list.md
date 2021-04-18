---
title: DRM-Attribut Liste
description: DRM-Attribut Liste
ms.assetid: 222ef91c-b776-4de8-b1ad-88c2beca05aa
keywords:
- Windows Media-Format-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, Digital Rights Management (DRM)
- Digital Rights Management (DRM), Attribute
- DRM (Digital Rights Management), Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3beccc33a48f57015040f06c140a55f5f9691daa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337815"
---
# <a name="drm-attribute-list"></a><span data-ttu-id="83bd3-109">DRM-Attribut Liste</span><span class="sxs-lookup"><span data-stu-id="83bd3-109">DRM Attribute List</span></span>

<span data-ttu-id="83bd3-110">In der folgenden Tabelle werden alle DRM-bezogenen Dateiattribute aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="83bd3-110">For convenience, the following table lists all the DRM-related file attributes.</span></span> <span data-ttu-id="83bd3-111">(Diese Attribute werden auch in der Tabelle mit allen Attributen in der [Attribut Liste](attribute-list.md)aufgeführt.)</span><span class="sxs-lookup"><span data-stu-id="83bd3-111">(These attributes are also listed in the table of all attributes under [Attribute List](attribute-list.md).)</span></span>

<span data-ttu-id="83bd3-112">Diese Werte können von Anwendungen beim Schreiben von DRM-Dateien festgelegt werden, und Sie können beim Lesen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="83bd3-112">Applications can set these values when writing DRM files and can retrieve them when reading.</span></span>



| <span data-ttu-id="83bd3-113">DRM-Datei Attribut</span><span class="sxs-lookup"><span data-stu-id="83bd3-113">DRM file attribute</span></span>                                                                   | <span data-ttu-id="83bd3-114">Globaler Bezeichner</span><span class="sxs-lookup"><span data-stu-id="83bd3-114">Global identifier</span></span>                             | <span data-ttu-id="83bd3-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="83bd3-115">Data type</span></span>             |
|--------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|
| [<span data-ttu-id="83bd3-116">**DRM- \_ contentid**</span><span class="sxs-lookup"><span data-stu-id="83bd3-116">**DRM\_ContentID**</span></span>](drm-contentid.md)                                              | <span data-ttu-id="83bd3-117">g \_ wszwmdrm- \_ contentid</span><span class="sxs-lookup"><span data-stu-id="83bd3-117">g\_wszWMDRM\_ContentID</span></span>                        | <span data-ttu-id="83bd3-118">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-118">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-119">**DRM- \_ drmHeader- \_ contentdistributor**</span><span class="sxs-lookup"><span data-stu-id="83bd3-119">**DRM\_DRMHeader\_ContentDistributor**</span></span>](drm-drmheader-contentdistributor.md)       | <span data-ttu-id="83bd3-120">g \_ wszwmdrm \_ drmHeader- \_ contentdistributor</span><span class="sxs-lookup"><span data-stu-id="83bd3-120">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>    | <span data-ttu-id="83bd3-121">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-121">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-122">**DRM- \_ drmHeader- \_ contentid**</span><span class="sxs-lookup"><span data-stu-id="83bd3-122">**DRM\_DRMHeader\_ContentID**</span></span>](drm-drmheader-contentid.md)                         | <span data-ttu-id="83bd3-123">g \_ wszwmdrm \_ drmHeader \_ contentid</span><span class="sxs-lookup"><span data-stu-id="83bd3-123">g\_wszWMDRM\_DRMHeader\_ContentID</span></span>             | <span data-ttu-id="83bd3-124">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-124">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-125">**DRM \_ drmHeader \_ IndividualizedVersion**</span><span class="sxs-lookup"><span data-stu-id="83bd3-125">**DRM\_DRMHeader\_IndividualizedVersion**</span></span>](drm-drmheader-individualizedversion.md) | <span data-ttu-id="83bd3-126">g \_ wszwmdrm \_ drmHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="83bd3-126">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span> | <span data-ttu-id="83bd3-127">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-127">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-128">**DRM- \_ drmHeader- \_ keyid**</span><span class="sxs-lookup"><span data-stu-id="83bd3-128">**DRM\_DRMHeader\_KeyID**</span></span>](drm-drmheader-keyid.md)                                 | <span data-ttu-id="83bd3-129">g \_ wszwmdrm \_ drmHeader- \_ keyid</span><span class="sxs-lookup"><span data-stu-id="83bd3-129">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>                 | <span data-ttu-id="83bd3-130">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-130">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-131">**DRM \_ drmHeader \_ licenanacqurl**</span><span class="sxs-lookup"><span data-stu-id="83bd3-131">**DRM\_DRMHeader\_LicenseAcqURL**</span></span>](drm-drmheader-licenseacqurl.md)                 | <span data-ttu-id="83bd3-132">g \_ wszwmdrm \_ drmHeader \_ licengacqurl</span><span class="sxs-lookup"><span data-stu-id="83bd3-132">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>         | <span data-ttu-id="83bd3-133">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-133">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-134">**DRM- \_ drmHeader- \_ abonnemencontentid**</span><span class="sxs-lookup"><span data-stu-id="83bd3-134">**DRM\_DRMHeader\_SubscriptionContentID**</span></span>](drm-drmheader-subscriptioncontentid.md) | <span data-ttu-id="83bd3-135">g \_ wszwmdrm \_ drmHeader \_ abonnemencontentid</span><span class="sxs-lookup"><span data-stu-id="83bd3-135">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span> | <span data-ttu-id="83bd3-136">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-136">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-137">**DRM- \_ drmHeader**</span><span class="sxs-lookup"><span data-stu-id="83bd3-137">**DRM\_DRMHeader**</span></span>](drm-drmheader.md)                                              | <span data-ttu-id="83bd3-138">g \_ wszwmdrm \_ drmHeader</span><span class="sxs-lookup"><span data-stu-id="83bd3-138">g\_wszWMDRM\_DRMHeader</span></span>                        | <span data-ttu-id="83bd3-139">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-139">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-140">**DRM- \_ IndividualizedVersion**</span><span class="sxs-lookup"><span data-stu-id="83bd3-140">**DRM\_IndividualizedVersion**</span></span>](drm-individualizedversion.md)                      | <span data-ttu-id="83bd3-141">g \_ wszwmdrm \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="83bd3-141">g\_wszWMDRM\_IndividualizedVersion</span></span>            | <span data-ttu-id="83bd3-142">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-142">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-143">**DRM- \_ Schlüssel-ID**</span><span class="sxs-lookup"><span data-stu-id="83bd3-143">**DRM\_KeyID**</span></span>](drm-keyid.md)                                                      | <span data-ttu-id="83bd3-144">Schlüssel-ID für g \_ wszwmdrm \_</span><span class="sxs-lookup"><span data-stu-id="83bd3-144">g\_wszWMDRM\_KeyID</span></span>                            | <span data-ttu-id="83bd3-145">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-145">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-146">**DRM- \_ lasignaturecert**</span><span class="sxs-lookup"><span data-stu-id="83bd3-146">**DRM\_LASignatureCert**</span></span>](drm-lasignaturecert.md)                                  | <span data-ttu-id="83bd3-147">g \_ wszwmdrm \_ lasignaturecert</span><span class="sxs-lookup"><span data-stu-id="83bd3-147">g\_wszWMDRM\_LASignatureCert</span></span>                  | <span data-ttu-id="83bd3-148">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-148">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-149">**DRM \_ lasignaturelicsrvcert**</span><span class="sxs-lookup"><span data-stu-id="83bd3-149">**DRM\_LASignatureLicSrvCert**</span></span>](drm-lasignaturelicsrvcert.md)                      | <span data-ttu-id="83bd3-150">g \_ wszwmdrm \_ lasignaturelicsrvcert</span><span class="sxs-lookup"><span data-stu-id="83bd3-150">g\_wszWMDRM\_LASignatureLicSrvCert</span></span>            | <span data-ttu-id="83bd3-151">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-151">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-152">**DRM- \_ lasignatureprivkey**</span><span class="sxs-lookup"><span data-stu-id="83bd3-152">**DRM\_LASignaturePrivKey**</span></span>](drm-lasignatureprivkey.md)                            | <span data-ttu-id="83bd3-153">g \_ wszwmdrm \_ lasignatureprivkey</span><span class="sxs-lookup"><span data-stu-id="83bd3-153">g\_wszWMDRM\_LASignaturePrivKey</span></span>               | <span data-ttu-id="83bd3-154">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-154">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-155">**DRM \_ lasignaturerootcert**</span><span class="sxs-lookup"><span data-stu-id="83bd3-155">**DRM\_LASignatureRootCert**</span></span>](drm-lasignaturerootcert.md)                          | <span data-ttu-id="83bd3-156">g \_ wszwmdrm \_ lasignaturerootcert</span><span class="sxs-lookup"><span data-stu-id="83bd3-156">g\_wszWMDRM\_LASignatureRootCert</span></span>              | <span data-ttu-id="83bd3-157">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-157">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-158">**DRM- \_ Lizenz-AcqURL**</span><span class="sxs-lookup"><span data-stu-id="83bd3-158">**DRM\_LicenseAcqURL**</span></span>](drm-licenseacqurl.md)                                      | <span data-ttu-id="83bd3-159">"g \_ wszwmdrm \_ licenanacqurl"</span><span class="sxs-lookup"><span data-stu-id="83bd3-159">g\_wszWMDRM\_LicenseAcqURL</span></span>                    | <span data-ttu-id="83bd3-160">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-160">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="83bd3-161">**DRM- \_ V1LicenseAcqURL**</span><span class="sxs-lookup"><span data-stu-id="83bd3-161">**DRM\_V1LicenseAcqURL**</span></span>](drm-v1licenseacqurl.md)                                  | <span data-ttu-id="83bd3-162">g \_ wszwmdrm \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="83bd3-162">g\_wszWMDRM\_V1LicenseAcqURL</span></span>                  | <span data-ttu-id="83bd3-163">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="83bd3-163">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="83bd3-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83bd3-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83bd3-165">**Attribute nach Typ**</span><span class="sxs-lookup"><span data-stu-id="83bd3-165">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="83bd3-166">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="83bd3-166">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




