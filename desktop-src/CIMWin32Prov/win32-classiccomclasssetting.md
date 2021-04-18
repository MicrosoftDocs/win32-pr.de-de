---
description: Stellt die Einstellungen einer Component Object Model-Komponente (com) dar.
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344969"
---
# <a name="win32_classiccomclasssetting-class"></a><span data-ttu-id="bbd52-103">Win32 \_ classiccomclasssetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="bbd52-103">Win32\_ClassicCOMClassSetting class</span></span>

<span data-ttu-id="bbd52-104">Die **Win32 \_ classiccomclasssetting** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Einstellungen einer Component Object Model (com)-Komponente dar.</span><span class="sxs-lookup"><span data-stu-id="bbd52-104">The **Win32\_ClassicCOMClassSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="bbd52-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bbd52-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bbd52-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bbd52-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd52-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbd52-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a><span data-ttu-id="bbd52-108">Member</span><span class="sxs-lookup"><span data-stu-id="bbd52-108">Members</span></span>

<span data-ttu-id="bbd52-109">Die **Win32 \_ classiccomclasssetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bbd52-109">The **Win32\_ClassicCOMClassSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="bbd52-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbd52-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbd52-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbd52-111">Properties</span></span>

<span data-ttu-id="bbd52-112">Die **Win32 \_ classiccomclasssetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bbd52-112">The **Win32\_ClassicCOMClassSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbd52-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="bbd52-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-116">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[AppID\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-117">GUID (Global Unique Identifier) für die COM-Anwendung, die diese COM-Komponente verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbd52-117">Globally unique identifier (GUID) for the COM application using this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-118">**Autoconvertumclsid**</span><span class="sxs-lookup"><span data-stu-id="bbd52-118">**AutoConvertToClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-121">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ autoconvertto \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoConvertTo\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-122">GUID der com-Klasse, in die diese COM-Komponente automatisch konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="bbd52-122">GUID of the COM class to which this COM component will automatically be converted.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-123">**AutoTreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="bbd52-123">**AutoTreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-126">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoTreatAs \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-126">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoTreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-127">GUID für die COM-Komponente, die Instanzen dieser Klasse automatisch emuliert.</span><span class="sxs-lookup"><span data-stu-id="bbd52-127">GUID for the COM component that will automatically emulate instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bbd52-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-131">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bbd52-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-132">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="bbd52-132">Short textual description of the current object.</span></span>

<span data-ttu-id="bbd52-133">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bbd52-133">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-134">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="bbd52-134">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-137">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes Software Classes \\ \\ CLSID \\ \\ {GUID} \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-138">GUID dieser COM-Komponente.</span><span class="sxs-lookup"><span data-stu-id="bbd52-138">GUID of this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-139">**Steuerung**</span><span class="sxs-lookup"><span data-stu-id="bbd52-139">**Control**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-140">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bbd52-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-142">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID}- \\ \\ Steuerelement")</span><span class="sxs-lookup"><span data-stu-id="bbd52-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Control")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-143">COM-Komponente ist ein OLE-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="bbd52-143">COM component is an OLE control.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-144">**DefaultIcon**</span><span class="sxs-lookup"><span data-stu-id="bbd52-144">**DefaultIcon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-147">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\DefaultIcon\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-148">Pfad zur ausführbaren Datei und zum Ressourcen Bezeichner des Standard Symbols, das von der-Klasse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd52-148">Path to the executable file and resource identifier of the default icon used by the class.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-149">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bbd52-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-152">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="bbd52-152">Textual description of the current object.</span></span>

