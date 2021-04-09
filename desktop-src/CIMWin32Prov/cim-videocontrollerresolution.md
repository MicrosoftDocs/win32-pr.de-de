---
description: Die CIM \_ videocontrollerresolution-Klasse stellt die verschiedenen Video Modi dar, die von einem Videocontroller unterstützt werden können.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: CIM_VideoControllerResolution-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861683"
---
# <a name="cim_videocontrollerresolution-class"></a><span data-ttu-id="f223b-103">CIM \_ videocontrollerresolution-Klasse</span><span class="sxs-lookup"><span data-stu-id="f223b-103">CIM\_VideoControllerResolution class</span></span>

<span data-ttu-id="f223b-104">Die **CIM \_ videocontrollerresolution** -Klasse stellt die verschiedenen Video Modi dar, die von einem Videocontroller unterstützt werden können.</span><span class="sxs-lookup"><span data-stu-id="f223b-104">The **CIM\_VideoControllerResolution** class represents the various video modes that a video controller can support.</span></span> <span data-ttu-id="f223b-105">Videomodi werden durch die möglichen horizontalen und vertikalen Auflösungen, die Aktualisierungsrate, den Überprüfungs Modus und die Anzahl der Farbeinstellungen definiert, die von einem Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f223b-105">Video modes are defined by the possible horizontal and vertical resolutions, refresh rate, scan mode, and number of color settings supported by a controller.</span></span> <span data-ttu-id="f223b-106">Die tatsächlich verwendeten Auflösungen sind die Werte, die im [**CIM \_ Videocontroller**](cim-videocontroller.md) -Objekt angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="f223b-106">The actual resolutions in use are the values specified in the [**CIM\_VideoController**](cim-videocontroller.md) object.</span></span>

<span data-ttu-id="f223b-107">Hardware, die nicht mit dem Windows-Anzeigetreiber Modell (WDDM) kompatibel ist, gibt falsche Eigenschaftswerte für Instanzen dieser Klasse zurück.</span><span class="sxs-lookup"><span data-stu-id="f223b-107">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f223b-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f223b-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f223b-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f223b-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f223b-110">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f223b-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f223b-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f223b-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f223b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f223b-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="f223b-113">Member</span><span class="sxs-lookup"><span data-stu-id="f223b-113">Members</span></span>

<span data-ttu-id="f223b-114">Die **CIM \_ videocontrollerresolution** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f223b-114">The **CIM\_VideoControllerResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="f223b-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f223b-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f223b-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f223b-116">Properties</span></span>

<span data-ttu-id="f223b-117">Die **CIM \_ videocontrollerresolution** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f223b-117">The **CIM\_VideoControllerResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f223b-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f223b-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f223b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-121">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f223b-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f223b-122">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f223b-122">Short textual description of the current object.</span></span>

<span data-ttu-id="f223b-123">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f223b-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f223b-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f223b-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f223b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f223b-127">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f223b-127">Textual description of the current object.</span></span>

<span data-ttu-id="f223b-128">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f223b-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f223b-129">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="f223b-129">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f223b-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-132">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Happthorizontalresolution**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="f223b-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="f223b-133">Horizontale Auflösung in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f223b-133">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f223b-134">**Maxfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="f223b-134">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-135">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f223b-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-137">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Maxaktushrate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,7 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="f223b-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f223b-138">Maximale Aktualisierungsrate, wenn ein Bereich von Raten bei den angegebenen Auflösungen unterstützt wird (in Hertz).</span><span class="sxs-lookup"><span data-stu-id="f223b-138">Maximum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="f223b-139">**Minfreshshrate**</span><span class="sxs-lookup"><span data-stu-id="f223b-139">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-140">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f223b-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-142">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Minfreshshrate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,6 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="f223b-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f223b-143">Minimale Aktualisierungsrate, wenn ein Bereich von Raten bei den angegebenen Auflösungen unterstützt wird (in Hertz).</span><span class="sxs-lookup"><span data-stu-id="f223b-143">Minimum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="f223b-144">**Anzahl von Farben**</span><span class="sxs-lookup"><span data-stu-id="f223b-144">**NumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-145">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f223b-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-147">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentzahlofcolors**")</span><span class="sxs-lookup"><span data-stu-id="f223b-147">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span></span>
</dt> </dl>

