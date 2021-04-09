---
description: Die Win32 \_ desktopwmi-Klasse stellt die allgemeinen Merkmale des Desktops eines Benutzers dar. Die Eigenschaften dieser Klasse können vom Benutzer geändert werden, um den Desktop anzupassen.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Win32_Desktop-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861719"
---
# <a name="win32_desktop-class"></a><span data-ttu-id="64441-104">Win32 \_ -Desktop Klasse</span><span class="sxs-lookup"><span data-stu-id="64441-104">Win32\_Desktop class</span></span>

<span data-ttu-id="64441-105">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) für den **Win32 \_ -Desktop** stellt die allgemeinen Merkmale des Desktops eines Benutzers dar.</span><span class="sxs-lookup"><span data-stu-id="64441-105">The **Win32\_Desktop**[WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the common characteristics of a user's desktop.</span></span> <span data-ttu-id="64441-106">Die Eigenschaften dieser Klasse können vom Benutzer geändert werden, um den Desktop anzupassen.</span><span class="sxs-lookup"><span data-stu-id="64441-106">The properties of this class can be modified by the user to customize the desktop.</span></span>

<span data-ttu-id="64441-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64441-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="64441-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="64441-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="64441-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="64441-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a><span data-ttu-id="64441-110">Member</span><span class="sxs-lookup"><span data-stu-id="64441-110">Members</span></span>

<span data-ttu-id="64441-111">Die **Win32 \_ -Desktop** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="64441-111">The **Win32\_Desktop** class has these types of members:</span></span>

-   [<span data-ttu-id="64441-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64441-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64441-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64441-113">Properties</span></span>

<span data-ttu-id="64441-114">Die **Win32 \_ -Desktop** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64441-114">The **Win32\_Desktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64441-115">**Rahmenbreite**</span><span class="sxs-lookup"><span data-stu-id="64441-115">**BorderWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-116">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64441-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64441-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-118">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -Systemsteuerung \\ \\ Desktop \\ \\ WindowMetrics \| BorderWidth ")</span><span class="sxs-lookup"><span data-stu-id="64441-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|BorderWidth")</span></span>
</dt> </dl>

<span data-ttu-id="64441-119">Breite der Rahmen um alle Fenster mit anpassbaren Rändern.</span><span class="sxs-lookup"><span data-stu-id="64441-119">Width of the borders around all windows with adjustable borders.</span></span>

<span data-ttu-id="64441-120">Beispiel: 3</span><span class="sxs-lookup"><span data-stu-id="64441-120">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="64441-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="64441-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="64441-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64441-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-124">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="64441-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="64441-125">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="64441-125">Short textual description of the current object.</span></span>

<span data-ttu-id="64441-126">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="64441-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="64441-127">**Coolswitch**</span><span class="sxs-lookup"><span data-stu-id="64441-127">**CoolSwitch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="64441-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64441-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-130">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Control Panel \\ \\ Desktop \| coolswitch")</span><span class="sxs-lookup"><span data-stu-id="64441-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CoolSwitch")</span></span>
</dt> </dl>

<span data-ttu-id="64441-131">Der schnelle Aufgaben Wechsel ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="64441-131">Fast task switching is turned on.</span></span> <span data-ttu-id="64441-132">Der schnelle Aufgaben Wechsel ermöglicht es dem Benutzer, mithilfe der Tastenkombination **Alt + Tab** zwischen Fenstern zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="64441-132">Fast task switching allows the user to switch between windows using the **ALT+TAB** keyboard combination.</span></span>

</dd> <dt>

<span data-ttu-id="64441-133">**Cursor-Blinkrate**</span><span class="sxs-lookup"><span data-stu-id="64441-133">**CursorBlinkRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64441-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64441-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-136">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Control Panel \\ \\ Desktop \| geschweisorblinkrate"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Millisekunden")</span><span class="sxs-lookup"><span data-stu-id="64441-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CursorBlinkRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="64441-137">Zeitspanne zwischen aufeinander folgenden Cursor-Blinks.</span><span class="sxs-lookup"><span data-stu-id="64441-137">Length of time between successive cursor blinks.</span></span>

<span data-ttu-id="64441-138">Beispiel: 530</span><span class="sxs-lookup"><span data-stu-id="64441-138">Example: 530</span></span>