<span data-ttu-id="bbd52-153">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bbd52-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-154">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="bbd52-154">**InprocHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-157">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-158">Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname zu einem benutzerdefinierten 16-Bit-Handler für die COM-Komponente</span><span class="sxs-lookup"><span data-stu-id="bbd52-158">Full path including filename or only filename to a 16-bit custom handler for the COM component.</span></span> <span data-ttu-id="bbd52-159">Der Anbieter gibt nicht immer den vollständigen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="bbd52-159">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-160">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="bbd52-160">**InprocHandler32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-163">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-164">Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname zu einem benutzerdefinierten 32-Bit-Handler für die COM-Komponente</span><span class="sxs-lookup"><span data-stu-id="bbd52-164">Full path including filename or only filename to a 32-bit custom handler for the COM component.</span></span> <span data-ttu-id="bbd52-165">Der Anbieter gibt nicht immer den vollständigen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="bbd52-165">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-166">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="bbd52-166">**InprocServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-169">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-170">Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname zu einer 16-Bit-Prozess internen Server-DLL für diese COM-Komponente.</span><span class="sxs-lookup"><span data-stu-id="bbd52-170">Full path including filename or only filename to a 16-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="bbd52-171">Der Anbieter gibt nicht immer den vollständigen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="bbd52-171">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-172">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="bbd52-172">**InprocServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-173">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-175">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-176">Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname zu einer 32-Bit-Prozess internen Server-DLL für diese COM-Komponente.</span><span class="sxs-lookup"><span data-stu-id="bbd52-176">Full path including filename or only filename to a 32-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="bbd52-177">Der Anbieter gibt nicht immer den vollständigen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="bbd52-177">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-178">**Einfügbar**</span><span class="sxs-lookup"><span data-stu-id="bbd52-178">**Insertable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-179">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bbd52-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-180">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-181">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")</span><span class="sxs-lookup"><span data-stu-id="bbd52-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Insertable")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-182">COM-Komponente kann in OLE-Container Anwendungen eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="bbd52-182">COM component can be inserted into OLE container applications.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-183">**JAVACLASS**</span><span class="sxs-lookup"><span data-stu-id="bbd52-183">**JavaClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-184">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="bbd52-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-186">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ JAVACLASS \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[JavaClass\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-187">Die COM-Komponente ist eine Java-Komponente.</span><span class="sxs-lookup"><span data-stu-id="bbd52-187">COM component is a Java component.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-188">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="bbd52-188">**LocalServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-191">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-192">Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname für eine 16-Bit-Anwendung für einen lokalen</span><span class="sxs-lookup"><span data-stu-id="bbd52-192">Full path including filename or only filename to a 16-bit local server application.</span></span> <span data-ttu-id="bbd52-193">Der Anbieter gibt nicht immer den vollständigen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="bbd52-193">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-194">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="bbd52-194">**LocalServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-195">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-196">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-197">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-198">Vollständiger Pfad, einschließlich Dateiname oder nur Dateiname für eine lokale 32-Bit-Serveranwendung.</span><span class="sxs-lookup"><span data-stu-id="bbd52-198">Full path including filename or only filename to a 32-bit local server application.</span></span> <span data-ttu-id="bbd52-199">Der Anbieter gibt nicht immer den vollständigen Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="bbd52-199">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-200">**LongDisplayName**</span><span class="sxs-lookup"><span data-stu-id="bbd52-200">**LongDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-203">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ auxusertype \\ \\ 3 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\3\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-204">Der vollständige Name der com-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bbd52-204">Full name of the COM application.</span></span> <span data-ttu-id="bbd52-205">Sie wird in Bereichen wie dem **Ergebnis** Feld des OLE-Dialog Felds " **speziell einfügen** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbd52-205">It is used in areas such as the **Results** field of the **OLE Paste Special** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-206">**ProgID**</span><span class="sxs-lookup"><span data-stu-id="bbd52-206">**ProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-209">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-209">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ProgID\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-210">Programm Bezeichner, der der COM-Komponente zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bbd52-210">Programmatic identifier associated with the COM component.</span></span> <span data-ttu-id="bbd52-211">Das Format einer ProgID ist <Vendor. <Component. <Version.</span><span class="sxs-lookup"><span data-stu-id="bbd52-211">The format of a ProgID is <Vendor.<Component.<Version.</span></span> <span data-ttu-id="bbd52-212">Es ist nicht garantiert, dass dieser Bezeichner eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="bbd52-212">This identifier is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-213">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="bbd52-213">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-214">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-216">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bbd52-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-217">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="bbd52-217">Identifier by which the current object is known.</span></span>

