---
description: Stellt einen Anzeige Controller dar.
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: CIM_DisplayController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357402"
---
# <a name="cim_displaycontroller-class"></a><span data-ttu-id="ec397-103">CIM \_ Displaycontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="ec397-103">CIM\_DisplayController class</span></span>

<span data-ttu-id="ec397-104">Stellt einen Anzeige Controller dar.</span><span class="sxs-lookup"><span data-stu-id="ec397-104">Represents a display controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec397-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec397-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="ec397-106">Member</span><span class="sxs-lookup"><span data-stu-id="ec397-106">Members</span></span>

<span data-ttu-id="ec397-107">Die **CIM \_ Displaycontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ec397-107">The **CIM\_DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="ec397-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ec397-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec397-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ec397-109">Properties</span></span>

<span data-ttu-id="ec397-110">Die **CIM \_ Displaycontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ec397-110">The **CIM\_DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec397-111">**Beschleuniger Funktionen**</span><span class="sxs-lookup"><span data-stu-id="ec397-111">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-112">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ec397-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ec397-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec397-114">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Displaycontroller**.**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="ec397-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ec397-115">Die Grafik-und 3D-Funktionen des Anzeige Controllers.</span><span class="sxs-lookup"><span data-stu-id="ec397-115">The graphics and 3D capabilities of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec397-116">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ec397-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ec397-117">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ec397-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="ec397-118">**Grafikbeschleuniger** (2)</span><span class="sxs-lookup"><span data-stu-id="ec397-118">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="ec397-119">**3D-Accelerator** (3)</span><span class="sxs-lookup"><span data-stu-id="ec397-119">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

<span data-ttu-id="ec397-120">**PCI-schnelles Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="ec397-120">**PCI Fast Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

<span data-ttu-id="ec397-121">**Unterstützung für Multimonitor** (5)</span><span class="sxs-lookup"><span data-stu-id="ec397-121">**MultiMonitor Support** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

<span data-ttu-id="ec397-122">**PCI-Mastering** (6)</span><span class="sxs-lookup"><span data-stu-id="ec397-122">**PCI Mastering** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

<span data-ttu-id="ec397-123">**Unterstützung für den zweiten Monochrom-Adapter** (7)</span><span class="sxs-lookup"><span data-stu-id="ec397-123">**Second Monochrome Adapter Support** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

<span data-ttu-id="ec397-124">**Unterstützung für große Speicheradressen** (8)</span><span class="sxs-lookup"><span data-stu-id="ec397-124">**Large Memory Address Support** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec397-125">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="ec397-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-126">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ec397-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ec397-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec397-128">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Displaycontroller**.**Acceleratorfunktionen**")</span><span class="sxs-lookup"><span data-stu-id="ec397-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ec397-129">Ausführliche Erläuterungen zu den Funktionen von Video-Accelerator des **acceleratorfunktionalitäten** -Arrays.</span><span class="sxs-lookup"><span data-stu-id="ec397-129">Detailed explanations for video accelerator features of the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="ec397-130">Die Elemente in diesem Array entsprechen den Array Elementen in **acceleratorfunktionen**.</span><span class="sxs-lookup"><span data-stu-id="ec397-130">The items in this array correspond to the array items in **AcceleratorCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="ec397-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec397-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec397-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec397-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec397-134">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,18 ")</span><span class="sxs-lookup"><span data-stu-id="ec397-134">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.18")</span></span>
</dt> </dl>

<span data-ttu-id="ec397-135">Eine Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ec397-135">A text description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="ec397-136">**Maxmemorysupported**</span><span class="sxs-lookup"><span data-stu-id="ec397-136">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec397-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec397-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec397-139">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **Punit** ("Byte")</span><span class="sxs-lookup"><span data-stu-id="ec397-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="ec397-140">Die maximal unterstützte Arbeitsspeicher Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ec397-140">The maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ec397-141">**Anzahl der videopages**</span><span class="sxs-lookup"><span data-stu-id="ec397-141">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec397-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec397-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec397-144">Die Anzahl der unterstützten Videoseiten anhand der aktuellen Auflösungen und des verfügbaren Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="ec397-144">The number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="ec397-145">**Othervideoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="ec397-145">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec397-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec397-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec397-148">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Displaycontroller**".**Videoarchitecture**")</span><span class="sxs-lookup"><span data-stu-id="ec397-148">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoArchitecture**")</span></span>
</dt> </dl>

