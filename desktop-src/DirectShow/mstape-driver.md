---
description: Mstape-Treiber
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Mstape-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859985"
---
# <a name="mstape-driver"></a><span data-ttu-id="5edea-103">Mstape-Treiber</span><span class="sxs-lookup"><span data-stu-id="5edea-103">MSTape Driver</span></span>

<span data-ttu-id="5edea-104">Dieses Thema gilt für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="5edea-104">This topic applies to Windows XP or later.</span></span>

<span data-ttu-id="5edea-105">Der mstape-Treiber unterstützt D-VHS-und MPEG-Camcorder-Geräte.</span><span class="sxs-lookup"><span data-stu-id="5edea-105">The MSTape driver supports D-VHS and MPEG camcorder devices.</span></span> <span data-ttu-id="5edea-106">Sie wird für Anwendungen als [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="5edea-106">It is exposed to applications as the [WDM Video Capture](wdm-video-capture-filter.md) filter.</span></span> <span data-ttu-id="5edea-107">Seine Funktionalität ähnelt der von [msdv](msdv-driver.md), dem DV-Camcorder-Treiber:</span><span class="sxs-lookup"><span data-stu-id="5edea-107">Its functionality is similar to that of [MSDV](msdv-driver.md), the DV camcorder driver:</span></span>

-   <span data-ttu-id="5edea-108">Sie wird in den Filter Kategorien "Video Erfassungs Quellen" (CLSID \_ videoinputdebug) und "WDM Streaming Rendering Devices" (am \_ kscategory Rendering \_ ) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5edea-108">It appears in the "Video Capture Sources" (CLSID\_VideoInputDeviceCategory) and "WDM Streaming Rendering Devices" (AM\_KSCATEGORY\_RENDER) filter categories.</span></span>
-   <span data-ttu-id="5edea-109">Eine Anwendung kann eine Instanz des Filters mithilfe der [**ikreatedevenum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) -Schnittstelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="5edea-109">An application can create an instance of the filter using the [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) interface.</span></span>
-   <span data-ttu-id="5edea-110">Es verfügt über eine Ausgabe-PIN zum Erfassen und transportieren vom Gerät und eine Eingabe-PIN für den Transport zum Gerät.</span><span class="sxs-lookup"><span data-stu-id="5edea-110">It has an output pin for capture and transport from the device, and an input pin for transport to the device.</span></span> <span data-ttu-id="5edea-111">Es kann jeweils nur eine PIN verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="5edea-111">Only one pin can be connected at time.</span></span>

<span data-ttu-id="5edea-112">**Medientypen**</span><span class="sxs-lookup"><span data-stu-id="5edea-112">**Media Types**</span></span>

<span data-ttu-id="5edea-113">Die eingabepin unterstützt einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="5edea-113">The input pin supports one media type.</span></span>



|              |                                                            |
|--------------|------------------------------------------------------------|
| <span data-ttu-id="5edea-114">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="5edea-114">Major Type</span></span>   | <span data-ttu-id="5edea-115">MediaType- \_ Stream</span><span class="sxs-lookup"><span data-stu-id="5edea-115">MEDIATYPE\_Stream</span></span>                                          |
| <span data-ttu-id="5edea-116">Subtype</span><span class="sxs-lookup"><span data-stu-id="5edea-116">Subtype</span></span>      | <span data-ttu-id="5edea-117">Mediasubtype \_ MPEG2- \_ Transport \_ Stride</span><span class="sxs-lookup"><span data-stu-id="5edea-117">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span>                     |
| <span data-ttu-id="5edea-118">Stichprobengröße</span><span class="sxs-lookup"><span data-stu-id="5edea-118">Sample Size</span></span>  | <span data-ttu-id="5edea-119">192 x 256</span><span class="sxs-lookup"><span data-stu-id="5edea-119">192 x 256</span></span>                                                  |
| <span data-ttu-id="5edea-120">Format Block</span><span class="sxs-lookup"><span data-stu-id="5edea-120">Format Block</span></span> | [<span data-ttu-id="5edea-121">**MPEG2- \_ Transport \_ Stride**</span><span class="sxs-lookup"><span data-stu-id="5edea-121">**MPEG2\_TRANSPORT\_STRIDE**</span></span>](mpeg2-transport-stride.md) |



 

<span data-ttu-id="5edea-122">Die Ausgabepin unterstützt zwei Medientypen.</span><span class="sxs-lookup"><span data-stu-id="5edea-122">The output pin supports two media types.</span></span>



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="5edea-123">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="5edea-123">Major Type</span></span>   | <span data-ttu-id="5edea-124">MediaType- \_ Stream</span><span class="sxs-lookup"><span data-stu-id="5edea-124">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="5edea-125">Subtype</span><span class="sxs-lookup"><span data-stu-id="5edea-125">Subtype</span></span>      | <span data-ttu-id="5edea-126">Mediasubtype \_ MPEG2- \_ Transport \_ Stride</span><span class="sxs-lookup"><span data-stu-id="5edea-126">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="5edea-127">Stichprobengröße</span><span class="sxs-lookup"><span data-stu-id="5edea-127">Sample Size</span></span>  | <span data-ttu-id="5edea-128">192 x 256</span><span class="sxs-lookup"><span data-stu-id="5edea-128">192 x 256</span></span>                              |
| <span data-ttu-id="5edea-129">Format Block</span><span class="sxs-lookup"><span data-stu-id="5edea-129">Format Block</span></span> | <span data-ttu-id="5edea-130">MPEG2- \_ Transport \_ Stride</span><span class="sxs-lookup"><span data-stu-id="5edea-130">MPEG2\_TRANSPORT\_STRIDE</span></span>               |



 



|              |                                        |
|--------------|----------------------------------------|
| <span data-ttu-id="5edea-131">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="5edea-131">Major Type</span></span>   | <span data-ttu-id="5edea-132">MediaType- \_ Stream</span><span class="sxs-lookup"><span data-stu-id="5edea-132">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="5edea-133">Subtype</span><span class="sxs-lookup"><span data-stu-id="5edea-133">Subtype</span></span>      | <span data-ttu-id="5edea-134">Mediasubtype \_ MPEG2- \_ Transport \_ Stride</span><span class="sxs-lookup"><span data-stu-id="5edea-134">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="5edea-135">Stichprobengröße</span><span class="sxs-lookup"><span data-stu-id="5edea-135">Sample Size</span></span>  | <span data-ttu-id="5edea-136">188 x 256</span><span class="sxs-lookup"><span data-stu-id="5edea-136">188 x 256</span></span>                              |
| <span data-ttu-id="5edea-137">Format Block</span><span class="sxs-lookup"><span data-stu-id="5edea-137">Format Block</span></span> | <span data-ttu-id="5edea-138">**NULL**</span><span class="sxs-lookup"><span data-stu-id="5edea-138">**NULL**</span></span>                               |



 

<span data-ttu-id="5edea-139">**Geräteinformationen**</span><span class="sxs-lookup"><span data-stu-id="5edea-139">**Device Information**</span></span>

<span data-ttu-id="5edea-140">Der Treiber liest dynamisch Informationen aus dem Geräte Konfigurations-Rom.</span><span class="sxs-lookup"><span data-stu-id="5edea-140">The driver dynamically reads information from the device configuration ROM.</span></span> <span data-ttu-id="5edea-141">Diese Informationen können von der Anwendung abgerufen werden, indem der gerätermoniker an einen Eigenschaften Behälter gebunden und die **IPropertyBag:: Read** -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5edea-141">The application can retrieve this information by binding the device moniker to a property bag and calling the **IPropertyBag::Read** method.</span></span>



| <span data-ttu-id="5edea-142">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5edea-142">Property</span></span>            | <span data-ttu-id="5edea-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5edea-143">Description</span></span>                                                                                                                                                                         | <span data-ttu-id="5edea-144">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5edea-144">Data type</span></span>           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="5edea-145">UniqueId \_ niedrig</span><span class="sxs-lookup"><span data-stu-id="5edea-145">UniqueID\_Low</span></span>       | <span data-ttu-id="5edea-146">Eindeutige ID des Geräts (niedriges **DWORD**).</span><span class="sxs-lookup"><span data-stu-id="5edea-146">Unique ID of the device (low **DWORD**).</span></span>                                                                                                                                            | <span data-ttu-id="5edea-147">**Long** (VT \_ I4)</span><span class="sxs-lookup"><span data-stu-id="5edea-147">**long** (VT\_I4)</span></span>   |
| <span data-ttu-id="5edea-148">UniqueId \_ hoch</span><span class="sxs-lookup"><span data-stu-id="5edea-148">UniqueID\_High</span></span>      | <span data-ttu-id="5edea-149">Eindeutige ID des Geräts (High **DWORD**)</span><span class="sxs-lookup"><span data-stu-id="5edea-149">Unique ID of the device (high **DWORD**)</span></span>                                                                                                                                            | <span data-ttu-id="5edea-150">**long**</span><span class="sxs-lookup"><span data-stu-id="5edea-150">**long**</span></span>            |
| <span data-ttu-id="5edea-151">VendorID</span><span class="sxs-lookup"><span data-stu-id="5edea-151">VendorID</span></span>            | <span data-ttu-id="5edea-152">Anbieter-ID.</span><span class="sxs-lookup"><span data-stu-id="5edea-152">Vendor ID.</span></span>                                                                                                                                                                          | <span data-ttu-id="5edea-153">**long**</span><span class="sxs-lookup"><span data-stu-id="5edea-153">**long**</span></span>            |
| <span data-ttu-id="5edea-154">ModelID</span><span class="sxs-lookup"><span data-stu-id="5edea-154">ModelID</span></span>             | <span data-ttu-id="5edea-155">Modell-ID</span><span class="sxs-lookup"><span data-stu-id="5edea-155">Model ID.</span></span>                                                                                                                                                                           | <span data-ttu-id="5edea-156">**long**</span><span class="sxs-lookup"><span data-stu-id="5edea-156">**long**</span></span>            |
| <span data-ttu-id="5edea-157">Vendortext</span><span class="sxs-lookup"><span data-stu-id="5edea-157">VendorText</span></span>          | <span data-ttu-id="5edea-158">Der Name des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="5edea-158">Vendor name.</span></span>                                                                                                                                                                        | <span data-ttu-id="5edea-159">**BSTR** (VT \_ BSTR)</span><span class="sxs-lookup"><span data-stu-id="5edea-159">**BSTR** (VT\_BSTR)</span></span> |
| <span data-ttu-id="5edea-160">Modeltext</span><span class="sxs-lookup"><span data-stu-id="5edea-160">ModelText</span></span>           | <span data-ttu-id="5edea-161">Gerätemodell Name.</span><span class="sxs-lookup"><span data-stu-id="5edea-161">Device model name.</span></span>                                                                                                                                                                  | <span data-ttu-id="5edea-162">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="5edea-162">**BSTR**</span></span>            |
| <span data-ttu-id="5edea-163">Unitmodeltext</span><span class="sxs-lookup"><span data-stu-id="5edea-163">UnitModelText</span></span>       | <span data-ttu-id="5edea-164">Name des Einheitsmodells; kann mit modeltext identisch sein.</span><span class="sxs-lookup"><span data-stu-id="5edea-164">Unit model name; may be the same as ModelText.</span></span>                                                                                                                                      | <span data-ttu-id="5edea-165">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="5edea-165">**BSTR**</span></span>            |
| <span data-ttu-id="5edea-166">DeviceOPcr0Payload</span><span class="sxs-lookup"><span data-stu-id="5edea-166">DeviceOPcr0Payload</span></span>  | <span data-ttu-id="5edea-167">opcr-Nutzlast (Ausgabe-Plug-in).</span><span class="sxs-lookup"><span data-stu-id="5edea-167">oPCR (Output Plug Control) payload.</span></span> <span data-ttu-id="5edea-168">Beispiel: 146 quadlets.</span><span class="sxs-lookup"><span data-stu-id="5edea-168">Example: 146 quadlets.</span></span>                                                                                                                          | <span data-ttu-id="5edea-169">**long**</span><span class="sxs-lookup"><span data-stu-id="5edea-169">**long**</span></span>            |
| <span data-ttu-id="5edea-170">DeviceOPcr0DataRate</span><span class="sxs-lookup"><span data-stu-id="5edea-170">DeviceOPcr0DataRate</span></span> | <span data-ttu-id="5edea-171">opcr-Datenrate.</span><span class="sxs-lookup"><span data-stu-id="5edea-171">oPCR data rate.</span></span> <span data-ttu-id="5edea-172">Beispiele: 0 (S100), 1 (S200) oder 2 (S400).</span><span class="sxs-lookup"><span data-stu-id="5edea-172">Examples: 0 (S100), 1 (S200), or 2 (S400).</span></span>                                                                                                                          | <span data-ttu-id="5edea-173">**long**</span><span class="sxs-lookup"><span data-stu-id="5edea-173">**long**</span></span>            |
| <span data-ttu-id="5edea-174">Geräte-ID</span><span class="sxs-lookup"><span data-stu-id="5edea-174">DeviceClassGUID</span></span>     | <span data-ttu-id="5edea-175">GUID, die den Gerätetreiber identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5edea-175">GUID that identifies the device driver.</span></span> <span data-ttu-id="5edea-176">Für mstape ist dieser Wert `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` .</span><span class="sxs-lookup"><span data-stu-id="5edea-176">For MSTape, this value is `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}`.</span></span> <span data-ttu-id="5edea-177">Diese GUID wird in der Header Datei xprtdefs. h als mstapedeviceguid definiert.</span><span class="sxs-lookup"><span data-stu-id="5edea-177">This GUID is defined as MSTapeDeviceGUID in the header file Xprtdefs.h.</span></span> | <span data-ttu-id="5edea-178">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="5edea-178">**BSTR**</span></span>            |
| <span data-ttu-id="5edea-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5edea-179">Description</span></span>         | <span data-ttu-id="5edea-180">Eine Beschreibung des Geräts aus der INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="5edea-180">A description of the device, taken from the INF file.</span></span> <span data-ttu-id="5edea-181">Diese Zeichenfolge enthält normalerweise den Markennamen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="5edea-181">This string usually contains the brand name of the device.</span></span>                                                                    | <span data-ttu-id="5edea-182">**BSTR**</span><span class="sxs-lookup"><span data-stu-id="5edea-182">**BSTR**</span></span>            |



 

<span data-ttu-id="5edea-183">Die Geräte-ID ist eine 64-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="5edea-183">The device ID is a 64-bit integer.</span></span> <span data-ttu-id="5edea-184">Das niedrige **DWORD** wird in der UniqueId \_ Low-Eigenschaft gespeichert, und das High **DWORD** wird in der UniqueId \_ High-Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5edea-184">The low **DWORD** is stored in the UniqueID\_Low property, and the high **DWORD** is stored in the UniqueID\_High property.</span></span>

<span data-ttu-id="5edea-185">Weitere Informationen zu gerätermonikern finden [Sie unter Verwenden des System Geräte Enumerators](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="5edea-185">For more information about device monikers, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5edea-186">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5edea-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5edea-187">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="5edea-187">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="5edea-188">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="5edea-188">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