<span data-ttu-id="f223b-148">Anzahl von Farben, die bei der aktuellen Auflösung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f223b-148">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="f223b-149">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f223b-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f223b-150">**RefreshRate**</span><span class="sxs-lookup"><span data-stu-id="f223b-150">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f223b-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-153">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**CurrentRefreshRate**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Hertz ")</span><span class="sxs-lookup"><span data-stu-id="f223b-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="f223b-154">Aktualisierungsrate in Hertz.</span><span class="sxs-lookup"><span data-stu-id="f223b-154">Refresh rate, in hertz.</span></span> <span data-ttu-id="f223b-155">Wenn ein Bereich von Raten unterstützt wird, verwenden Sie die Eigenschaften **minaktushrate** und **maxfreshshrate** , und legen Sie diese Eigenschaft auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="f223b-155">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f223b-156">**Scanmode**</span><span class="sxs-lookup"><span data-stu-id="f223b-156">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-157">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f223b-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-159">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentscanmode**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="f223b-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="f223b-160">Scanmodus, in dem der Controller arbeitet.</span><span class="sxs-lookup"><span data-stu-id="f223b-160">Scan mode at which the controller operates.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f223b-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f223b-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f223b-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="f223b-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f223b-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (3)</span><span class="sxs-lookup"><span data-stu-id="f223b-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="f223b-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Nicht-Interlacing-Vorgang** (4)</span><span class="sxs-lookup"><span data-stu-id="f223b-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f223b-165">Nicht Interlacing-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f223b-165">Noninterlaced operation</span></span>

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="f223b-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>Zeilen Sprung **Vorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="f223b-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f223b-167">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="f223b-167">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-168">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f223b-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-170">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f223b-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f223b-171">Eine ID, die als Teil des Schlüssels für die aktuelle Instanz dient.</span><span class="sxs-lookup"><span data-stu-id="f223b-171">An ID that serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="f223b-172">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="f223b-172">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f223b-173">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f223b-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f223b-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f223b-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f223b-175">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Videocontroller**](cim-videocontroller.md)".**Currentverticalresolution**"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF- \| Monitor Auflösungen \| 002,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="f223b-175">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="f223b-176">Vertikale Auflösung des Controllers in Pixel.</span><span class="sxs-lookup"><span data-stu-id="f223b-176">Controller's vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f223b-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f223b-177">Remarks</span></span>

<span data-ttu-id="f223b-178">WMI implementiert die **CIM \_ videocontrollerresolution** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="f223b-178">WMI implements the **CIM\_VideoControllerResolution** class.</span></span> <span data-ttu-id="f223b-179">Die **CIM \_ videocontrollerresolution** -Klasse ist eine dynamische Klasse.</span><span class="sxs-lookup"><span data-stu-id="f223b-179">The **CIM\_VideoControllerResolution** class is a dynamic class.</span></span>

<span data-ttu-id="f223b-180">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f223b-180">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f223b-181">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f223b-181">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="f223b-182">Beachten Sie, dass diese Klasse eine Basisklasse ist.</span><span class="sxs-lookup"><span data-stu-id="f223b-182">Note that this class is a base class.</span></span> <span data-ttu-id="f223b-183">Wenn Sie über WMI auf Ihren Videocontroller zugreifen möchten, können Sie stattdessen [**Win32 \_ Videocontroller**](win32-videocontroller.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f223b-183">If you are attempting to access your video controller through WMI, you may wish to use [**Win32\_VideoController**](win32-videocontroller.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="f223b-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f223b-184">Requirements</span></span>



| <span data-ttu-id="f223b-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f223b-185">Requirement</span></span> | <span data-ttu-id="f223b-186">Wert</span><span class="sxs-lookup"><span data-stu-id="f223b-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f223b-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f223b-187">Minimum supported client</span></span><br/> | <span data-ttu-id="f223b-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f223b-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f223b-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f223b-189">Minimum supported server</span></span><br/> | <span data-ttu-id="f223b-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f223b-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f223b-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="f223b-191">Namespace</span></span><br/>                | <span data-ttu-id="f223b-192">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f223b-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f223b-193">MOF</span><span class="sxs-lookup"><span data-stu-id="f223b-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f223b-194"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f223b-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f223b-195">DLL</span><span class="sxs-lookup"><span data-stu-id="f223b-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f223b-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f223b-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f223b-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f223b-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f223b-198">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="f223b-198">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