<span data-ttu-id="ec397-149">Eine Beschreibung des Video Architektur Typs, wenn die **Video Architecture** -Eigenschaft "1" (sonstige) enthält.</span><span class="sxs-lookup"><span data-stu-id="ec397-149">A description of the video architecture type when the **VideoArchitecture** property contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="ec397-150">**Othervideomemorytype**</span><span class="sxs-lookup"><span data-stu-id="ec397-150">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec397-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec397-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec397-153">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Displaycontroller**".**Videomemorytype**")</span><span class="sxs-lookup"><span data-stu-id="ec397-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="ec397-154">Der Typ des Video Speichers, wenn die **videomemorytype** -Eigenschaft "1" (sonstige) ist.</span><span class="sxs-lookup"><span data-stu-id="ec397-154">The video memory type when the **VideoMemoryType** property is "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="ec397-155">**Videoarchitecture**</span><span class="sxs-lookup"><span data-stu-id="ec397-155">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-156">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec397-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec397-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec397-158">Die Anzeige Controller-Video Architektur, mit der das Videosignal generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ec397-158">The display controllers video architecture used to generate the video signal.</span></span> <span data-ttu-id="ec397-159">In der Regel generiert ein dedizierter Videoprozessor das Videosignal entsprechend der angegebenen Architektur.</span><span class="sxs-lookup"><span data-stu-id="ec397-159">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="ec397-160">Die Architektur gibt die maximale Auflösungs Funktion des Anzeige Controllers an.</span><span class="sxs-lookup"><span data-stu-id="ec397-160">The architecture indicates of the maximum resolution capability of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec397-161">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ec397-161">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ec397-162">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ec397-162">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="ec397-163">**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="ec397-163">**CGA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="ec397-164">**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="ec397-164">**EGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="ec397-165">**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="ec397-165">**VGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="ec397-166">**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="ec397-166">**SVGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="ec397-167">**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="ec397-167">**MDA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="ec397-168">**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="ec397-168">**HGC** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="ec397-169">**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="ec397-169">**MCGA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="ec397-170">**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="ec397-170">**8514A** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="ec397-171">**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="ec397-171">**XGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="ec397-172">**Linearer Rahmen Puffer** (11)</span><span class="sxs-lookup"><span data-stu-id="ec397-172">**Linear Frame Buffer** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="ec397-173">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="ec397-173">**PC-98** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ec397-174">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ec397-174">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ec397-175">**Anbieter reserviert** (0X8000..)</span><span class="sxs-lookup"><span data-stu-id="ec397-175">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec397-176">**Videomemorytype**</span><span class="sxs-lookup"><span data-stu-id="ec397-176">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-177">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec397-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec397-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec397-179">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,6 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Displaycontroller**".**Othervideomemorytype**")</span><span class="sxs-lookup"><span data-stu-id="ec397-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.6"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**OtherVideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="ec397-180">Der Typ des Video Speichers.</span><span class="sxs-lookup"><span data-stu-id="ec397-180">The type of video memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ec397-181">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ec397-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ec397-182">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ec397-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="ec397-183">**VRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="ec397-183">**VRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="ec397-184">**DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="ec397-184">**DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="ec397-185">**SRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="ec397-185">**SRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="ec397-186">**Wram** (5)</span><span class="sxs-lookup"><span data-stu-id="ec397-186">**WRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="ec397-187">**EDO RAM** (6)</span><span class="sxs-lookup"><span data-stu-id="ec397-187">**EDO RAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="ec397-188">**Burst synchroner DRAM** (7)</span><span class="sxs-lookup"><span data-stu-id="ec397-188">**Burst Synchronous DRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="ec397-189">**Pipelined Burst-SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="ec397-189">**Pipelined Burst SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="ec397-190">**CDRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="ec397-190">**CDRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="ec397-191">**3dram** (10)</span><span class="sxs-lookup"><span data-stu-id="ec397-191">**3DRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="ec397-192">**SDRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="ec397-192">**SDRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="ec397-193">**SGRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="ec397-193">**SGRAM** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec397-194">**Videoprocessor**</span><span class="sxs-lookup"><span data-stu-id="ec397-194">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec397-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ec397-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec397-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ec397-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec397-197">Eine Textbeschreibung des Video Prozessors/-Controllers.</span><span class="sxs-lookup"><span data-stu-id="ec397-197">A text description of the video processor/controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec397-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec397-198">Requirements</span></span>



| <span data-ttu-id="ec397-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec397-199">Requirement</span></span> | <span data-ttu-id="ec397-200">Wert</span><span class="sxs-lookup"><span data-stu-id="ec397-200">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec397-201">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec397-201">Minimum supported client</span></span><br/> | <span data-ttu-id="ec397-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ec397-202">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ec397-203">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec397-203">Minimum supported server</span></span><br/> | <span data-ttu-id="ec397-204">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec397-204">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ec397-205">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec397-205">Namespace</span></span><br/>                | <span data-ttu-id="ec397-206">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ec397-206">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec397-207">MOF</span><span class="sxs-lookup"><span data-stu-id="ec397-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec397-208"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ec397-208"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec397-209">DLL</span><span class="sxs-lookup"><span data-stu-id="ec397-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec397-210"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec397-210"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec397-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec397-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec397-212">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="ec397-212">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

