---
description: MSTape-Treiber
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: MSTape-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951084f8827f925bba43028c0792736883d5ff0f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909398"
---
# <a name="mstape-driver"></a><span data-ttu-id="49ec6-103">MSTape-Treiber</span><span class="sxs-lookup"><span data-stu-id="49ec6-103">MSTape Driver</span></span>

<span data-ttu-id="49ec6-104">Dieses Thema gilt für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="49ec6-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="49ec6-105">Der MSTape-Treiber unterstützt D-VHS- und MPEG-Mpeg-Geräte.</span><span class="sxs-lookup"><span data-stu-id="49ec6-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="49ec6-106">Sie wird für Anwendungen als [WDM Video Capture-Filter](wdm-video-capture-filter.md) verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="49ec6-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="49ec6-107">Seine Funktionalität ähnelt der von [MSDV](msdv-driver.md), dem DV-Treiber:</span><span class="sxs-lookup"><span data-stu-id="49ec6-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="49ec6-108">Sie wird in den Filterkategorien "Video Capture Sources" (CLSID \_ VideoInputDeviceCategory) und "WDM Streaming Rendering Devices" (AM \_ KSCATEGORY \_ RENDER) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="49ec6-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="49ec6-109">Eine Anwendung kann mithilfe der [**ICreateDevEnum-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) eine Instanz des Filters erstellen.</span><span class="sxs-lookup"><span data-stu-id="49ec6-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="49ec6-110">Sie verfügt über einen Ausgabestecker für die Erfassung und den Transport vom Gerät und einen Eingabepin für den Transport zum Gerät.</span><span class="sxs-lookup"><span data-stu-id="49ec6-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="49ec6-111">Es kann jeweils nur eine Stecknadel verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="49ec6-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="49ec6-112">**Medientypen**</span><span class="sxs-lookup"><span data-stu-id="49ec6-112">**Media Types**</span></span>

<span data-ttu-id="49ec6-113">Der Eingabepin unterstützt einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="49ec6-113">The input pin supports one media type.</span></span>