<span data-ttu-id="bbd52-218">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bbd52-218">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-219">**ShortDisplayName**</span><span class="sxs-lookup"><span data-stu-id="bbd52-219">**ShortDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-220">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-221">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-222">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ auxusertype \\ \\ 2 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\2\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-223">Kurzname der com-Anwendung (wird in Menüs und Popups verwendet).</span><span class="sxs-lookup"><span data-stu-id="bbd52-223">Short name of the COM application (used in menus and pop-ups).</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-224">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="bbd52-224">**ThreadingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-226">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-227">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InProcServer32 \[ ThreadingModel \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[ThreadingModel\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-228">Threading Modell, das von in-Process-COM-Klassen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd52-228">Threading model used by in-process COM classes.</span></span> <span data-ttu-id="bbd52-229">Wenn diese Eigenschaft **null** ist, wird kein Threading Modell verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbd52-229">If this property is **NULL**, then no threading model is used.</span></span> <span data-ttu-id="bbd52-230">Die Komponente wird im Haupt Thread des Clients erstellt, und Aufrufe von anderen Threads werden an diesen Thread gemarshallt.</span><span class="sxs-lookup"><span data-stu-id="bbd52-230">The component is created on the main thread of the client and calls from other threads are marshaled to this thread.</span></span>

<span data-ttu-id="bbd52-231">Das Apartment Modell gibt an, dass Komponenten nur von einem einzigen Thread eingegeben werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="bbd52-231">The Apartment model specifies that components may be entered by one and only one thread.</span></span> <span data-ttu-id="bbd52-232">Allgemeine Daten, die von diesen Objekt Server Typen gespeichert werden, müssen vor Thread Kollisionen geschützt werden, da der Objekt Server mehrere Komponenten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbd52-232">Common data held by these types of object servers must be protected against thread collisions because the object server supports multiple components.</span></span> <span data-ttu-id="bbd52-233">Jede Komponente kann gleichzeitig von verschiedenen Threads eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bbd52-233">Each component can be entered simultaneously by different threads.</span></span>

<span data-ttu-id="bbd52-234">Das kostenlose Modell gibt an, dass die Komponenten keine Einschränkungen für die Threads oder die Anzahl der Threads haben, die das Objekt eingeben können.</span><span class="sxs-lookup"><span data-stu-id="bbd52-234">The Free model specifies that components place no restrictions on which threads or how many threads can enter the object.</span></span> <span data-ttu-id="bbd52-235">Das Objekt kann keine Thread spezifischen Daten enthalten und muss seine Daten vor gleichzeitigem Zugriff durch mehrere Threads schützen.</span><span class="sxs-lookup"><span data-stu-id="bbd52-235">The object cannot contain thread-specific data and must protect its data from simultaneous access by multiple threads.</span></span> <span data-ttu-id="bbd52-236">Auf frei Thread Komponenten kann jedoch nicht direkt von Apartment Threads zugegriffen werden, und Aufrufe an diese Komponenten werden über das Client Apartment gemarshallt.</span><span class="sxs-lookup"><span data-stu-id="bbd52-236">Free-threaded components however, cannot be accessed by apartment threads directly, and calls to them are marshaled across from the client apartment.</span></span>

<span data-ttu-id="bbd52-237">Wenn beides angegeben ist, können Komponenten entweder im Apartment Thread-oder im Free Thread-Modus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bbd52-237">When Both is specified, components can be used in either apartment-threaded or free-threaded modes.</span></span> <span data-ttu-id="bbd52-238">Diese Komponenten können von mehreren Threads eingegeben werden, Ihre Daten vor Thread Kollisionen schützen und keine Thread spezifischen Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="bbd52-238">These components can be entered by multiple threads, protect their data from thread collisions, and do not contain thread-specific data.</span></span>

<span data-ttu-id="bbd52-239">Die Werte sind:</span><span class="sxs-lookup"><span data-stu-id="bbd52-239">The values are:</span></span>

<dl> <dd><span data-ttu-id="bbd52-240">Apartment</span><span class="sxs-lookup"><span data-stu-id="bbd52-240">"Apartment"</span></span></dd> <dd><span data-ttu-id="bbd52-241">Kosten</span><span class="sxs-lookup"><span data-stu-id="bbd52-241">"Free"</span></span></dd> <dd><span data-ttu-id="bbd52-242">Zwar</span><span class="sxs-lookup"><span data-stu-id="bbd52-242">"Both"</span></span></dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

