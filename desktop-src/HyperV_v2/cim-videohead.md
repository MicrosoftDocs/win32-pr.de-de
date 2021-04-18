---
description: Stellt eine Kopfzeile eines CIM- \_ Displaycontroller-Objekts dar.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: CIM_VideoHead-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343832"
---
# <a name="cim_videohead-class"></a><span data-ttu-id="44433-103">CIM- \_ videoheadklasse</span><span class="sxs-lookup"><span data-stu-id="44433-103">CIM\_VideoHead class</span></span>

<span data-ttu-id="44433-104">Stellt eine Kopfzeile eines [**CIM- \_ Displaycontroller**](cim-displaycontroller.md) -Objekts dar.</span><span class="sxs-lookup"><span data-stu-id="44433-104">Represents one head of a [**CIM\_DisplayController**](cim-displaycontroller.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="44433-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44433-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="44433-106">Member</span><span class="sxs-lookup"><span data-stu-id="44433-106">Members</span></span>

<span data-ttu-id="44433-107">Die **CIM- \_ videoheadklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="44433-107">The **CIM\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="44433-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44433-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44433-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="44433-109">Properties</span></span>

<span data-ttu-id="44433-110">Die **CIM- \_ videoheadklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="44433-110">The **CIM\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44433-111">**Currentbitsperpixel**</span><span class="sxs-lookup"><span data-stu-id="44433-111">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-112">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44433-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44433-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-114">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,12 "), **Punit** (" Bit ")</span><span class="sxs-lookup"><span data-stu-id="44433-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.12"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="44433-115">Die Anzahl der Bits, die zum Anzeigen der einzelnen Pixel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44433-115">The number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="44433-116">**Ereignis Auflösung**</span><span class="sxs-lookup"><span data-stu-id="44433-116">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-117">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44433-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44433-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-119">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,11 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ videoheadresolution. HorizontalResolution "), **Punit** (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="44433-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.11"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.HorizontalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="44433-120">Die aktuelle Anzahl von horizontalen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="44433-120">The current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="44433-121">**Currentzahlofcolors**</span><span class="sxs-lookup"><span data-stu-id="44433-121">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-122">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="44433-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="44433-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-124">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ videoheadresolution. numofcolors")</span><span class="sxs-lookup"><span data-stu-id="44433-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.NumberOfColors")</span></span>
</dt> </dl>

<span data-ttu-id="44433-125">Die Anzahl von Farben, die bei der aktuellen Auflösung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="44433-125">The number of colors supported at the current resolution.</span></span>

</dd> <dt>

<span data-ttu-id="44433-126">**Currentzahlofcolumns**</span><span class="sxs-lookup"><span data-stu-id="44433-126">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-127">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44433-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44433-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-129">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,14 ")</span><span class="sxs-lookup"><span data-stu-id="44433-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.14")</span></span>
</dt> </dl>

<span data-ttu-id="44433-130">Im Zeichenmodus die Anzahl der Spalten für den Anzeige Controller. andernfalls "0".</span><span class="sxs-lookup"><span data-stu-id="44433-130">If in character mode, the number of columns for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="44433-131">**Currentnumofrows**</span><span class="sxs-lookup"><span data-stu-id="44433-131">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-132">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44433-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44433-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-134">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,13 ")</span><span class="sxs-lookup"><span data-stu-id="44433-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.13")</span></span>
</dt> </dl>

<span data-ttu-id="44433-135">Im Zeichenmodus die Anzahl der Zeilen für den Anzeige Controller. andernfalls "0".</span><span class="sxs-lookup"><span data-stu-id="44433-135">If in character mode, the number of rows for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="44433-136">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="44433-136">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-137">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44433-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44433-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-139">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,15 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ videoheadresolution. freshshrate "), **Punit** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="44433-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.15"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.RefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="44433-140">Die aktuelle Aktualisierungsrate des Anzeige Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="44433-140">The current refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="44433-141">**Currentscanmode**</span><span class="sxs-lookup"><span data-stu-id="44433-141">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-142">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44433-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44433-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,8 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ videohead**.**Othercurrentscanmode**, CIM \_ videoheadresolution. scanmode ")</span><span class="sxs-lookup"><span data-stu-id="44433-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**OtherCurrentScanMode**, CIM\_VideoHeadResolution.ScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="44433-145">Der aktuelle Scanmodus des Anzeige Controllers.</span><span class="sxs-lookup"><span data-stu-id="44433-145">The current scan mode of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44433-146">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="44433-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44433-147">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="44433-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="44433-148">**Nicht unterstützt** (2)</span><span class="sxs-lookup"><span data-stu-id="44433-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="44433-149">**Nicht-Interlacing-Vorgang** (3)</span><span class="sxs-lookup"><span data-stu-id="44433-149">**Non-Interlaced Operation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="44433-150">Zeilen Sprung **Vorgang** (4)</span><span class="sxs-lookup"><span data-stu-id="44433-150">**Interlaced Operation** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44433-151">**Currentverticalresolution**</span><span class="sxs-lookup"><span data-stu-id="44433-151">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44433-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44433-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-154">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixel"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,10 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ videoheadresolution. VerticalResolution "), **Punit** (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="44433-154">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.10"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.VerticalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="44433-155">Die aktuelle Anzahl vertikaler Pixel.</span><span class="sxs-lookup"><span data-stu-id="44433-155">The current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="44433-156">**Maxfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="44433-156">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44433-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44433-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-159">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,5 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ videoheadresolution. maxfreshshrate "), **Punit** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="44433-159">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MaxRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="44433-160">Die maximale Aktualisierungsrate des Anzeige Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="44433-160">The maximum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="44433-161">**Minfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="44433-161">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-162">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44433-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44433-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-164">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Video \| 004,4 "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ videoheadresolution. minfreshshrate "), **Punit** (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="44433-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MinRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="44433-165">Die minimale Aktualisierungsrate des Anzeige Controllers in Hertz.</span><span class="sxs-lookup"><span data-stu-id="44433-165">The minimum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="44433-166">**Othercurrentscanmode**</span><span class="sxs-lookup"><span data-stu-id="44433-166">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44433-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="44433-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44433-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="44433-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44433-169">Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ videohead**.**Currentscanmode**, CIM \_ videoheadresolution. otherscanmode ")</span><span class="sxs-lookup"><span data-stu-id="44433-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**CurrentScanMode**, CIM\_VideoHeadResolution.OtherScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="44433-170">Eine Beschreibung des aktuellen Überprüfungs Modus, wenn die **currentscanmode** -Eigenschaft den Wert "1" (sonstige) hat.</span><span class="sxs-lookup"><span data-stu-id="44433-170">A description of current scan mode when the **CurrentScanMode** property is "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44433-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44433-171">Requirements</span></span>



| <span data-ttu-id="44433-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44433-172">Requirement</span></span> | <span data-ttu-id="44433-173">Wert</span><span class="sxs-lookup"><span data-stu-id="44433-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44433-174">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44433-174">Minimum supported client</span></span><br/> | <span data-ttu-id="44433-175">Windows 8</span><span class="sxs-lookup"><span data-stu-id="44433-175">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="44433-176">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44433-176">Minimum supported server</span></span><br/> | <span data-ttu-id="44433-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44433-177">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="44433-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="44433-178">Namespace</span></span><br/>                | <span data-ttu-id="44433-179">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="44433-179">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="44433-180">MOF</span><span class="sxs-lookup"><span data-stu-id="44433-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44433-181"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="44433-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44433-182">DLL</span><span class="sxs-lookup"><span data-stu-id="44433-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44433-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44433-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="44433-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44433-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44433-185">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="44433-185">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