</dd> <dt>

<span data-ttu-id="64441-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64441-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="64441-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64441-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64441-142">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="64441-142">Textual description of the current object.</span></span>

<span data-ttu-id="64441-143">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="64441-143">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="64441-144">**DragFullWindows**</span><span class="sxs-lookup"><span data-stu-id="64441-144">**DragFullWindows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-145">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="64441-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64441-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-147">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Control Panel \\ \\ Desktop \| DragFullWindows")</span><span class="sxs-lookup"><span data-stu-id="64441-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|DragFullWindows")</span></span>
</dt> </dl>

<span data-ttu-id="64441-148">Der Inhalt eines Fensters wird angezeigt, wenn ein Benutzer das Fenster verschiebt.</span><span class="sxs-lookup"><span data-stu-id="64441-148">Contents of a window are shown when a user moves the window.</span></span>

</dd> <dt>

<span data-ttu-id="64441-149">**Gridgranularität**</span><span class="sxs-lookup"><span data-stu-id="64441-149">**GridGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-150">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64441-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64441-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-152">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| Control Panel \\ \\ Desktop- \| Granularität"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 Pixel")</span><span class="sxs-lookup"><span data-stu-id="64441-152">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|GridGranularity"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span></span>
</dt> </dl>

<span data-ttu-id="64441-153">Abstand des Rasters, an das Windows auf dem Desktop gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="64441-153">Spacing of the grid that windows are bound to on the desktop.</span></span> <span data-ttu-id="64441-154">Dies erleichtert das Organisieren von Fenstern.</span><span class="sxs-lookup"><span data-stu-id="64441-154">This makes organizing windows easier.</span></span> <span data-ttu-id="64441-155">Der Abstand ist in der Regel ausreichend, dass der Benutzer ihn nicht bemerkt.</span><span class="sxs-lookup"><span data-stu-id="64441-155">The spacing is usually fine enough that the user does not notice it.</span></span>

<span data-ttu-id="64441-156">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="64441-156">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="64441-157">**IconSpacing**</span><span class="sxs-lookup"><span data-stu-id="64441-157">**IconSpacing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-158">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64441-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64441-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-160">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Pixel ")</span><span class="sxs-lookup"><span data-stu-id="64441-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="64441-161">Abstand zwischen Symbolen.</span><span class="sxs-lookup"><span data-stu-id="64441-161">Spacing between icons.</span></span>

<span data-ttu-id="64441-162">Beispiel: 75</span><span class="sxs-lookup"><span data-stu-id="64441-162">Example: 75</span></span>

</dd> <dt>

<span data-ttu-id="64441-163">**Icontitlefakename**</span><span class="sxs-lookup"><span data-stu-id="64441-163">**IconTitleFaceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="64441-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64441-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-166">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \\ \\ WindowMetrics \| IconFont ")</span><span class="sxs-lookup"><span data-stu-id="64441-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconFont")</span></span>
</dt> </dl>

<span data-ttu-id="64441-167">Schriftart, die für die Namen der Symbole verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64441-167">Font used for the names of the icons.</span></span>

<span data-ttu-id="64441-168">Beispiel: "MS San Serif"</span><span class="sxs-lookup"><span data-stu-id="64441-168">Example: "MS San Serif"</span></span>

</dd> <dt>

<span data-ttu-id="64441-169">**IconTitleSize**</span><span class="sxs-lookup"><span data-stu-id="64441-169">**IconTitleSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64441-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64441-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-172">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Font and Text Structures \| [**logfontw**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfheight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Point")</span><span class="sxs-lookup"><span data-stu-id="64441-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Font and Text Structures\|[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)\|lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")</span></span>
</dt> </dl>

<span data-ttu-id="64441-173">Schriftart Größe des Symbols.</span><span class="sxs-lookup"><span data-stu-id="64441-173">Icon font size.</span></span>

<span data-ttu-id="64441-174">Beispiel: 9</span><span class="sxs-lookup"><span data-stu-id="64441-174">Example: 9</span></span>

</dd> <dt>

<span data-ttu-id="64441-175">**IconTitleWrap**</span><span class="sxs-lookup"><span data-stu-id="64441-175">**IconTitleWrap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-176">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="64441-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64441-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-178">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap ")</span><span class="sxs-lookup"><span data-stu-id="64441-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconTitleWrap")</span></span>
</dt> </dl>