| <span data-ttu-id="49ec6-114">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="49ec6-114">Label</span></span> | <span data-ttu-id="49ec6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="49ec6-115">Value</span></span> |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="49ec6-116">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="49ec6-116">Major Type</span></span>   | <span data-ttu-id="49ec6-117">\_MEDIATYPE-Stream</span><span class="sxs-lookup"><span data-stu-id="49ec6-117">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="49ec6-118">Subtype</span><span class="sxs-lookup"><span data-stu-id="49ec6-118">Subtype</span></span>      | <span data-ttu-id="49ec6-119">MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE</span><span class="sxs-lookup"><span data-stu-id="49ec6-119">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="49ec6-120">Stichprobengröße</span><span class="sxs-lookup"><span data-stu-id="49ec6-120">Sample Size</span></span>  | <span data-ttu-id="49ec6-121">192 x 256</span><span class="sxs-lookup"><span data-stu-id="49ec6-121">192 x 256</span></span>                                                  |
| <span data-ttu-id="49ec6-122">Block formatieren</span><span class="sxs-lookup"><span data-stu-id="49ec6-122">Format Block</span></span> | [<span data-ttu-id="49ec6-123">**MPEG2 \_ TRANSPORT \_ STRIDE**</span><span class="sxs-lookup"><span data-stu-id="49ec6-123">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="49ec6-124">Der Ausgabepin unterstützt zwei Medientypen.</span><span class="sxs-lookup"><span data-stu-id="49ec6-124">The output pin supports two media types.</span></span>



| <span data-ttu-id="49ec6-125">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="49ec6-125">Label</span></span> | <span data-ttu-id="49ec6-126">Wert</span><span class="sxs-lookup"><span data-stu-id="49ec6-126">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="49ec6-127">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="49ec6-127">Major Type</span></span>   | <span data-ttu-id="49ec6-128">\_MEDIATYPE-Stream</span><span class="sxs-lookup"><span data-stu-id="49ec6-128">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="49ec6-129">Subtype</span><span class="sxs-lookup"><span data-stu-id="49ec6-129">Subtype</span></span>      | <span data-ttu-id="49ec6-130">MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT-STRIDE \_</span><span class="sxs-lookup"><span data-stu-id="49ec6-130">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="49ec6-131">Stichprobengröße</span><span class="sxs-lookup"><span data-stu-id="49ec6-131">Sample Size</span></span>  | <span data-ttu-id="49ec6-132">192 x 256</span><span class="sxs-lookup"><span data-stu-id="49ec6-132">192 x 256</span></span>                              |
| <span data-ttu-id="49ec6-133">Formatblock</span><span class="sxs-lookup"><span data-stu-id="49ec6-133">Format Block</span></span> | <span data-ttu-id="49ec6-134">\_ \_ MPEG2-TRANSPORT-STRIDE</span><span class="sxs-lookup"><span data-stu-id="49ec6-134">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



| <span data-ttu-id="49ec6-135">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="49ec6-135">Label</span></span> | <span data-ttu-id="49ec6-136">Wert</span><span class="sxs-lookup"><span data-stu-id="49ec6-136">Value</span></span> |
|--------------|----------------------------------------|
| <span data-ttu-id="49ec6-137">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="49ec6-137">Major Type</span></span>   | <span data-ttu-id="49ec6-138">\_MEDIATYPE-Stream</span><span class="sxs-lookup"><span data-stu-id="49ec6-138">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="49ec6-139">Subtype</span><span class="sxs-lookup"><span data-stu-id="49ec6-139">Subtype</span></span>      | <span data-ttu-id="49ec6-140">MEDIASUBTYPE \_ \_ MPEG2-TRANSPORT-STRIDE \_</span><span class="sxs-lookup"><span data-stu-id="49ec6-140">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="49ec6-141">Stichprobengröße</span><span class="sxs-lookup"><span data-stu-id="49ec6-141">Sample Size</span></span>  | <span data-ttu-id="49ec6-142">188 x 256</span><span class="sxs-lookup"><span data-stu-id="49ec6-142">188 x 256</span></span>                              |
| <span data-ttu-id="49ec6-143">Formatblock</span><span class="sxs-lookup"><span data-stu-id="49ec6-143">Format Block</span></span> | <span data-ttu-id="49ec6-144">**NULL**</span><span class="sxs-lookup"><span data-stu-id="49ec6-144">**NULL**</span></span>                               |



 

<span data-ttu-id="49ec6-145">**Geräteinformationen**</span><span class="sxs-lookup"><span data-stu-id="49ec6-145">**Device Information**</span></span>

<span data-ttu-id="49ec6-146">Der Treiber liest Informationen dynamisch aus der Gerätekonfigurations-ROM.</span><span class="sxs-lookup"><span data-stu-id="49ec6-146">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="49ec6-147">Die Anwendung kann diese Informationen abrufen, indem sie den Gerätemoniker an eine Eigenschaftentüte binden und die **IPropertyBag::Read-Methode** aufruft.</span><span class="sxs-lookup"><span data-stu-id="49ec6-147">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="49ec6-148">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="49ec6-148">Property</span></span>            | <span data-ttu-id="49ec6-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49ec6-149">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="49ec6-150">Datentyp</span><span class="sxs-lookup"><span data-stu-id="49ec6-150">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="49ec6-151">UniqueID \_ Low</span><span class="sxs-lookup"><span data-stu-id="49ec6-151">UniqueID\_Low</span></span>       | <span data-ttu-id="49ec6-152">Eindeutige ID des Geräts **(niedriges DWORD).**</span><span class="sxs-lookup"><span data-stu-id="49ec6-152">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="49ec6-153">**long** (VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="49ec6-153">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="49ec6-154">UniqueID \_ High</span><span class="sxs-lookup"><span data-stu-id="49ec6-154">UniqueID\_High</span></span>      | <span data-ttu-id="49ec6-155">Eindeutige ID des Geräts (hoher **DWORD-Wert)**</span><span class="sxs-lookup"><span data-stu-id="49ec6-155">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="49ec6-156">**long**</span><span class="sxs-lookup"><span data-stu-id="49ec6-156">**long**</span></span>            |
| <span data-ttu-id="49ec6-157">VendorID</span><span class="sxs-lookup"><span data-stu-id="49ec6-157">VendorID</span></span>            | <span data-ttu-id="49ec6-158">Anbieter-ID.</span><span class="sxs-lookup"><span data-stu-id="49ec6-158">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="49ec6-159">**long**</span><span class="sxs-lookup"><span data-stu-id="49ec6-159">**long**</span></span>            |
| <span data-ttu-id="49ec6-160">ModelID</span><span class="sxs-lookup"><span data-stu-id="49ec6-160">ModelID</span></span>             | <span data-ttu-id="49ec6-161">Modell-ID</span><span class="sxs-lookup"><span data-stu-id="49ec6-161">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="49ec6-162">**long**</span><span class="sxs-lookup"><span data-stu-id="49ec6-162">**long**</span></span>            |
| <span data-ttu-id="49ec6-163">VendorText</span><span class="sxs-lookup"><span data-stu-id="49ec6-163">VendorText</span></span>          | <span data-ttu-id="49ec6-164">Name des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="49ec6-164">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="49ec6-165">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="49ec6-165">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="49ec6-166">ModelText</span><span class="sxs-lookup"><span data-stu-id="49ec6-166">ModelText</span></span>           | <span data-ttu-id="49ec6-167">Name des Gerätemodells.</span><span class="sxs-lookup"><span data-stu-id="49ec6-167">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="49ec6-168">**Bstr**</span><span class="sxs-lookup"><span data-stu-id="49ec6-168">**BSTR**</span></span>            |
| <span data-ttu-id="49ec6-169">UnitModelText</span><span class="sxs-lookup"><span data-stu-id="49ec6-169">UnitModelText</span></span>       | <span data-ttu-id="49ec6-170">Name des Einheitenmodells; kann mit ModelText identisch sein.</span><span class="sxs-lookup"><span data-stu-id="49ec6-170">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="49ec6-171">**Bstr**</span><span class="sxs-lookup"><span data-stu-id="49ec6-171">**BSTR**</span></span>            |
| <span data-ttu-id="49ec6-172">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="49ec6-172">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="49ec6-173">oPCR(Output Plug Control)-Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="49ec6-173">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="49ec6-174">Beispiel: 146 Quadlets.</span><span class="sxs-lookup"><span data-stu-id="49ec6-174">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="49ec6-175">**long**</span><span class="sxs-lookup"><span data-stu-id="49ec6-175">**long**</span></span>            |
| <span data-ttu-id="49ec6-176">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="49ec6-176">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="49ec6-177">oPCR-Datenrate.</span><span class="sxs-lookup"><span data-stu-id="49ec6-177">oPCR data rate.</span></span> <span data-ttu-id="49ec6-178">Beispiele: 0 (S100), 1 (S200) oder 2 (S400).</span><span class="sxs-lookup"><span data-stu-id="49ec6-178">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="49ec6-179">**long**</span><span class="sxs-lookup"><span data-stu-id="49ec6-179">**long**</span></span>            |
| <span data-ttu-id="49ec6-180">DeviceClassGUID</span><span class="sxs-lookup"><span data-stu-id="49ec6-180">DeviceClassGUID</span></span>     | <span data-ttu-id="49ec6-181">GUID, die den Gerätetreiber identifiziert.</span><span class="sxs-lookup"><span data-stu-id="49ec6-181">GUID that identifies the device driver.</span></span> <span data-ttu-id="49ec6-182">Für MSTape ist dieser Wert `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="49ec6-182">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="49ec6-183">Diese GUID ist in der Headerdatei Xprtdefs.h als MSTapeDeviceGUID definiert.</span><span class="sxs-lookup"><span data-stu-id="49ec6-183">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="49ec6-184">**Bstr**</span><span class="sxs-lookup"><span data-stu-id="49ec6-184">**BSTR**</span></span>            |
| <span data-ttu-id="49ec6-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49ec6-185">Description</span></span>         | <span data-ttu-id="49ec6-186">Eine Beschreibung des Geräts aus der INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="49ec6-186">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="49ec6-187">Diese Zeichenfolge enthält in der Regel den Markennamen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="49ec6-187">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="49ec6-188">**Bstr**</span><span class="sxs-lookup"><span data-stu-id="49ec6-188">**BSTR**</span></span>            |



 

<span data-ttu-id="49ec6-189">Die Geräte-ID ist eine 64-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="49ec6-189">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="49ec6-190">Das niedrige **DWORD** wird in der UniqueID Low-Eigenschaft gespeichert, und das \_ hohe **DWORD** wird in der UniqueID \_ High-Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="49ec6-190">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="49ec6-191">Weitere Informationen zu Gerätemonikern finden Sie unter [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="49ec6-191">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49ec6-192">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49ec6-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49ec6-193">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="49ec6-193">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="49ec6-194">Steuern eines DV-Dvd</span><span class="sxs-lookup"><span data-stu-id="49ec6-194">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



