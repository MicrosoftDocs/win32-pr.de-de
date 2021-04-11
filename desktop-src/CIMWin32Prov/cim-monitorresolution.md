---
description: Die CIM- \_ monitorresolution-Klasse stellt die Beziehung zwischen horizontaler und vertikaler Auflösung und der Aktualisierungsrate und dem Überprüfungs Modus für einen Desktop Monitor dar. Werte werden im Videocontroller Objekt angegeben.
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: CIM_MonitorResolution-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b359a2e7eccf31b32aced8a2ea9f85fb6dc48b7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958472"
---
# <a name="cim_monitorresolution-class"></a><span data-ttu-id="841a0-104">CIM- \_ monitorresolution-Klasse</span><span class="sxs-lookup"><span data-stu-id="841a0-104">CIM\_MonitorResolution class</span></span>

<span data-ttu-id="841a0-105">Die **CIM- \_ monitorresolution** -Klasse stellt die Beziehung zwischen horizontaler und vertikaler Auflösung und der Aktualisierungsrate und dem Überprüfungs Modus für einen Desktop Monitor dar.</span><span class="sxs-lookup"><span data-stu-id="841a0-105">The **CIM\_MonitorResolution** class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="841a0-106">Werte werden im Videocontroller Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="841a0-106">Values are specified in the video controller object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="841a0-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="841a0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="841a0-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="841a0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="841a0-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="841a0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="841a0-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="841a0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="841a0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="841a0-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="841a0-112">Member</span><span class="sxs-lookup"><span data-stu-id="841a0-112">Members</span></span>

<span data-ttu-id="841a0-113">Die **CIM- \_ monitorresolution** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="841a0-113">The **CIM\_MonitorResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="841a0-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="841a0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="841a0-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="841a0-115">Properties</span></span>

<span data-ttu-id="841a0-116">Die **CIM- \_ monitorresolution** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="841a0-116">The **CIM\_MonitorResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="841a0-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="841a0-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="841a0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841a0-120">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="841a0-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="841a0-121">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="841a0-121">Short textual description of the current object.</span></span>

<span data-ttu-id="841a0-122">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="841a0-122">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="841a0-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="841a0-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="841a0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="841a0-126">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="841a0-126">Textual description of the current object.</span></span>

<span data-ttu-id="841a0-127">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="841a0-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="841a0-128">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="841a0-128">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="841a0-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841a0-131">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Happthorizontalresolution**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="841a0-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="841a0-132">Horizontale Auflösung des Monitors in Pixel.</span><span class="sxs-lookup"><span data-stu-id="841a0-132">Monitor's horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="841a0-133">**Maxfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="841a0-133">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="841a0-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841a0-136">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Maxaktushrate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="841a0-136">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="841a0-137">Die maximale Aktualisierungsrate des Monitors in Hertz, wenn ein Bereich von Raten bei den angegebenen Auflösungen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="841a0-137">Monitor's maximum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="841a0-138">**Minfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="841a0-138">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-139">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="841a0-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841a0-141">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Minfreshshrate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,6 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="841a0-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="841a0-142">Die minimale Aktualisierungsrate des Monitors in Hertz, wenn ein Bereich von Raten bei den angegebenen Auflösungen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="841a0-142">Monitor's minimum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="841a0-143">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="841a0-143">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-144">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="841a0-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841a0-146">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**CurrentRefreshRate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="841a0-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="841a0-147">Die Aktualisierungsrate des Monitors in Hertz.</span><span class="sxs-lookup"><span data-stu-id="841a0-147">Monitor's refresh rate, in hertz.</span></span> <span data-ttu-id="841a0-148">Wenn ein Bereich von Raten unterstützt wird, verwenden Sie die Eigenschaften **minaktushrate** und **maxfreshshrate** , und legen Sie diese Eigenschaft auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="841a0-148">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="841a0-149">**Scanmode**</span><span class="sxs-lookup"><span data-stu-id="841a0-149">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-150">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="841a0-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841a0-152">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentscanmode**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="841a0-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="841a0-153">Der Scanmodus, den der Monitor verwendet.</span><span class="sxs-lookup"><span data-stu-id="841a0-153">Scan mode that the monitor uses.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="841a0-154">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="841a0-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="841a0-155">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="841a0-155">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="841a0-156">**Nicht unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="841a0-156">**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="841a0-157">**Nicht-Interlacing-Vorgang** (4)</span><span class="sxs-lookup"><span data-stu-id="841a0-157">**Non-Interlaced Operation** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="841a0-158">Zeilen Sprung **Vorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="841a0-158">**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="841a0-159">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="841a0-159">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="841a0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841a0-162">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="841a0-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="841a0-163">Dient als Teil des Schlüssels für die aktuelle-Instanz.</span><span class="sxs-lookup"><span data-stu-id="841a0-163">Serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="841a0-164">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="841a0-164">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841a0-165">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="841a0-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="841a0-166">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="841a0-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841a0-167">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentverticalresolution**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="841a0-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="841a0-168">Vertikale Auflösung des Monitors in Pixel.</span><span class="sxs-lookup"><span data-stu-id="841a0-168">Monitor's vertical resolution in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="841a0-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="841a0-169">Remarks</span></span>

<span data-ttu-id="841a0-170">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="841a0-170">WMI does not implement this class.</span></span>

<span data-ttu-id="841a0-171">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="841a0-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="841a0-172">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="841a0-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="841a0-173">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="841a0-173">Requirements</span></span>



| <span data-ttu-id="841a0-174">Anforderung</span><span class="sxs-lookup"><span data-stu-id="841a0-174">Requirement</span></span> | <span data-ttu-id="841a0-175">Wert</span><span class="sxs-lookup"><span data-stu-id="841a0-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="841a0-176">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="841a0-176">Minimum supported client</span></span><br/> | <span data-ttu-id="841a0-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="841a0-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="841a0-178">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="841a0-178">Minimum supported server</span></span><br/> | <span data-ttu-id="841a0-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="841a0-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="841a0-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="841a0-180">Namespace</span></span><br/>                | <span data-ttu-id="841a0-181">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="841a0-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="841a0-182">MOF</span><span class="sxs-lookup"><span data-stu-id="841a0-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="841a0-183"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="841a0-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="841a0-184">DLL</span><span class="sxs-lookup"><span data-stu-id="841a0-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="841a0-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="841a0-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="841a0-186">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="841a0-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841a0-187">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="841a0-187">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