<span data-ttu-id="64441-179">Der Titeltext des Symbols wird in die nächste Zeile umschlossen.</span><span class="sxs-lookup"><span data-stu-id="64441-179">Icon's title text wraps to the next line.</span></span>

</dd> <dt>

<span data-ttu-id="64441-180">**Name**</span><span class="sxs-lookup"><span data-stu-id="64441-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="64441-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64441-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-183">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="64441-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="64441-184">Der Name, der das aktuelle Desktop Profil identifiziert.</span><span class="sxs-lookup"><span data-stu-id="64441-184">Name that identifies the current desktop profile.</span></span>

<span data-ttu-id="64441-185">Beispiel: "mainprof"</span><span class="sxs-lookup"><span data-stu-id="64441-185">Example: "MainProf"</span></span>

</dd> <dt>

<span data-ttu-id="64441-186">**Muster**</span><span class="sxs-lookup"><span data-stu-id="64441-186">**Pattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="64441-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64441-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-189">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -System Steuerungs \\ \\ Desktop- \| Muster ")</span><span class="sxs-lookup"><span data-stu-id="64441-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Pattern")</span></span>
</dt> </dl>

<span data-ttu-id="64441-190">Der Name des Musters, das als Hintergrund für den Desktop verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64441-190">Name of the pattern used as the background for the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="64441-191">**ScreenSaverActive**</span><span class="sxs-lookup"><span data-stu-id="64441-191">**ScreenSaverActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-192">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="64441-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64441-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-194">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -Systemsteuerung \\ \\ Desktop \| screensaveactive ")</span><span class="sxs-lookup"><span data-stu-id="64441-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveActive")</span></span>
</dt> </dl>

<span data-ttu-id="64441-195">Der Bildschirmschoner ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="64441-195">Screen saver is active.</span></span>

</dd> <dt>

<span data-ttu-id="64441-196">**Screensaverausführ Bare Datei**</span><span class="sxs-lookup"><span data-stu-id="64441-196">**ScreenSaverExecutable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="64441-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64441-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-199">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -Systemsteuerung \\ \\ Desktop \|SCRNSAVE.EXE ")</span><span class="sxs-lookup"><span data-stu-id="64441-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|SCRNSAVE.EXE")</span></span>
</dt> </dl>

<span data-ttu-id="64441-200">Der Name der aktuellen ausführbaren Datei für den Bildschirmschoner.</span><span class="sxs-lookup"><span data-stu-id="64441-200">Name of the current screen saver executable file.</span></span>

<span data-ttu-id="64441-201">Beispiel: "Login. SCR</span><span class="sxs-lookup"><span data-stu-id="64441-201">Example: "LOGON.SCR"</span></span>

</dd> <dt>

<span data-ttu-id="64441-202">**ScreenSaverSecure**</span><span class="sxs-lookup"><span data-stu-id="64441-202">**ScreenSaverSecure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-203">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="64441-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64441-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-205">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \| ScreenSaverIsSecure ")</span><span class="sxs-lookup"><span data-stu-id="64441-205">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaverIsSecure")</span></span>
</dt> </dl>

<span data-ttu-id="64441-206">Das Kennwort ist für den Bildschirmschoner aktiviert.</span><span class="sxs-lookup"><span data-stu-id="64441-206">Password is enabled for the screen saver.</span></span>

</dd> <dt>

<span data-ttu-id="64441-207">**Screensavertimeout**</span><span class="sxs-lookup"><span data-stu-id="64441-207">**ScreenSaverTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-208">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="64441-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="64441-209">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-210">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \| SCREENSAVETIMEOUT "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Sekunden ")</span><span class="sxs-lookup"><span data-stu-id="64441-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="64441-211">Die Zeitspanne, die vor dem Start des Bildschirmschoners verstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="64441-211">Amount of time that passes before the screen saver starts.</span></span>

</dd> <dt>

<span data-ttu-id="64441-212">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="64441-212">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-213">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="64441-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64441-214">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-215">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="64441-215">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="64441-216">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="64441-216">Identifier by which the current object is known.</span></span>