<span data-ttu-id="bbd52-243">**Apartment** ("Apartment")</span><span class="sxs-lookup"><span data-stu-id="bbd52-243">**Apartment** ("Apartment")</span></span>


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

<span data-ttu-id="bbd52-244">**Kostenlos** ("kostenlos")</span><span class="sxs-lookup"><span data-stu-id="bbd52-244">**Free** ("Free")</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="bbd52-245">**Beides** ("beides")</span><span class="sxs-lookup"><span data-stu-id="bbd52-245">**Both** ("Both")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbd52-246">**ToolBoxBitmap32**</span><span class="sxs-lookup"><span data-stu-id="bbd52-246">**ToolBoxBitmap32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-248">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-249">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ToolBoxBitmap32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-250">Modulname und Ressourcen Bezeichner für eine kleine (16x16) Bitmap, die für das Gesicht einer Symbolleiste oder Toolbox Schaltfläche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd52-250">Module name and resource identifier for a small (16x16) bitmap used for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="bbd52-251">Wird verwendet, wenn die COM-Komponente ein OLE-oder ActiveX-Steuerelement ist.</span><span class="sxs-lookup"><span data-stu-id="bbd52-251">Used when the COM component is an OLE or ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-252">**TreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="bbd52-252">**TreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-253">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-254">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-255">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-255">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-256">GUID einer COM-Komponente, die Instanzen dieser Komponente emulieren kann.</span><span class="sxs-lookup"><span data-stu-id="bbd52-256">GUID of a COM component that can emulate instances of this component.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-257">**TypeLibraryId**</span><span class="sxs-lookup"><span data-stu-id="bbd52-257">**TypeLibraryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-258">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-259">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-260">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ typelib \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-260">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TypeLib\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-261">GUID für die Typbibliothek für diese COM-Komponente.</span><span class="sxs-lookup"><span data-stu-id="bbd52-261">GUID for the type library for this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-262">**Version**</span><span class="sxs-lookup"><span data-stu-id="bbd52-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-265">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Version \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Version\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-266">Versionsnummer dieser com-Klasse.</span><span class="sxs-lookup"><span data-stu-id="bbd52-266">Version number of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="bbd52-267">**VersionIndependentProgId**</span><span class="sxs-lookup"><span data-stu-id="bbd52-267">**VersionIndependentProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbd52-268">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bbd52-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bbd52-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbd52-270">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ \\ \\ Classes \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="bbd52-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\VersionIndependentProgId\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="bbd52-271">Programm Bezeichner, der für alle Versionen desselben Programms konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="bbd52-271">Program identifier that is consistent for all versions of the same program.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bbd52-272">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbd52-272">Remarks</span></span>

<span data-ttu-id="bbd52-273">Die **Win32 \_ classiccomclasssetting** -Klasse wird von [**Win32 \_ comsetting**](win32-comsetting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="bbd52-273">The **Win32\_ClassicCOMClassSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd52-274">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbd52-274">Requirements</span></span>



| <span data-ttu-id="bbd52-275">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbd52-275">Requirement</span></span> | <span data-ttu-id="bbd52-276">Wert</span><span class="sxs-lookup"><span data-stu-id="bbd52-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd52-277">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbd52-277">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd52-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbd52-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bbd52-279">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbd52-279">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd52-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbd52-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bbd52-281">Namespace</span><span class="sxs-lookup"><span data-stu-id="bbd52-281">Namespace</span></span><br/>                | <span data-ttu-id="bbd52-282">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bbd52-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bbd52-283">MOF</span><span class="sxs-lookup"><span data-stu-id="bbd52-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbd52-284"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bbd52-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbd52-285">DLL</span><span class="sxs-lookup"><span data-stu-id="bbd52-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbd52-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbd52-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd52-287">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbd52-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd52-288">**Win32- \_ comsetting**</span><span class="sxs-lookup"><span data-stu-id="bbd52-288">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="bbd52-289">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bbd52-289">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