<span data-ttu-id="64441-217">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="64441-217">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="64441-218">**Hintergrundbild**</span><span class="sxs-lookup"><span data-stu-id="64441-218">**Wallpaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-219">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="64441-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64441-220">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-221">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -System Steuerungs \\ \\ Desktop- \| Hintergrundbild ")</span><span class="sxs-lookup"><span data-stu-id="64441-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Wallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="64441-222">Der Dateiname für das Hintergrundbild im Hintergrund des Desktops.</span><span class="sxs-lookup"><span data-stu-id="64441-222">File name for the wallpaper design on the background of the desktop.</span></span>

<span data-ttu-id="64441-223">Beispiel: "WINNT.BMP"</span><span class="sxs-lookup"><span data-stu-id="64441-223">Example: "WINNT.BMP"</span></span>

</dd> <dt>

<span data-ttu-id="64441-224">**Wallpapier gestreckt**</span><span class="sxs-lookup"><span data-stu-id="64441-224">**WallpaperStretched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-225">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="64441-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64441-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-227">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ -Systemsteuerung \\ \\ Desktop \| Wallart ")</span><span class="sxs-lookup"><span data-stu-id="64441-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|WallpaperStyle")</span></span>
</dt> </dl>

<span data-ttu-id="64441-228">Das Hintergrundbild wird gestreckt, um den gesamten Bildschirm auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="64441-228">Wallpaper is stretched to fill the entire screen.</span></span> <span data-ttu-id="64441-229">Microsoft Plus!</span><span class="sxs-lookup"><span data-stu-id="64441-229">Microsoft Plus!</span></span> <span data-ttu-id="64441-230">muss installiert werden, bevor diese Option verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="64441-230">must be installed before this option is available.</span></span> <span data-ttu-id="64441-231">Wenn der Wert **false** ist, behält das Hintergrund seine ursprünglichen Dimensionen im Desktop Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="64441-231">If **FALSE**, the wallpaper retains its original dimensions on the desktop background.</span></span>

</dd> <dt>

<span data-ttu-id="64441-232">**Wallpapierkachel**</span><span class="sxs-lookup"><span data-stu-id="64441-232">**WallpaperTiled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64441-233">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="64441-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64441-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64441-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64441-235">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Standard \\ \\ systemsteuerungpanel \\ \\ Desktop \| tilewallpaper ")</span><span class="sxs-lookup"><span data-stu-id="64441-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|TileWallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="64441-236">Das Hintergrundbild wird gekachelt oder zentriert.</span><span class="sxs-lookup"><span data-stu-id="64441-236">Wallpaper is tiled or centered.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64441-237">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64441-237">Remarks</span></span>

<span data-ttu-id="64441-238">Die **Win32 \_ -Desktop** Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="64441-238">The **Win32\_Desktop** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="64441-239">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="64441-239">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="64441-240">Wenn Sie diese Klasse z. b. auf dem lokalen Computer auflisten, muss das Konto, unter dem Ihre Anwendung ausgeführt wird, über diese Berechtigung verfügen.</span><span class="sxs-lookup"><span data-stu-id="64441-240">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="64441-241">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="64441-241">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="64441-242">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64441-242">Examples</span></span>

<span data-ttu-id="64441-243">Im folgenden Codebeispiel wird das Abrufen von Desktop Informationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="64441-243">The following code sample describes how to retrieve desktop information.</span></span>


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a><span data-ttu-id="64441-244">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64441-244">Requirements</span></span>



| <span data-ttu-id="64441-245">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64441-245">Requirement</span></span> | <span data-ttu-id="64441-246">Wert</span><span class="sxs-lookup"><span data-stu-id="64441-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64441-247">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64441-247">Minimum supported client</span></span><br/> | <span data-ttu-id="64441-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64441-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64441-249">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64441-249">Minimum supported server</span></span><br/> | <span data-ttu-id="64441-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64441-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64441-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="64441-251">Namespace</span></span><br/>                | <span data-ttu-id="64441-252">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64441-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64441-253">MOF</span><span class="sxs-lookup"><span data-stu-id="64441-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64441-254"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="64441-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64441-255">DLL</span><span class="sxs-lookup"><span data-stu-id="64441-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64441-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64441-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64441-257">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64441-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64441-258">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="64441-258">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="64441-259">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64441-259">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

