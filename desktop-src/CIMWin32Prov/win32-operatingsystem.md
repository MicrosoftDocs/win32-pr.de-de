---
description: Stellt ein Windows-basiertes Betriebssystem dar, das auf einem Computer installiert ist.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Win32_OperatingSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214270"
---
# <a name="win32_operatingsystem-class"></a><span data-ttu-id="eb6d5-103">Win32- \_ OperatingSystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="eb6d5-103">Win32\_OperatingSystem class</span></span>

<span data-ttu-id="eb6d5-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) des **Win32- \_ OperatingSystems** stellt ein Windows-basiertes Betriebssystem dar, das auf einem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-104">The **Win32\_OperatingSystem** [WMI class](../wmisdk/retrieving-a-class.md) represents a Windows-based operating system installed on a computer.</span></span>

<span data-ttu-id="eb6d5-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="eb6d5-106">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb6d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb6d5-107">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a><span data-ttu-id="eb6d5-108">Member</span><span class="sxs-lookup"><span data-stu-id="eb6d5-108">Members</span></span>

<span data-ttu-id="eb6d5-109">Die **Win32 \_ OperatingSystem** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eb6d5-109">The **Win32\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="eb6d5-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="eb6d5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="eb6d5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb6d5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="eb6d5-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="eb6d5-112">Methods</span></span>

<span data-ttu-id="eb6d5-113">Die **Win32 \_ OperatingSystem** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-113">The **Win32\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="eb6d5-114">Methode</span><span class="sxs-lookup"><span data-stu-id="eb6d5-114">Method</span></span>                                                                                     | <span data-ttu-id="eb6d5-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb6d5-115">Description</span></span>                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb6d5-116">**Reboot**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-116">**Reboot**</span></span>](reboot-method-in-class-win32-operatingsystem.md)                             | <span data-ttu-id="eb6d5-117">Der Computer wird heruntergefahren und dann neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-117">Shuts down and then restarts the computer system.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="eb6d5-118">**SetDateTime**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-118">**SetDateTime**</span></span>](setdatetime-method-in-class-win32-operatingsystem.md)                   | <span data-ttu-id="eb6d5-119">Ermöglicht das Festlegen des Datums und der Uhrzeit des Computers.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-119">Allows the computer date and time to be set.</span></span><br/>                                                                                                                                                                                                                |
| [<span data-ttu-id="eb6d5-120">**Abschlusses**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-120">**Shutdown**</span></span>](shutdown-method-in-class-win32-operatingsystem.md)                         | <span data-ttu-id="eb6d5-121">Entlädt Programme und DLLs an den Punkt, an dem Sie den Computer sicher ausschalten können.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-121">Unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="eb6d5-122">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-122">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)               | <span data-ttu-id="eb6d5-123">Bietet den vollständigen Satz von Optionen für das Herunterfahren, die von den Windows-Betriebssystemen</span><span class="sxs-lookup"><span data-stu-id="eb6d5-123">Provides the full set of shutdown options supported by Windows operating systems.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="eb6d5-124">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-124">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | <span data-ttu-id="eb6d5-125">Bietet den gleichen Satz von Optionen für das Herunterfahren, der von der [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) -Methode im **Win32- \_ OperatingSystem** unterstützt wird. Sie können jedoch auch Kommentare, einen Grund für das Herunterfahren oder einen Timeout Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-125">Provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in **Win32\_OperatingSystem**, but also allows you to specify comments, a reason for shutdown, or a timeout.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="eb6d5-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb6d5-126">Properties</span></span>

<span data-ttu-id="eb6d5-127">Die **Win32 \_ OperatingSystem** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-127">The **Win32\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb6d5-128">**BootDevice**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-128">**BootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-131">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Drive \_ map \_ Info \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-132">Der Name des Laufwerks, von dem aus das Windows-Betriebssystem gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-132">Name of the disk drive from which the Windows operating system starts.</span></span>

<span data-ttu-id="eb6d5-133">Beispiel: " \\ \\ Device \\ Harddisk0"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-133">Example: "\\\\Device\\Harddisk0"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-134">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-134">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-137">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwBuildNumber")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-138">Buildnummer eines Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-138">Build number of an operating system.</span></span> <span data-ttu-id="eb6d5-139">Sie kann für präzisere Versionsinformationen als Produkt Versionsnummern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-139">It can be used for more precise version information than product release version numbers.</span></span>

<span data-ttu-id="eb6d5-140">Beispiel: "1381"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-140">Example: "1381"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-141">**BuildType**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-141">**BuildType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-144">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ \| CurrentType")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|CurrentType")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-145">Typ des Builds, der für ein Betriebssystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-145">Type of build used for an operating system.</span></span>

<span data-ttu-id="eb6d5-146">Beispiele: "" Retail Build "", "" aktivierter Build ""</span><span class="sxs-lookup"><span data-stu-id="eb6d5-146">Examples: ""retail build"", ""checked build""</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-150">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-151">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-151">Short description of the object—a one-line string.</span></span> <span data-ttu-id="eb6d5-152">Die Zeichenfolge enthält die Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-152">The string includes the operating system version.</span></span> <span data-ttu-id="eb6d5-153">Beispiel: "Microsoft Windows 7 Enterprise".</span><span class="sxs-lookup"><span data-stu-id="eb6d5-153">For example, "Microsoft Windows 7 Enterprise ".</span></span> <span data-ttu-id="eb6d5-154">Diese Eigenschaft kann lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-154">This property can be localized.</span></span>

<span data-ttu-id="eb6d5-155">**Windows Vista und Windows 7:** Diese Eigenschaft kann nachfolgende Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-155">**Windows Vista and Windows 7:** This property may contain trailing characters.</span></span> <span data-ttu-id="eb6d5-156">Beispielsweise kann die Zeichenfolge "Microsoft Windows 7 Enterprise" (nachfolgende Leerzeichen) erforderlich sein, um Informationen mithilfe dieser Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-156">For example, the string "Microsoft Windows 7 Enterprise " (trailing space included) may be necessary to retrieve information using this property.</span></span>

<span data-ttu-id="eb6d5-157">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-158">**Codesatz**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-158">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-159">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-160">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-161">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (6), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**getlocaleingefo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ idefaultansicodepage")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-161">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_IDEFAULTANSICODEPAGE")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-162">Der Code Page Wert, den ein Betriebssystem verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-162">Code page value an operating system uses.</span></span> <span data-ttu-id="eb6d5-163">Eine Codepage enthält eine Zeichentabelle, die von einem Betriebssystem verwendet wird, um Zeichen folgen für verschiedene Sprachen zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-163">A code page contains a character table that an operating system uses to translate strings for different languages.</span></span> <span data-ttu-id="eb6d5-164">Der American National Standards Institute (ANSI) listet Werte auf, die definierte Codepages darstellen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-164">The American National Standards Institute (ANSI) lists values that represent defined code pages.</span></span> <span data-ttu-id="eb6d5-165">Wenn ein Betriebssystem keine ANSI-Codepage verwendet, wird dieses Element auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-165">If an operating system does not use an ANSI code page, this member is set to 0 (zero).</span></span> <span data-ttu-id="eb6d5-166">Die **Codeset** -Zeichenfolge kann maximal sechs Zeichen verwenden, um den Code Page Wert zu definieren.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-166">The **CodeSet** string can use a maximum of six characters to define the code page value.</span></span>

<span data-ttu-id="eb6d5-167">Beispiel: "1255"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-167">Example: "1255"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-168">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-168">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-170">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-171">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**getlocaleingefo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ iCountry")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-171">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ICOUNTRY")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-172">Code für das Land bzw. die Region, das von einem Betriebssystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-172">Code for the country/region that an operating system uses.</span></span> <span data-ttu-id="eb6d5-173">Werte basieren auf den Präfixen für die internationale Telefon Wahl – auch als IBM Land/Region-Codes bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-173">Values are based on international phone dialing prefixes—also referred to as IBM country/region codes.</span></span> <span data-ttu-id="eb6d5-174">Für diese Eigenschaft können maximal sechs Zeichen verwendet werden, um den Code Wert für Land/Region zu definieren.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-174">This property can use a maximum of six characters to define the country/region code value.</span></span>

<span data-ttu-id="eb6d5-175">Beispiel: "1" (USA)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-175">Example: "1" (United States)</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-176">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-179">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-179">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-180">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt wird, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-180">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="eb6d5-181">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-181">When used with other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="eb6d5-182">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-182">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-183">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-183">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-184">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-185">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-186">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-186">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-187">Der Name der Erstellungs Klasse des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-187">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="eb6d5-188">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-188">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-189">**CSDVersion**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-189">**CSDVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-190">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-192">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**szCSDVersion**")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-193">**Null**-terminierte Zeichenfolge, die die neueste auf einem Computer installierte Service Pack angibt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-193">**NULL**-terminated string that indicates the latest service pack installed on a computer.</span></span> <span data-ttu-id="eb6d5-194">Wenn keine Service Pack installiert ist, ist die Zeichenfolge **null**.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-194">If no service pack is installed, the string is **NULL**.</span></span>

<span data-ttu-id="eb6d5-195">Beispiel: "Service Pack 3"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-195">Example: "Service Pack 3"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-196">**CSName**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-196">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-199">Qualifizierer: weiter [**gegeben ("**](../wmisdk/standard-qualifiers.md) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-199">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-200">Name des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-200">Name of the scoping computer system.</span></span>

<span data-ttu-id="eb6d5-201">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-201">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-202">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-202">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-203">Datentyp: **sint16**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-203">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-205">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Minuten")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-205">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-206">Die Anzahl in Minuten, für die ein Betriebssystem von der Greenwich Mean Time (GMT) versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-206">Number, in minutes, an operating system is offset from Greenwich mean time (GMT).</span></span> <span data-ttu-id="eb6d5-207">Die Zahl ist positiv, negativ oder 0 (null).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-207">The number is positive, negative, or zero.</span></span>

<span data-ttu-id="eb6d5-208">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-208">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-209">**Dataexecutionprevention \_ 32bitapplications**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-209">**DataExecutionPrevention\_32BitApplications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-210">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-212">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-213">Wenn die Hardware Funktion zur Daten Ausführungs Verhinderung verfügbar ist, gibt diese Eigenschaft an, dass die Funktion für 32-Bit-Anwendungen auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-213">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for 32-bit applications if **True**.</span></span> <span data-ttu-id="eb6d5-214">Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im [Startkonfigurationsdaten-Speicher (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) konfiguriert, und die Eigenschaften im **Win32- \_ OperatingSystem** werden entsprechend festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-214">On 64-bit computers, the data execution prevention feature is configured in the [Boot Configuration Data (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-215">**Dataexecutionprevention \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-215">**DataExecutionPrevention\_Available**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-216">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-218">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-219">Die Verhinderung von Datenausführung ist eine Hardware Funktion, um Pufferüberlauf Angriffe zu verhindern, indem Sie die Ausführung von Code auf Datentyp-Speicherseiten beenden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-219">Data execution prevention is a hardware feature to prevent buffer overrun attacks by stopping the execution of code on data-type memory pages.</span></span> <span data-ttu-id="eb6d5-220">**True** gibt an, dass diese Funktion verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-220">If **True**, then this feature is available.</span></span> <span data-ttu-id="eb6d5-221">Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im BCD-Speicher konfiguriert, und die Eigenschaften im **Win32- \_ OperatingSystem** werden entsprechend festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-221">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-222">**Dataexecutionprevention- \_ Treiber**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-222">**DataExecutionPrevention\_Drivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-223">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-225">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-226">Wenn die Hardware Funktion zur Daten Ausführungs Verhinderung verfügbar ist, gibt diese Eigenschaft an, dass die Funktion für Treiber auf " **true**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-226">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for drivers if **True**.</span></span> <span data-ttu-id="eb6d5-227">Auf 64-Bit-Computern wird das Feature zur Verhinderung der Datenausführung im BCD-Speicher konfiguriert, und die Eigenschaften im **Win32- \_ OperatingSystem** werden entsprechend festgelegt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-227">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-228">**Dataexecutionprevention \_ supportpolicy**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-228">**DataExecutionPrevention\_SupportPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-229">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-229">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-231">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-232">Gibt an, welche Einstellung für die Daten Ausführungs Verhinderung (DEP) angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-232">Indicates which Data Execution Prevention (DEP) setting is applied.</span></span> <span data-ttu-id="eb6d5-233">Die DEP-Einstellung gibt den Umfang an, in dem DEP auf 32-Bit-Anwendungen im System angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-233">The DEP setting specifies the extent to which DEP applies to 32-bit applications on the system.</span></span> <span data-ttu-id="eb6d5-234">DEP wird immer auf den Windows-Kernel angewendet.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-234">DEP is always applied to the Windows kernel.</span></span>

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span data-ttu-id="eb6d5-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Immer aus** (0)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-236">DEP ist für alle 32-Bit-Anwendungen auf dem Computer deaktiviert, ohne dass Ausnahmen auftreten.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-236">DEP is turned off for all 32-bit applications on the computer with no exceptions.</span></span> <span data-ttu-id="eb6d5-237">Diese Einstellung ist für die Benutzeroberfläche nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-237">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span data-ttu-id="eb6d5-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-239">DEP ist für alle 32-Bit-Anwendungen auf dem Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-239">DEP is enabled for all 32-bit applications on the computer.</span></span> <span data-ttu-id="eb6d5-240">Diese Einstellung ist für die Benutzeroberfläche nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-240">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span data-ttu-id="eb6d5-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt in** (2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt In** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-242">DEP ist für eine begrenzte Anzahl von Binärdateien, den Kernel und alle Windows-basierten Dienste aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-242">DEP is enabled for a limited number of binaries, the kernel, and all Windows-based services.</span></span> <span data-ttu-id="eb6d5-243">Allerdings ist es für alle 32-Bit-Anwendungen standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-243">However, it is off by default for all 32-bit applications.</span></span> <span data-ttu-id="eb6d5-244">Ein Benutzer oder Administrator muss explizit entweder die **Always on** oder die **opt** -Einstellung auswählen, bevor DEP auf 32-Bit-Anwendungen angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-244">A user or administrator must explicitly choose either the **Always On** or the **Opt Out** setting before DEP can be applied to 32-bit applications.</span></span>

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span data-ttu-id="eb6d5-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Ablehnen** (3)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Opt Out** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-246">DEP ist für alle 32-Bit-Anwendungen standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-246">DEP is enabled by default for all 32-bit applications.</span></span> <span data-ttu-id="eb6d5-247">Ein Benutzer oder Administrator kann die Unterstützung für eine 32-Bit-Anwendung explizit entfernen, indem er die Anwendung einer Ausnahmeliste hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-247">A user or administrator can explicitly remove support for a 32-bit application by adding the application to an exceptions list.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-248">**Debuggen**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-248">**Debug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-249">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-251">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ Debug")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-251">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)\|SM\_DEBUG")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-252">Das Betriebssystem ist ein aktivierter (Debuggen) Build.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-252">Operating system is a checked (debug) build.</span></span> <span data-ttu-id="eb6d5-253">Wenn der Wert **true** ist, wird die Debugversion installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-253">If **True**, the debugging version is installed.</span></span> <span data-ttu-id="eb6d5-254">Aktivierte Builds bieten Fehlerüberprüfung, Argument Überprüfung und systemdebugcode.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-254">Checked builds provide error checking, argument verification, and system debugging code.</span></span> <span data-ttu-id="eb6d5-255">Zusätzlicher Code in einer überprüften Binärdatei generiert eine Kernel Debugger-Fehlermeldung und unterbricht den Debugger.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-255">Additional code in a checked binary generates a kernel debugger error message and breaks into the debugger.</span></span> <span data-ttu-id="eb6d5-256">Dadurch können Sie sofort die Ursache und den Speicherort des Fehlers bestimmen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-256">This helps immediately determine the cause and location of the error.</span></span> <span data-ttu-id="eb6d5-257">Aufgrund des zusätzlichen Codes, der ausgeführt wird, kann die Leistung von einem aktivierten Build beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-257">Performance may be affected in a checked build due to the additional code that is executed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-258">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-258">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-259">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-260">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eb6d5-260">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-261">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Beschreibung"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-261">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-262">Die Beschreibung des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-262">Description of the Windows operating system.</span></span> <span data-ttu-id="eb6d5-263">Einige Benutzeroberflächen, z. b. solche, die das Bearbeiten dieser Beschreibung ermöglichen, beschränken die Länge auf 48 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-263">Some user interfaces for example, those that allow editing of this description, limit its length to 48 characters.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-264">**Distri**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-264">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-265">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-266">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-267">**True** gibt an, dass das Betriebssystem auf mehrere Computersystem Knoten verteilt ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-267">If **True**, the operating system is distributed across several computer system nodes.</span></span> <span data-ttu-id="eb6d5-268">Wenn dies der Fall ist, sollten diese Knoten als Cluster gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-268">If so, these nodes should be grouped as a cluster.</span></span>

<span data-ttu-id="eb6d5-269">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-269">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-270">**EncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-270">**EncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-271">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-271">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-272">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-273">Verschlüsselungs Stufe für sichere Transaktionen: 40-Bit, 128-Bit oder *n*-Bit.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-273">Encryption level for secure transactions: 40-bit, 128-bit, or *n*-bit.</span></span>

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

<span data-ttu-id="eb6d5-274">**40-Bit** (0)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-274">**40-bit** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

<span data-ttu-id="eb6d5-275">**128-Bit** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-275">**128-bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

<span data-ttu-id="eb6d5-276">**n-Bit** (2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-276">**n-bit** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-277">**ForegroundApplicationBoost**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-277">**ForegroundApplicationBoost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-278">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-278">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-279">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eb6d5-279">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-280">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ prioritycontrol \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-281">Der Vordergrund Anwendung wird eine Erhöhung der Priorität eingeräumt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-281">Increase in priority is given to the foreground application.</span></span> <span data-ttu-id="eb6d5-282">Anwendungs Verstärkung wird implementiert, indem eine Anwendung mehr Ausführungszeit Scheiben (Quantum-Längen) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-282">Application boost is implemented by giving an application more execution time slices (quantum lengths).</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="eb6d5-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (0)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-284">Das System erhöht die Quantum-Länge um 6.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-284">The system boosts the quantum length by 6.</span></span>

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="eb6d5-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimal** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-286">Das System erhöht die Quantum-Länge um 12.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-286">The system boosts the quantum length by 12.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="eb6d5-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-288">Das System erhöht die Quantum-Länge um 18.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-288">The system boosts the quantum length by 18.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-289">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-289">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-290">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-291">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-292">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-292">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-293">Anzahl von physischem Speicher (in Kilobytes), der derzeit nicht verwendet wird und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-293">Number, in kilobytes, of physical memory currently unused and available.</span></span>

<span data-ttu-id="eb6d5-294">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-294">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="eb6d5-295">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-295">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-296">**Freespaceinpagingfiles**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-296">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-297">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-298">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-299">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| System Arbeitsspeicher-Einstellungen \| 001,4 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-300">Die Zahl in Kilobytes, die in den Auslagerungs Dateien des Betriebssystems zugeordnet werden kann, ohne dass andere Seiten ausgetauscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-300">Number, in kilobytes, that can be mapped into the operating system paging files without causing any other pages to be swapped out.</span></span>

<span data-ttu-id="eb6d5-301">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="eb6d5-302">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-302">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-303">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-303">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-304">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-305">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-306">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-306">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-307">Anzahl in Kilobyte des virtuellen Speichers, der derzeit nicht verwendet wird und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-307">Number, in kilobytes, of virtual memory currently unused and available.</span></span>

<span data-ttu-id="eb6d5-308">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="eb6d5-309">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-309">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-311">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-312">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-313">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-313">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-314">Date-Objekt wurde installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-314">Date object was installed.</span></span> <span data-ttu-id="eb6d5-315">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-315">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="eb6d5-316">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-317">**LargeSystemCache**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-317">**LargeSystemCache**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-318">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-319">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-320">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-321">Diese Eigenschaft ist veraltet und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-321">This property is obsolete and not supported.</span></span>

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span data-ttu-id="eb6d5-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Für Anwendungen optimieren** (0)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimize for Applications** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-323">Optimieren Sie den Arbeitsspeicher für Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-323">Optimize memory for applications.</span></span>

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span data-ttu-id="eb6d5-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimieren der System Leistung** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimize for System Performance** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-325">Optimieren Sie den Arbeitsspeicher für die Systemleistung.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-325">Optimize memory for system performance.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-326">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-326">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-327">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-328">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-329">Datum und Uhrzeit des letzten Neustarts des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-329">Date and time the operating system was last restarted.</span></span>

<span data-ttu-id="eb6d5-330">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-330">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-331">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-331">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-332">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-333">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-334">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrsystemdate "," MIF. Allgemeine Informationen zu DMTF \| \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-335">Betriebssystemversion des lokalen Datums und der Tageszeit.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-335">Operating system version of the local date and time-of-day.</span></span>

<span data-ttu-id="eb6d5-336">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-336">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-337">**Gebietsschema**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-337">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-338">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-339">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-340">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ iLanguage")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-340">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ILANGUAGE")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-341">Der vom Betriebssystem verwendete sprach Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-341">Language identifier used by the operating system.</span></span> <span data-ttu-id="eb6d5-342">Eine sprach Kennung ist eine standardmäßige internationale numerische Abkürzung für ein Land/eine Region.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-342">A language identifier is a standard international numeric abbreviation for a country/region.</span></span> <span data-ttu-id="eb6d5-343">Jede Sprache verfügt über eine eindeutige Sprach-ID (langid), einen 16-Bit-Wert, der aus einem primären und einem sekundären sprach Bezeichner besteht.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-343">Each language has a unique language identifier (LANGID), a 16-bit value that consists of a primary language identifier and a secondary language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-344">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-344">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-345">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-346">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-347">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-348">Der Name des Betriebssystem Herstellers.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-348">Name of the operating system manufacturer.</span></span> <span data-ttu-id="eb6d5-349">Bei Windows-basierten Systemen ist dieser Wert "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="eb6d5-349">For Windows-based systems, this value is "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-350">**Maxnumofprocesses**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-350">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-351">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-352">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-353">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrsystemmaxprocesses ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-353">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-354">Maximale Anzahl von Prozess Kontexten, die vom Betriebssystem unterstützt werden können.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-354">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="eb6d5-355">Der vom Anbieter festgelegte Standardwert ist 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-355">The default value set by the provider is 4294967295 (0xFFFFFFFF).</span></span> <span data-ttu-id="eb6d5-356">Wenn kein festes Maximum vorhanden ist, sollte der Wert 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-356">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="eb6d5-357">Auf Systemen mit einem maximalen Höchstwert kann dieses Objekt bei der Diagnose von Fehlern helfen, die auftreten, wenn der Höchstwert erreicht ist – wenn dies unbekannt ist, geben Sie 4294967295 (0xFFFFFFFF) ein.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-357">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached—if unknown, enter 4294967295 (0xFFFFFFFF).</span></span>

<span data-ttu-id="eb6d5-358">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-358">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-359">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-359">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-360">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-361">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-362">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-362">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-363">Maximale Anzahl von Arbeitsspeicher in Kilobytes, die einem Prozess zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-363">Maximum number, in kilobytes, of memory that can be allocated to a process.</span></span> <span data-ttu-id="eb6d5-364">Bei Betriebssystemen ohne virtuellen Arbeitsspeicher entspricht dieser Wert in der Regel der Gesamtmenge an physischem Arbeitsspeicher abzüglich dem vom BIOS und dem Betriebssystem verwendeten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-364">For operating systems with no virtual memory, typically this value is equal to the total amount of physical memory minus the memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="eb6d5-365">Bei einigen Betriebssystemen kann dieser Wert unendlich sein. in diesem Fall sollte 0 (null) eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-365">For some operating systems, this value may be infinity, in which case 0 (zero) should be entered.</span></span> <span data-ttu-id="eb6d5-366">In anderen Fällen kann dieser Wert eine Konstante sein, z. b. 2G oder 4G.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-366">In other cases, this value could be a constant, for example, 2G or 4G.</span></span>

<span data-ttu-id="eb6d5-367">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="eb6d5-368">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-368">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-369">**Muilanguages**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-369">**MUILanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-370">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="eb6d5-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-372">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-373">Auf dem Computer installierte Multilingual User Interface Pack (MUI Pack)-Sprachen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-373">Multilingual User Interface Pack (MUI Pack ) languages installed on the computer.</span></span> <span data-ttu-id="eb6d5-374">Beispiel: "en-US".</span><span class="sxs-lookup"><span data-stu-id="eb6d5-374">For example, "en-us".</span></span> <span data-ttu-id="eb6d5-375">MUI Pack Sprachen sind Ressourcen Dateien, die in der englischen Version des Betriebssystems installiert werden können.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-375">MUI Pack languages are resource files that can be installed on the English version of the operating system.</span></span> <span data-ttu-id="eb6d5-376">Wenn eine MUI Pack installiert ist, können Sie die Sprache der Benutzeroberfläche in eine von 33 unterstützten Sprachen ändern.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-376">When an MUI Pack is installed, you can can change the user interface language to one of 33 supported languages.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-377">**Name**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-377">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-378">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-378">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-379">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-380">Betriebssystem Instanz innerhalb eines Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-380">Operating system instance within a computer system.</span></span>

<span data-ttu-id="eb6d5-381">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-381">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-382">**"Numoflicensedusers"**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-382">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-383">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-384">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-385">Anzahl der Benutzerlizenzen für das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-385">Number of user licenses for the operating system.</span></span> <span data-ttu-id="eb6d5-386">Wenn unbegrenzt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-386">If unlimited, enter 0 (zero).</span></span> <span data-ttu-id="eb6d5-387">Wenn unbekannt, geben Sie-1 ein.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-387">If unknown, enter -1.</span></span>

<span data-ttu-id="eb6d5-388">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-388">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-389">**Anzahlungsprozesse**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-389">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-390">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-391">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-392">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrsystemprocesses ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-392">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-393">Anzahl von Prozess Kontexten, die derzeit auf dem Betriebssystem geladen oder ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-393">Number of process contexts currently loaded or running on the operating system.</span></span>

<span data-ttu-id="eb6d5-394">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-394">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-395">**Numofusers**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-395">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-396">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-397">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-398">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrsystemnumusers ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-399">Anzahl der Benutzersitzungen, für die das Betriebssystem derzeit Zustandsinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-399">Number of user sessions for which the operating system is storing state information currently.</span></span>

<span data-ttu-id="eb6d5-400">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-400">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-401">**OperatingSystemSKU**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-401">**OperatingSystemSKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-402">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-403">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-404">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-405">SKU-Nummer (Stock Keeping Unit) für das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-405">Stock Keeping Unit (SKU) number for the operating system.</span></span> <span data-ttu-id="eb6d5-406">Diese Werte sind identisch mit den \**Product \_ \** _-Konstanten, die in "Winnt. h" definiert sind und mit der Funktion " [_ *GetProductInfo* \*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) " verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-406">These values are the same as the \**PRODUCT\_\** _ constants defined in WinNT.h that are used with the [_ *GetProductInfo*\*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span>

<span data-ttu-id="eb6d5-407">In der folgenden Liste werden mögliche SKU-Werte aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-407">The following list lists possible SKU values.</span></span>

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span data-ttu-id="eb6d5-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Produkt \_ Nicht definiert** (0)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUCT\_UNDEFINED** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-409">Nicht definiert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-409">Undefined</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span data-ttu-id="eb6d5-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Produkt \_ Ultimate** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUCT\_ULTIMATE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-411">Ultimate Edition, z. b. Windows Vista Ultimate.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-411">Ultimate Edition, e.g. Windows Vista Ultimate.</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span data-ttu-id="eb6d5-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Produkt \_ Home \_ Basic** (2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUCT\_HOME\_BASIC** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-413">Home Basic Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-413">Home Basic Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span data-ttu-id="eb6d5-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Produkt \_ Home \_ Premium** (3)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUCT\_HOME\_PREMIUM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-415">Home Premium Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-415">Home Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span data-ttu-id="eb6d5-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Produkt \_ Enterprise** (4)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUCT\_ENTERPRISE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-417">Enterprise</span><span class="sxs-lookup"><span data-stu-id="eb6d5-417">Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span data-ttu-id="eb6d5-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Produkt \_ Business** (6)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUCT\_BUSINESS** (6)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-419">Business Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-419">Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span data-ttu-id="eb6d5-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Produkt \_ Standard \_ Server** (7)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUCT\_STANDARD\_SERVER** (7)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-421">Windows Server Standard Edition (Desktop Darstellung-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-421">Windows Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span data-ttu-id="eb6d5-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Produkt \_ Datacenter \_ Server** (8)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUCT\_DATACENTER\_SERVER** (8)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-423">Windows Server Datacenter Edition (Desktop Darstellung-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-423">Windows Server Datacenter Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span data-ttu-id="eb6d5-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Produkt \_ SmallBusiness \_ Server** (9)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUCT\_SMALLBUSINESS\_SERVER** (9)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-425">Small Business Server-Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-425">Small Business Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span data-ttu-id="eb6d5-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Produkt \_ Enterprise \_ Server** (10)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUCT\_ENTERPRISE\_SERVER** (10)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-427">Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-427">Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span data-ttu-id="eb6d5-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Produkt \_ Starter** (11)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUCT\_STARTER** (11)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-429"> Starter Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-429">Starter Edition</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span data-ttu-id="eb6d5-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Produkt \_ Datacenter \_ Server \_ Core** (12)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE** (12)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-431">Datacenter Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-431">Datacenter Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span data-ttu-id="eb6d5-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Produkt \_ Standard \_ Server \_ Core** (13)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUCT\_STANDARD\_SERVER\_CORE** (13)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-433">Standard Server Core-Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-433">Standard Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span data-ttu-id="eb6d5-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Produkt \_ Enterprise \_ Server \_ Core** (14)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE** (14)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-435">Enterprise Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-435">Enterprise Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span data-ttu-id="eb6d5-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Produkt \_ Webserver \_** (17)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUCT\_WEB\_SERVER** (17)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-437">Webserver Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-437">Web Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span data-ttu-id="eb6d5-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Produkt \_ Home \_ Server** (19)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUCT\_HOME\_SERVER** (19)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-439">Home Server Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-439">Home Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span data-ttu-id="eb6d5-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Produkt \_ Storage \_ Express \_ Server** (20)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER** (20)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-441">Storage Express Server-Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-441">Storage Express Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span data-ttu-id="eb6d5-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Produkt \_ Storage \_ Standard \_ Server** (21)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER** (21)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-443">Windows Storage Server Standard Edition (Desktop Darstellung-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-443">Windows Storage Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span data-ttu-id="eb6d5-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Produkt \_ Speicher \_ \_ Arbeitsgruppenserver** (22)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER** (22)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-445">Windows Storage Server Workgroup Edition (Desktop Darstellung Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-445">Windows Storage Server Workgroup Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span data-ttu-id="eb6d5-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Produkt \_ Storage \_ Enterprise \_ Server** (23)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER** (23)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-447">Storage Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-447">Storage Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span data-ttu-id="eb6d5-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Produkt \_ Server \_ für \_ SmallBusiness** (24)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUCT\_SERVER\_FOR\_SMALLBUSINESS** (24)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-449">Server für Small Business Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-449">Server For Small Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span data-ttu-id="eb6d5-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Produkt \_ SmallBusiness \_ Server \_ Premium** (25)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM** (25)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-451">Small Business Server Premium Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-451">Small Business Server Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span data-ttu-id="eb6d5-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Produkt \_ Enterprise \_ N** (27)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUCT\_ENTERPRISE\_N** (27)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-453">Windows Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-453">Windows Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span data-ttu-id="eb6d5-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Produkt \_ Ultimate \_ N** (28)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUCT\_ULTIMATE\_N** (28)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-455">Windows Ultimate-Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-455">Windows Ultimate Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span data-ttu-id="eb6d5-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Produkt \_ Webserver \_ \_ Core** (29)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUCT\_WEB\_SERVER\_CORE** (29)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-457">Windows Server-Webserver Edition (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-457">Windows Server Web Server Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span data-ttu-id="eb6d5-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Produkt \_ Standard \_ Server \_ V** (36)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUCT\_STANDARD\_SERVER\_V** (36)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-459">Windows Server Standard Edition ohne Hyper-V</span><span class="sxs-lookup"><span data-stu-id="eb6d5-459">Windows Server Standard Edition without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span data-ttu-id="eb6d5-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Produkt \_ Datacenter \_ Server \_ V** (37)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUCT\_DATACENTER\_SERVER\_V** (37)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-461">Windows Server Datacenter Edition ohne Hyper-V (vollständige Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-461">Windows Server Datacenter Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span data-ttu-id="eb6d5-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Produkt \_ Enterprise \_ Server \_ V** (38)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_V** (38)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-463">Windows Server Enterprise Edition ohne Hyper-V (vollständige Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-463">Windows Server Enterprise Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span data-ttu-id="eb6d5-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Produkt \_ Datacenter \_ Server \_ Core \_ V** (39)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE\_V** (39)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-465">Windows Server Datacenter Edition ohne Hyper-V (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-465">Windows Server Datacenter Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span data-ttu-id="eb6d5-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Produkt \_ Standard \_ Server \_ Core \_ V** (40)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUCT\_STANDARD\_SERVER\_CORE\_V** (40)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-467">Windows Server Standard Edition ohne Hyper-V (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-467">Windows Server Standard Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span data-ttu-id="eb6d5-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Produkt \_ Enterprise \_ Server \_ Core \_ V** (41)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE\_V** (41)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-469">Windows Server Enterprise Edition ohne Hyper-V (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-469">Windows Server Enterprise Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span data-ttu-id="eb6d5-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Produkt \_ HyperV** (42)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUCT\_HYPERV** (42)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-471">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="eb6d5-471">Microsoft Hyper-V Server</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span data-ttu-id="eb6d5-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Produkt \_ Storage \_ Express \_ Server \_ Core** (43)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER\_CORE** (43)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-473">Storage Server Express Edition (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-473">Storage Server Express Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span data-ttu-id="eb6d5-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Produkt \_ Storage \_ Standard \_ Server \_ Core** (44)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER\_CORE** (44)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-475">Storage Server Standard Edition (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-475">Storage Server Standard Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span data-ttu-id="eb6d5-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Produkt \_ Speicher \_ \_ Arbeitsgruppenserver \_ Core** (45)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER\_CORE** (45)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-477">Storage Server Workgroup Edition (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-477">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span data-ttu-id="eb6d5-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Produkt \_ Storage \_ Enterprise \_ Server \_ Core** (46)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER\_CORE** (46)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-479">Storage Server Workgroup Edition (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-479">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span data-ttu-id="eb6d5-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Produkt \_ Professional** (48)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUCT\_PROFESSIONAL** (48)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-481">Windows Professional</span><span class="sxs-lookup"><span data-stu-id="eb6d5-481">Windows Professional</span></span>

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span data-ttu-id="eb6d5-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Produkt \_ SB- \_ Lösungs \_ Server** (50)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUCT\_SB\_SOLUTION\_SERVER** (50)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-483">Windows Server Essentials (Desktop Darstellung-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-483">Windows Server Essentials (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span data-ttu-id="eb6d5-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Produkt \_ SmallBusiness \_ Server \_ Premium \_ Core** (63)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM\_CORE** (63)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-485">Small Business Server Premium (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-485">Small Business Server Premium (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span data-ttu-id="eb6d5-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Produkt \_ Cluster \_ Server \_ V** (64)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUCT\_CLUSTER\_SERVER\_V** (64)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-487">Windows Compute Cluster Server ohne Hyper-V</span><span class="sxs-lookup"><span data-stu-id="eb6d5-487">Windows Compute Cluster Server without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span data-ttu-id="eb6d5-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Produkt \_ \_Kernarm** (97)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUCT\_CORE\_ARM** (97)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-489">Windows RT</span><span class="sxs-lookup"><span data-stu-id="eb6d5-489">Windows RT</span></span>

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span data-ttu-id="eb6d5-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**Produkt \_ Core** (101)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUCT\_CORE** (101)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-491">Windows-Startseite</span><span class="sxs-lookup"><span data-stu-id="eb6d5-491">Windows Home</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span data-ttu-id="eb6d5-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Produkt \_ Professional \_ WMC** (103)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUCT\_PROFESSIONAL\_WMC** (103)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-493">Windows Professional mit Media Center</span><span class="sxs-lookup"><span data-stu-id="eb6d5-493">Windows Professional with Media Center</span></span>

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span data-ttu-id="eb6d5-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Produkt \_ Mobile \_ Kerne** (104)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUCT\_MOBILE\_CORE** (104)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-495">Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="eb6d5-495">Windows Mobile</span></span>

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span data-ttu-id="eb6d5-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Produkt \_ Iotuap** (123)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUCT\_IOTUAP** (123)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-497">Windows IOT (Internet der Dinge) Core</span><span class="sxs-lookup"><span data-stu-id="eb6d5-497">Windows IoT (Internet of Things) Core</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span data-ttu-id="eb6d5-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Produkt \_ Rechenzentrum \_ Nano \_ Server** (143)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUCT\_DATACENTER\_NANO\_SERVER** (143)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-499">Windows Server Datacenter Edition (Nano Server-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-499">Windows Server Datacenter Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span data-ttu-id="eb6d5-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Produkt \_ Standard \_ Nano \_ Server** (144)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUCT\_STANDARD\_NANO\_SERVER** (144)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-501">Windows Server Standard Edition (Nano Server-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-501">Windows Server Standard Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span data-ttu-id="eb6d5-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Produkt \_ Datacenter \_ WS \_ Server \_ Core** (147)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUCT\_DATACENTER\_WS\_SERVER\_CORE** (147)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-503">Windows Server Datacenter Edition (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-503">Windows Server Datacenter Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span data-ttu-id="eb6d5-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Produkt \_ Standard- \_ WS- \_ Server \_ Core** (148)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUCT\_STANDARD\_WS\_SERVER\_CORE** (148)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-505">Windows Server Standard Edition (Server Core-Installation)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-505">Windows Server Standard Edition (Server Core installation)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-506">**Organisation**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-506">**Organization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-507">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-508">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-508">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-509">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-509">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|RegisteredOrganization")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-510">Der Name des Unternehmens für den registrierten Benutzer des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-510">Company name for the registered user of the operating system.</span></span>

<span data-ttu-id="eb6d5-511">Beispiel: "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-511">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-512">**OSArchitecture**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-512">**OSArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-513">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-513">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-514">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-515">Architektur des Betriebssystems im Gegensatz zum Prozessor.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-515">Architecture of the operating system, as opposed to the processor.</span></span> <span data-ttu-id="eb6d5-516">Diese Eigenschaft kann lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-516">This property can be localized.</span></span>

<span data-ttu-id="eb6d5-517">Beispiel: 32-Bit</span><span class="sxs-lookup"><span data-stu-id="eb6d5-517">Example: 32-bit</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-518">**OSLanguage**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-518">**OSLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-519">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-519">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-520">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-520">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-521">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Default \\ \\ Control Panel \\ \\ International \| locale")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-521">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|DEFAULT\\\\Control Panel\\\\International\|Locale")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-522">Die Sprachversion des installierten Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-522">Language version of the operating system installed.</span></span> <span data-ttu-id="eb6d5-523">In der folgenden Liste sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-523">The following list lists the possible values.</span></span> <span data-ttu-id="eb6d5-524">Beispiel: 0x0807 (Deutsch, Schweiz).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-524">Example: 0x0807 (German, Switzerland).</span></span>

<dt>

<span data-ttu-id="eb6d5-525">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-525">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-526">Arabisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-526">Arabic</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-527">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-527">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-528">Chinesisch (vereinfacht) – China</span><span class="sxs-lookup"><span data-stu-id="eb6d5-528">Chinese (Simplified)– China</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-529">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-529">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-530">Englisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-530">English</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-531">1025 (0x401)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-531">1025 (0x401)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-532">Arabisch – Saudi-Arabien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-532">Arabic – Saudi Arabia</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-533">1026 (0x402)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-533">1026 (0x402)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-534">Bulgarisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-534">Bulgarian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-535">1027 (0x403)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-535">1027 (0x403)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-536">Katalanisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-536">Catalan</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-537">1028 (0x404)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-537">1028 (0x404)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-538">Chinesisch (traditionell) – Taiwan</span><span class="sxs-lookup"><span data-stu-id="eb6d5-538">Chinese (Traditional) – Taiwan</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-539">1029 (0x405)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-539">1029 (0x405)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-540">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-540">Czech</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-541">1030 (0x406)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-541">1030 (0x406)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-542">Dänisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-542">Danish</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-543">1031 (0x407)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-543">1031 (0x407)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-544">Deutsch (Deutschland)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-544">German – Germany</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-545">1032 (0x408)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-545">1032 (0x408)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-546">Griechisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-546">Greek</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-547">1033 (0x409)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-547">1033 (0x409)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-548">Englisch – USA</span><span class="sxs-lookup"><span data-stu-id="eb6d5-548">English – United States</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-549">1034 (0x40a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-549">1034 (0x40A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-550">Spanisch – traditionelle Sortierung</span><span class="sxs-lookup"><span data-stu-id="eb6d5-550">Spanish – Traditional Sort</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-551">1035 (0x40b)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-551">1035 (0x40B)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-552">Finnisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-552">Finnish</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-553">1036 (0x40c)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-553">1036 (0x40C)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-554">Französisch (Frankreich)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-554">French – France</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-555">1037 (0x40d)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-555">1037 (0x40D)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-556">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-556">Hebrew</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-557">1038 (0x40e)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-557">1038 (0x40E)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-558">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-558">Hungarian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-559">1039 (0x40f)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-559">1039 (0x40F)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-560">Isländisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-560">Icelandic</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-561">1040 (0x410)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-561">1040 (0x410)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-562">Italienisch (Italien)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-562">Italian – Italy</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-563">1041 (0x411)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-563">1041 (0x411)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-564">Japanisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-564">Japanese</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-565">1042 (0x412)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-565">1042 (0x412)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-566">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-566">Korean</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-567">1043 (0x413)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-567">1043 (0x413)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-568">Niederländisch (Niederlande)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-568">Dutch – Netherlands</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-569">1044 (0x414)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-569">1044 (0x414)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-570">Norwegisch – Bokmal</span><span class="sxs-lookup"><span data-stu-id="eb6d5-570">Norwegian – Bokmal</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-571">1045 (0x415)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-571">1045 (0x415)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-572">Polnisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-572">Polish</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-573">1046 (0x416)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-573">1046 (0x416)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-574">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-574">Portuguese – Brazil</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-575">1047 (0x417)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-575">1047 (0x417)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-576">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="eb6d5-576">Rhaeto-Romanic</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-577">1048 (0x418)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-577">1048 (0x418)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-578">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-578">Romanian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-579">1049 (0x419)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-579">1049 (0x419)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-580">Russisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-580">Russian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-581">1050 (0x41A)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-581">1050 (0x41A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-582">Kroatisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-582">Croatian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-583">1051 (0x41b)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-583">1051 (0x41B)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-584">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-584">Slovak</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-585">1052 (0x41c)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-585">1052 (0x41C)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-586">Albanisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-586">Albanian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-587">1053 (0x41d)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-587">1053 (0x41D)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-588">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-588">Swedish</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-589">1054 (0x41e)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-589">1054 (0x41E)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-590">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-590">Thai</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-591">1055 (0x41f)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-591">1055 (0x41F)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-592">Türkisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-592">Turkish</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-593">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-593">1056 (0x420)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-594">Urdu</span><span class="sxs-lookup"><span data-stu-id="eb6d5-594">Urdu</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-595">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-595">1057 (0x421)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-596">Indonesisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-596">Indonesian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-597">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-597">1058 (0x422)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-598">Ukrainisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-598">Ukrainian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-599">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-599">1059 (0x423)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-600">Belarussisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-600">Belarusian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-601">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-601">1060 (0x424)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-602">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-602">Slovenian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-603">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-603">1061 (0x425)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-604">Estnisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-604">Estonian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-605">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-605">1062 (0x426)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-606">Lettisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-606">Latvian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-607">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-607">1063 (0x427)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-608">Litauisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-608">Lithuanian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-609">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-609">1065 (0x429)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-610">Persisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-610">Persian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-611">1066 (0x42a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-611">1066 (0x42A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-612">Vietnamesisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-612">Vietnamese</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-613">1069 (0x42d)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-613">1069 (0x42D)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-614">Baskisch (Baskenland)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-614">Basque (Basque)</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-615">1070 (0x42e)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-615">1070 (0x42E)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-616">Serbisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-616">Serbian</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-617">1071 (0x42f)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-617">1071 (0x42F)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-618">Mazedonisch (Nordmazedonien)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-618">Macedonian (North Macedonia)</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-619">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-619">1072 (0x430)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-620">Sutu</span><span class="sxs-lookup"><span data-stu-id="eb6d5-620">Sutu</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-621">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-621">1073 (0x431)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-622">Tsonga</span><span class="sxs-lookup"><span data-stu-id="eb6d5-622">Tsonga</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-623">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-623">1074 (0x432)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-624">Tswana</span><span class="sxs-lookup"><span data-stu-id="eb6d5-624">Tswana</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-625">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-625">1076 (0x434)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-626">Xhosa</span><span class="sxs-lookup"><span data-stu-id="eb6d5-626">Xhosa</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-627">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-627">1077 (0x435)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-628">Zulu</span><span class="sxs-lookup"><span data-stu-id="eb6d5-628">Zulu</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-629">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-629">1078 (0x436)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-630">Afrikaans</span><span class="sxs-lookup"><span data-stu-id="eb6d5-630">Afrikaans</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-631">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-631">1080 (0x438)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-632">Faeroese</span><span class="sxs-lookup"><span data-stu-id="eb6d5-632">Faeroese</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-633">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-633">1081 (0x439)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-634">Hindi</span><span class="sxs-lookup"><span data-stu-id="eb6d5-634">Hindi</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-635">1082 (0x43a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-635">1082 (0x43A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-636">Maltesisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-636">Maltese</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-637">1084 (0x43c)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-637">1084 (0x43C)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-638">Schottisches Gälisch (Vereinigtes Königreich)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-638">Scottish Gaelic (United Kingdom)</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-639">1085 (0x43d)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-639">1085 (0x43D)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-640">Jiddisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-640">Yiddish</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-641">1086 (0x43e)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-641">1086 (0x43E)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-642">Malaiisch – Malaysia</span><span class="sxs-lookup"><span data-stu-id="eb6d5-642">Malay – Malaysia</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-643">2049 (0x801)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-643">2049 (0x801)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-644">Arabisch – Irak</span><span class="sxs-lookup"><span data-stu-id="eb6d5-644">Arabic – Iraq</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-645">2052 (0x804)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-645">2052 (0x804)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-646">Chinesisch (vereinfacht) – Volksrepublik China</span><span class="sxs-lookup"><span data-stu-id="eb6d5-646">Chinese (Simplified) – PRC</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-647">2055 (0x807)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-647">2055 (0x807)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-648">Deutsch – Schweiz</span><span class="sxs-lookup"><span data-stu-id="eb6d5-648">German – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-649">2057 (0x809)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-649">2057 (0x809)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-650">Englisch – Vereinigtes Königreich</span><span class="sxs-lookup"><span data-stu-id="eb6d5-650">English – United Kingdom</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-651">2058 (0x80a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-651">2058 (0x80A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-652">Spanisch – Mexiko</span><span class="sxs-lookup"><span data-stu-id="eb6d5-652">Spanish – Mexico</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-653">2060 (0x80c)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-653">2060 (0x80C)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-654">Französisch – Belgien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-654">French – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-655">2064 (0x810)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-655">2064 (0x810)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-656">Italienisch – Schweiz</span><span class="sxs-lookup"><span data-stu-id="eb6d5-656">Italian – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-657">2067 (0x813)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-657">2067 (0x813)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-658">Niederländisch – Belgien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-658">Dutch – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-659">2068 (0x814)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-659">2068 (0x814)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-660">Norwegisch – Nynorsk</span><span class="sxs-lookup"><span data-stu-id="eb6d5-660">Norwegian – Nynorsk</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-661">2070 (0x816)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-661">2070 (0x816)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-662">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-662">Portuguese – Portugal</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-663">2072 (0x818)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-663">2072 (0x818)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-664">Rumänisch – Republik Moldau</span><span class="sxs-lookup"><span data-stu-id="eb6d5-664">Romanian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-665">2073 (0x819)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-665">2073 (0x819)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-666">Russisch – Republik Moldau</span><span class="sxs-lookup"><span data-stu-id="eb6d5-666">Russian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-667">2074 (0x81a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-667">2074 (0x81A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-668">Serbisch – lateinisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-668">Serbian – Latin</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-669">2077 (0x81d)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-669">2077 (0x81D)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-670">Schwedisch – Finnland</span><span class="sxs-lookup"><span data-stu-id="eb6d5-670">Swedish – Finland</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-671">3073 (0xc01)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-671">3073 (0xC01)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-672">Arabisch – Ägypten</span><span class="sxs-lookup"><span data-stu-id="eb6d5-672">Arabic – Egypt</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-673">3076 (0xc04)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-673">3076 (0xC04)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-674">Chinesisch (traditionell) – Hongkong SAR</span><span class="sxs-lookup"><span data-stu-id="eb6d5-674">Chinese (Traditional) – Hong Kong SAR</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-675">3079 (0xc07)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-675">3079 (0xC07)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-676">Deutsch – Österreich</span><span class="sxs-lookup"><span data-stu-id="eb6d5-676">German – Austria</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-677">3081 (0xc09)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-677">3081 (0xC09)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-678">Englisch – Australien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-678">English – Australia</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-679">3082 (0xc0a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-679">3082 (0xC0A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-680">Spanisch – internationale Sortierung</span><span class="sxs-lookup"><span data-stu-id="eb6d5-680">Spanish – International Sort</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-681">3084 (0xc0c)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-681">3084 (0xC0C)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-682">Französisch – Kanada</span><span class="sxs-lookup"><span data-stu-id="eb6d5-682">French – Canada</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-683">3098 (0xc1a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-683">3098 (0xC1A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-684">Serbisch – Kyrillisch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-684">Serbian – Cyrillic</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-685">4097 (0x1001)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-685">4097 (0x1001)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-686">Arabisch – Libyen</span><span class="sxs-lookup"><span data-stu-id="eb6d5-686">Arabic – Libya</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-687">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-687">4100 (0x1004)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-688">Chinesisch (vereinfacht) – Singapur</span><span class="sxs-lookup"><span data-stu-id="eb6d5-688">Chinese (Simplified) – Singapore</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-689">4103 (0x1007)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-689">4103 (0x1007)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-690">Deutsch – Luxemburg</span><span class="sxs-lookup"><span data-stu-id="eb6d5-690">German – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-691">4105 (0x1009)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-691">4105 (0x1009)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-692">Englisch – Kanada</span><span class="sxs-lookup"><span data-stu-id="eb6d5-692">English – Canada</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-693">4106 (0x100a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-693">4106 (0x100A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-694">Spanisch – Guatemala</span><span class="sxs-lookup"><span data-stu-id="eb6d5-694">Spanish – Guatemala</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-695">4108 (0x100c)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-695">4108 (0x100C)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-696">Französisch – Schweiz</span><span class="sxs-lookup"><span data-stu-id="eb6d5-696">French – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-697">5121 (0x1401)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-697">5121 (0x1401)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-698">Arabisch – Algerien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-698">Arabic – Algeria</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-699">5127 (0x1407)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-699">5127 (0x1407)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-700">Deutsch – Liechtenstein</span><span class="sxs-lookup"><span data-stu-id="eb6d5-700">German – Liechtenstein</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-701">5129 (0x1409)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-701">5129 (0x1409)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-702">Englisch – Neuseeland</span><span class="sxs-lookup"><span data-stu-id="eb6d5-702">English – New Zealand</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-703">5130 (0x140a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-703">5130 (0x140A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-704">Spanisch – Costa Rica</span><span class="sxs-lookup"><span data-stu-id="eb6d5-704">Spanish – Costa Rica</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-705">5132 (0x140c)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-705">5132 (0x140C)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-706">Französisch – Luxemburg</span><span class="sxs-lookup"><span data-stu-id="eb6d5-706">French – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-707">6145 (0x1801)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-707">6145 (0x1801)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-708">Arabisch – Marokko</span><span class="sxs-lookup"><span data-stu-id="eb6d5-708">Arabic – Morocco</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-709">6153 (0x1809)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-709">6153 (0x1809)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-710">Englisch – Irland</span><span class="sxs-lookup"><span data-stu-id="eb6d5-710">English – Ireland</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-711">6154 (0x180a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-711">6154 (0x180A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-712">Spanisch – Panama</span><span class="sxs-lookup"><span data-stu-id="eb6d5-712">Spanish – Panama</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-713">7169 (0x1c01)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-713">7169 (0x1C01)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-714">Arabisch – Tunesien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-714">Arabic – Tunisia</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-715">7177 (0x109)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-715">7177 (0x1C09)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-716">Englisch – Südafrika</span><span class="sxs-lookup"><span data-stu-id="eb6d5-716">English – South Africa</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-717">7178 (0x1c0a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-717">7178 (0x1C0A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-718">Spanisch – Dominikanische Republik</span><span class="sxs-lookup"><span data-stu-id="eb6d5-718">Spanish – Dominican Republic</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-719">8193 (0x2001)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-719">8193 (0x2001)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-720">Arabisch – Oman</span><span class="sxs-lookup"><span data-stu-id="eb6d5-720">Arabic – Oman</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-721">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-721">8201 (0x2009)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-722">Englisch – Jamaika</span><span class="sxs-lookup"><span data-stu-id="eb6d5-722">English – Jamaica</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-723">8202 (0x200a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-723">8202 (0x200A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-724">Spanisch – Venezuela</span><span class="sxs-lookup"><span data-stu-id="eb6d5-724">Spanish – Venezuela</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-725">9217 (0x2401)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-725">9217 (0x2401)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-726">Arabisch – Jemen</span><span class="sxs-lookup"><span data-stu-id="eb6d5-726">Arabic – Yemen</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-727">9226 (0x240 a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-727">9226 (0x240A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-728">Spanisch – Kolumbien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-728">Spanish – Colombia</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-729">10241 (0x2801)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-729">10241 (0x2801)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-730">Arabisch – Syrien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-730">Arabic – Syria</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-731">10249 (0x2809)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-731">10249 (0x2809)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-732">Englisch – Belize</span><span class="sxs-lookup"><span data-stu-id="eb6d5-732">English – Belize</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-733">10250 (0x280a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-733">10250 (0x280A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-734">Spanisch – Peru</span><span class="sxs-lookup"><span data-stu-id="eb6d5-734">Spanish – Peru</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-735">11265 (0x2c01)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-735">11265 (0x2C01)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-736">Arabisch – Jordanien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-736">Arabic – Jordan</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-737">11273 (0x2c09)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-737">11273 (0x2C09)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-738">Englisch – Trinidad</span><span class="sxs-lookup"><span data-stu-id="eb6d5-738">English – Trinidad</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-739">11274 (0x2c0a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-739">11274 (0x2C0A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-740">Spanisch – Argentinien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-740">Spanish – Argentina</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-741">12289 (0x3001)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-741">12289 (0x3001)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-742">Arabisch – Libanon</span><span class="sxs-lookup"><span data-stu-id="eb6d5-742">Arabic – Lebanon</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-743">12298 (0x300a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-743">12298 (0x300A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-744">Spanisch – Ecuador</span><span class="sxs-lookup"><span data-stu-id="eb6d5-744">Spanish – Ecuador</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-745">13313 (0x3401)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-745">13313 (0x3401)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-746">Arabisch – Kuwait</span><span class="sxs-lookup"><span data-stu-id="eb6d5-746">Arabic – Kuwait</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-747">13322 (0x340a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-747">13322 (0x340A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-748">Spanisch – Chile</span><span class="sxs-lookup"><span data-stu-id="eb6d5-748">Spanish – Chile</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-749">14337 (0x3801)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-749">14337 (0x3801)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-750">Arabisch – Vereinigte Arabische Emirate</span><span class="sxs-lookup"><span data-stu-id="eb6d5-750">Arabic – U.A.E.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-751">14346 (0x380a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-751">14346 (0x380A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-752">Spanisch – Uruguay</span><span class="sxs-lookup"><span data-stu-id="eb6d5-752">Spanish – Uruguay</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-753">15361 (0x3c01)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-753">15361 (0x3C01)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-754">Arabisch – Bahrain</span><span class="sxs-lookup"><span data-stu-id="eb6d5-754">Arabic – Bahrain</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-755">15370 (0x3c0a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-755">15370 (0x3C0A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-756">Spanisch – Paraguay</span><span class="sxs-lookup"><span data-stu-id="eb6d5-756">Spanish – Paraguay</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-757">16385 (0x4001)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-757">16385 (0x4001)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-758">Arabisch – Katar</span><span class="sxs-lookup"><span data-stu-id="eb6d5-758">Arabic – Qatar</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-759">16394 (0x400a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-759">16394 (0x400A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-760">Spanisch – Bolivien</span><span class="sxs-lookup"><span data-stu-id="eb6d5-760">Spanish – Bolivia</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-761">17418 (0x440 a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-761">17418 (0x440A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-762">Spanisch – El Salvador</span><span class="sxs-lookup"><span data-stu-id="eb6d5-762">Spanish – El Salvador</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-763">18442 (0x480a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-763">18442 (0x480A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-764">Spanisch – Honduras</span><span class="sxs-lookup"><span data-stu-id="eb6d5-764">Spanish – Honduras</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-765">19466 (0x4c0a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-765">19466 (0x4C0A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-766">Spanisch – Nicaragua</span><span class="sxs-lookup"><span data-stu-id="eb6d5-766">Spanish – Nicaragua</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-767">20490 (0x500a)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-767">20490 (0x500A)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-768">Spanisch – Puerto Rico</span><span class="sxs-lookup"><span data-stu-id="eb6d5-768">Spanish – Puerto Rico</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-769">**OSProductSuite**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-769">**OSProductSuite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-770">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-770">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-771">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-771">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-772">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ PRODUCTOPTIONS \| ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business (restricted)", "Embedded NT", "Data Center")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-772">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\ProductOptions\|ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-773">Installierte und lizenzierte Systemprodukt Erweiterungen für das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-773">Installed and licensed system product additions to the operating system.</span></span> <span data-ttu-id="eb6d5-774">Der Wert 146 (0x92) für **OSProductSuite** zeigt beispielsweise Enterprise, Terminal Services und das Rechenzentrum (Bits 1, vier und sieben) an.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-774">For example, the value of 146 (0x92) for **OSProductSuite** indicates Enterprise, Terminal Services, and Data Center (bits one, four, and seven set).</span></span> <span data-ttu-id="eb6d5-775">In der folgenden Liste sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-775">The following list lists possible values.</span></span>

<dt>

<span data-ttu-id="eb6d5-776">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-776">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-777">Microsoft Small Business Server wurde installiert, kann jedoch auf eine andere Version von Windows aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-777">Microsoft Small Business Server was once installed, but may have been upgraded to another version of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-778">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-778">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-779">Windows Server 2008 Enterprise ist installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-779">Windows Server 2008 Enterprise is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-780">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-780">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-781">Windows BackOffice-Komponenten werden installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-781">Windows BackOffice components are installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-782">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-782">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-783">Der Kommunikations Server ist installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-783">Communication Server is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-784">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-784">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-785">Terminal Dienste sind installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-785">Terminal Services is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-786">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-786">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-787">Microsoft Small Business Server wird mit der eingeschränkten Client Lizenz installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-787">Microsoft Small Business Server is installed with the restrictive client license.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-788">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-788">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-789">Windows Embedded ist installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-789">Windows Embedded is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-790">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-790">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-791">Eine Datacenter Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-791">A Datacenter edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-792">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-792">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-793">Terminal Dienste sind installiert, es wird jedoch nur eine interaktive Sitzung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-793">Terminal Services is installed, but only one interactive session is supported.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-794">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-794">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-795">Windows Home Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-795">Windows Home Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-796">1024 (0x400)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-796">1024 (0x400)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-797">Die Webserver Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-797">Web Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-798">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-798">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-799">Storage Server Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-799">Storage Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-800">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-800">16384 (0x4000)</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-801">Compute Cluster Edition ist installiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-801">Compute Cluster Edition is installed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-802">**OSType**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-802">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-803">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-803">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-804">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-804">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-805">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md)".**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-805">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-806">Typ des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-806">Type of operating system.</span></span> <span data-ttu-id="eb6d5-807">In der folgenden Liste sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-807">The following list identifies the possible values.</span></span>

<span data-ttu-id="eb6d5-808">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-808">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6d5-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eb6d5-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="eb6d5-811"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-812">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="eb6d5-812">MACROS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="eb6d5-813"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="eb6d5-814"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="eb6d5-815"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="eb6d5-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="eb6d5-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="eb6d5-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="eb6d5-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="eb6d5-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="eb6d5-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="eb6d5-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="eb6d5-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="eb6d5-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="eb6d5-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="eb6d5-826"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-826"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="eb6d5-827"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-827"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="eb6d5-828"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-828"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="eb6d5-829"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-829"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="eb6d5-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="eb6d5-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="eb6d5-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="eb6d5-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="eb6d5-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="eb6d5-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="eb6d5-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="eb6d5-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="eb6d5-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="eb6d5-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd>

<span data-ttu-id="eb6d5-840">Solaris</span><span class="sxs-lookup"><span data-stu-id="eb6d5-840">Solaris</span></span>

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="eb6d5-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="eb6d5-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="eb6d5-843"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="eb6d5-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="eb6d5-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="eb6d5-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="eb6d5-847"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-847"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="eb6d5-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="eb6d5-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="eb6d5-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="eb6d5-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="eb6d5-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="eb6d5-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="eb6d5-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="eb6d5-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="eb6d5-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="eb6d5-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="eb6d5-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="eb6d5-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="eb6d5-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="eb6d5-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="eb6d5-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="eb6d5-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="eb6d5-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="eb6d5-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="eb6d5-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="eb6d5-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="eb6d5-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="eb6d5-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="eb6d5-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="eb6d5-871"><span id="OS_390"></span><span id="os_390"></span>**Betriebssystem/390** (60)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="eb6d5-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="eb6d5-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-874">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-874">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-875">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-875">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-876">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-876">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-877">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-877">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-878">Zusätzliche Beschreibung der aktuellen Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-878">Additional description for the current operating system version.</span></span>

<span data-ttu-id="eb6d5-879">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-879">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-880">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-880">**PAEEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-881">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-881">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-882">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-882">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-883">**True** gibt an, dass die physischen Adress Erweiterungen (PE) durch das Betriebssystem aktiviert werden, das auf Intel-Prozessoren ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-883">If **True**, the physical address extensions (PAE) are enabled by the operating system running on Intel processors.</span></span> <span data-ttu-id="eb6d5-884">Mithilfe von "PE" können Anwendungen mehr als 4 GB physischen Arbeitsspeicher adressieren.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-884">PAE allows applications to address more than 4 GB of physical memory.</span></span> <span data-ttu-id="eb6d5-885">Wenn "PE" aktiviert ist, verwendet das Betriebssystem die dreistufige lineare Adressübersetzung anstelle von zwei Ebenen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-885">When PAE is enabled, the operating system uses three-level linear address translation rather than two-level.</span></span> <span data-ttu-id="eb6d5-886">Durch die Bereitstellung von mehr physischem Arbeitsspeicher für eine Anwendung entfällt die Notwendigkeit, Arbeitsspeicher in der Auslagerungs Datei auszutauschen und die Leistung</span><span class="sxs-lookup"><span data-stu-id="eb6d5-886">Providing more physical memory to an application reduces the need to swap memory to the page file and increases performance.</span></span> <span data-ttu-id="eb6d5-887">Verwenden Sie zum Aktivieren von, den Schalter "/PAE-Schalter" in der Boot.ini-Datei.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-887">To enable, PAE, use the "/PAE" switch in the Boot.ini file.</span></span> <span data-ttu-id="eb6d5-888">Weitere Informationen zur Funktion für die physische Adress Erweiterung finden Sie unter <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .</span><span class="sxs-lookup"><span data-stu-id="eb6d5-888">For more information about the Physical Address Extension feature, see <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912>.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-889">**PlusProductID**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-889">**PlusProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-890">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-890">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-891">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-891">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-892">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus!</span><span class="sxs-lookup"><span data-stu-id="eb6d5-892">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="eb6d5-893">ProductID ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-893">ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-894">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-894">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-895">**Plusversionnumber**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-895">**PlusVersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-896">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-896">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-897">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-897">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-898">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus!</span><span class="sxs-lookup"><span data-stu-id="eb6d5-898">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="eb6d5-899">VersionNumber ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-899">VersionNumber")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-900">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-900">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-901">**Portableoperatingsystem**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-901">**PortableOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-902">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-902">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-903">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-903">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-904">Gibt an, ob das Betriebssystem von einem externen USB-Gerät gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-904">Specifies whether the operating system booted from an external USB device.</span></span> <span data-ttu-id="eb6d5-905">True gibt an, dass das Betriebssystem auf einem unterstützten lokal verbundenen Speichergerät gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-905">If true, the operating system has detected it is booting on a supported locally connected storage device.</span></span>

<span data-ttu-id="eb6d5-906">**Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Diese Eigenschaft wird vor Windows 8 und Windows Server 2012 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-906">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-907">**Primärer Server/verwaltete Instanz**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-907">**Primary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-908">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-908">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-909">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-909">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-910">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-910">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-911">Gibt an, ob dies das primäre Betriebssystem ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-911">Specifies whether this is the primary operating system.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-912">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-912">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-913">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-913">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-914">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-914">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-915">Zusätzliche Systeminformationen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-915">Additional system information.</span></span>

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

<span data-ttu-id="eb6d5-916">**Arbeits Station** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-916">**Work Station** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

<span data-ttu-id="eb6d5-917">**Domänen Controller** (2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-917">**Domain Controller** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="eb6d5-918">**Server** (3)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-918">**Server** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-919">**Quantum length**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-919">**QuantumLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-920">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-920">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-921">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eb6d5-921">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-922">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ prioritycontrol \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-922">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-923">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-923">Not supported</span></span>

<span data-ttu-id="eb6d5-924">\* \* Windows Server 2008 und Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="eb6d5-924">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="eb6d5-925">Die **QuantumLength** -Eigenschaft definiert die Anzahl der Takt Ticks pro Quantum.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-925">The **QuantumLength** property defines the number of clock ticks per quantum.</span></span> <span data-ttu-id="eb6d5-926">Ein Quantum ist eine Einheit der Ausführungszeit, die dem Scheduler vor dem Wechsel zu anderen Anwendungen zur Verfügung gestellt werden darf.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-926">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to other applications.</span></span> <span data-ttu-id="eb6d5-927">Wenn ein Thread ein Quantum ausführt, entfernt der Kernel ihn vorzeitig und verschiebt ihn an das Ende einer Warteschlange für Anwendungen mit gleicher Priorität.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-927">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="eb6d5-928">Die tatsächliche Länge des Quantums eines Threads variiert auf verschiedenen Windows-Plattformen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-928">The actual length of a thread's quantum varies across different Windows platforms.</span></span> <span data-ttu-id="eb6d5-929">Nur für Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-929">For Windows NT/Windows 2000 only.</span></span>

<span data-ttu-id="eb6d5-930">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-930">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6d5-931">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-931">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

<span data-ttu-id="eb6d5-932">**Ein Tick** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-932">**One tick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

<span data-ttu-id="eb6d5-933">**Zwei Ticks** (2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-933">**Two ticks** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-934">**Quantum Type**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-934">**QuantumType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-935">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-935">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-936">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eb6d5-936">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-937">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-937">Not supported</span></span>

<span data-ttu-id="eb6d5-938">\* \* Windows Server 2008 und Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="eb6d5-938">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="eb6d5-939">Die **quantumschlag** -Eigenschaft gibt die Quantums mit fester oder variabler Länge an.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-939">The **QuantumType** property specifies either fixed or variable length quantums.</span></span> <span data-ttu-id="eb6d5-940">Windows ist standardmäßig auf Quanten mit variabler Länge festgelegt, wobei die Vordergrund Anwendung ein längeres Quantum als die Hintergrundanwendungen hat.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-940">Windows defaults to variable length quantums where the foreground application has a longer quantum than the background applications.</span></span> <span data-ttu-id="eb6d5-941">Windows Server ist standardmäßig auf Quantums mit fester Länge eingestellt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-941">Windows Server defaults to fixed-length quantums.</span></span> <span data-ttu-id="eb6d5-942">Ein Quantum ist eine Einheit der Ausführungszeit, die dem Scheduler vor dem Wechsel zu einer anderen Anwendung erteilt werden darf.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-942">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to another application.</span></span> <span data-ttu-id="eb6d5-943">Wenn ein Thread ein Quantum ausführt, entfernt der Kernel ihn vorzeitig und verschiebt ihn an das Ende einer Warteschlange für Anwendungen mit gleicher Priorität.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-943">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="eb6d5-944">Die tatsächliche Länge des Quantums eines Threads variiert auf verschiedenen Windows-Plattformen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-944">The actual length of a thread's quantum varies across different Windows platforms.</span></span>

<span data-ttu-id="eb6d5-945">Mögliche Werte sind.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-945">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6d5-946">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-946">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="eb6d5-947">**Korrigiert** (1)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-947">**Fixed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

<span data-ttu-id="eb6d5-948">**Variable** (2)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-948">**Variable** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-949">**RegisteredUser**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-949">**RegisteredUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-950">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-950">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-951">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-952">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| RegisteredOwner")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-952">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|RegisteredOwner")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-953">Der Name des registrierten Benutzers des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-953">Name of the registered user of the operating system.</span></span>

<span data-ttu-id="eb6d5-954">Beispiel: "Ben Smith"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-954">Example: "Ben Smith"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-955">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-955">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-956">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-956">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-957">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-958">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-958">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-959">Serielle Identifikationsnummer des Betriebssystem Produkts.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-959">Operating system product serial identification number.</span></span>

<span data-ttu-id="eb6d5-960">Beispiel: "10497-OEM-0031416-71674"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-960">Example: "10497-OEM-0031416-71674"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-961">**ServicePackMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-961">**ServicePackMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-962">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-962">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-963">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-963">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-964">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-964">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMajor**")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-965">Die Hauptversionsnummer der Service Pack, die auf dem Computersystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-965">Major version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="eb6d5-966">Wenn keine Service Pack installiert wurde, ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-966">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-967">**ServicePackMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-967">**ServicePackMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-968">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-968">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-969">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-969">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-970">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-970">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMinor**")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-971">Die neben Versionsnummer der Service Pack, die auf dem Computersystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-971">Minor version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="eb6d5-972">Wenn keine Service Pack installiert wurde, ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-972">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-973">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-973">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-974">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-974">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-975">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-975">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-976">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF- \| System Arbeitsspeicher-Einstellungen \| 001,3 "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-976">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-977">Gesamtanzahl von Kilobyte, die in den Paging-Dateien des Betriebssystems gespeichert werden können – 0 (null) gibt an, dass keine Auslagerungs Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-977">Total number of kilobytes that can be stored in the operating system paging files—0 (zero) indicates that there are no paging files.</span></span> <span data-ttu-id="eb6d5-978">Beachten Sie, dass diese Zahl nicht die tatsächliche physische Größe der Auslagerungs Datei auf dem Datenträger darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-978">Be aware that this number does not represent the actual physical size of the paging file on disk.</span></span>

<span data-ttu-id="eb6d5-979">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-979">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="eb6d5-980">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-980">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-981">**Status**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-981">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-982">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-982">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-983">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-983">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-984">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-984">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-985">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-985">Current status of the object.</span></span> <span data-ttu-id="eb6d5-986">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-986">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="eb6d5-987">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein intelligent-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber prognostiziert einen Fehler in naher Zukunft).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-987">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="eb6d5-988">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="eb6d5-988">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="eb6d5-989">Der Dienststatus gilt für administrative Aufgaben, z. b. die Spiegelung eines Datenträgers, das erneute Laden einer Benutzer Berechtigungs Liste oder andere administrative Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-989">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="eb6d5-990">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-990">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="eb6d5-991">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-991">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eb6d5-992">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-992">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="eb6d5-993">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-993">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eb6d5-994">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-994">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eb6d5-995">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-995">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="eb6d5-996">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-996">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="eb6d5-997">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-997">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="eb6d5-998">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-998">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="eb6d5-999">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-999">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="eb6d5-1000">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1000">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="eb6d5-1001">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1001">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="eb6d5-1002">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1002">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="eb6d5-1003">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1003">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-1004">**Suitemask**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1004">**SuiteMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1005">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1005">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1006">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1006">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1007">Qualifizierer: [**Bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, BackOffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1007">Qualifiers: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1008">Bitflags, die die im System verfügbaren Produkt Suites identifizieren.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1008">Bit flags that identify the product suites available on the system.</span></span>

<span data-ttu-id="eb6d5-1009">Wenn Sie z. b. "Personal" und "BackOffice" angeben möchten, legen Sie **suitemask** auf `4 | 512` oder fest `516` .</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1009">For example, to specify both Personal and BackOffice, set **SuiteMask** to `4 | 512` or `516`.</span></span>

<dt>

<span data-ttu-id="eb6d5-1010">1</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1010">1</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1011">Kleinunternehmen</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1011">Small Business</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1012">2</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1012">2</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1013">Enterprise</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1013">Enterprise</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1014">4</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1014">4</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1015">Back Office</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1015">BackOffice</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1016">8</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1016">8</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1017">Kommunikation</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1017">Communications</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1018">16</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1018">16</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1019">Terminaldienste</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1019">Terminal Services</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1020">32</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1020">32</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1021">Kleinunternehmen eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1021">Small Business Restricted</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1022">64</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1022">64</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1023">Embedded Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1023">Embedded Edition</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1024">128</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1024">128</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1025">Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1025">Datacenter Edition</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1026">256</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1026">256</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1027">Einzelner Benutzer</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1027">Single User</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1028">512</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1028">512</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1029">Home Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1029">Home Edition</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1030">1024</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1030">1024</span></span>
</dt> <dd>

<span data-ttu-id="eb6d5-1031">Webserver Edition</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1031">Web Server Edition</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eb6d5-1032">**SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1032">**SystemDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1033">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1033">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1034">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1034">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1035">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Registry functions \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| path \| TargetDevice")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1035">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Registry Functions\|[**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring)\|Paths\|TargetDevice")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1036">Die physische Datenträger Partition, auf der das Betriebssystem installiert ist.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1036">Physical disk partition on which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1037">**System Directory**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1037">**SystemDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1038">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1038">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1039">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1039">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1040">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1040">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1041">System Verzeichnis des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1041">System directory of the operating system.</span></span>

<span data-ttu-id="eb6d5-1042">Beispiel: "C: \\ Windows \\ system32"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1042">Example: "C:\\WINDOWS\\SYSTEM32"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1043">**SystemDrive**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1043">**SystemDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1044">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1044">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1045">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1045">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1046">Der Buchstabe des Laufwerks, auf dem sich das Betriebssystem befindet.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1046">Letter of the disk drive on which the operating system resides.</span></span> <span data-ttu-id="eb6d5-1047">Beispiel: "C:"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1047">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1048">**Totaltauapspacesize**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1048">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1049">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1049">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1050">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1050">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1051">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1051">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1052">Gesamter Auslagerungs Bereich in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1052">Total swap space in kilobytes.</span></span> <span data-ttu-id="eb6d5-1053">Dieser Wert kann **null** (nicht angegeben) sein, wenn der Auslagerungs Bereich nicht von den Auslagerungs Dateien unterschieden wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1053">This value may be **NULL** (unspecified) if the swap space is not distinguished from page files.</span></span> <span data-ttu-id="eb6d5-1054">Allerdings unterscheiden einige Betriebssysteme diese Konzepte.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1054">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="eb6d5-1055">Beispielsweise können in UNIX gesamte Prozesse ausgetauscht werden, wenn die freie Seitenliste sinkt und unter dem angegebenen Betrag liegt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1055">For example, in UNIX, whole processes can be swapped out when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="eb6d5-1056">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1056">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="eb6d5-1057">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1057">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1058">**Totalvirtualmemorysize**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1058">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1059">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1059">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1060">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1060">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1061">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1061">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1062">Die Zahl des virtuellen Arbeitsspeichers in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1062">Number, in kilobytes, of virtual memory.</span></span> <span data-ttu-id="eb6d5-1063">Dies kann z. b. durch Hinzufügen des Gesamt RAM zur Größe des Auslagerungs Raums berechnet werden, d. h. durch Hinzufügen der Menge an Arbeitsspeicher, die vom Computersystem der Eigenschaft **SizeStoredInPagingFiles** hinzugefügt oder aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1063">For example, this may be calculated by adding the amount of total RAM to the amount of paging space, that is, adding the amount of memory in or aggregated by the computer system to the property, **SizeStoredInPagingFiles**.</span></span>

<span data-ttu-id="eb6d5-1064">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1064">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="eb6d5-1065">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1065">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1066">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1066">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1067">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1067">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1068">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1068">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1069">Qualifizierer: [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1069">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1070">Gesamtmenge des für das Betriebssystem verfügbaren physischen Speichers in Kilobyte.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1070">Total amount, in kilobytes, of physical memory available to the operating system.</span></span> <span data-ttu-id="eb6d5-1071">Dieser Wert gibt nicht notwendigerweise die tatsächliche Menge an physischem Speicher an, sondern dem Betriebssystem als verfügbar gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1071">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="eb6d5-1072">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1072">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="eb6d5-1073">Diese Eigenschaft wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1073">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1074">**Version**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1074">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1075">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1075">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1076">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1076">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1077">Qualifizierer: [**override**](../wmisdk/standard-qualifiers.md) ("Version"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1077">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwMajorVersion, dwMinorVersion")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1078">Versionsnummer des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1078">Version number of the operating system.</span></span>

<span data-ttu-id="eb6d5-1079">Beispiel: "4,0"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1079">Example: "4.0"</span></span>

</dd> <dt>

<span data-ttu-id="eb6d5-1080">**WindowsDirectory**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1080">**WindowsDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb6d5-1081">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1081">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1082">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1082">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb6d5-1083">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1083">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span></span>
</dt> </dl>

<span data-ttu-id="eb6d5-1084">Windows-Verzeichnis des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1084">Windows directory of the operating system.</span></span>

<span data-ttu-id="eb6d5-1085">Beispiel: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1085">Example: "C:\\WINDOWS"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb6d5-1086">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1086">Remarks</span></span>

<span data-ttu-id="eb6d5-1087">Die **Win32- \_ OperatingSystem** -Klasse wird vom [**CIM- \_ OperatingSystem**](cim-operatingsystem.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1087">The **Win32\_OperatingSystem** class is derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<span data-ttu-id="eb6d5-1088">Jedes Betriebssystem, das auf einem Computer installiert werden kann, auf dem ein Windows-basiertes Betriebssystem ausgeführt werden kann, ist ein Nachfolger oder Mitglied dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1088">Any operating system that can be installed on a computer that can run a Windows-based operating system is a descendant or member of this class.</span></span> <span data-ttu-id="eb6d5-1089">**Win32 \_ "OperatingSystem** " ist eine Singleton-Klasse.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1089">**Win32\_OperatingSystem** is a singleton class.</span></span> <span data-ttu-id="eb6d5-1090">Um die einzelne Instanz zu erhalten, verwenden Sie "@" für den Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1090">To get the single instance, use "@" for the key.</span></span>

<span data-ttu-id="eb6d5-1091">Im Gegensatz zu den meisten anderen WMI-Klassen, die von Mgmtclassgen generiert werden, gibt die **OperatingSystem. kreateinstance**()-Methode ein leeres **OperatingSystem** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1091">Unlike most of the other WMI classes generated by MgmtClassGen, the **OperatingSystem.CreateInstance**() method will return a blank **OperatingSystem** object.</span></span> <span data-ttu-id="eb6d5-1092">Wenn Sie also C \# mit Mgmtclassgen verwenden, können Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1092">Therefore, if you are using C\# with MgmtClassGen, you can use the following code:</span></span>


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a><span data-ttu-id="eb6d5-1093">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1093">Examples</span></span>

<span data-ttu-id="eb6d5-1094">Ein VBScript-Beispiel, das Betriebssystem-und Prozessor Daten von [**Win32 \_ Computersystem**](win32-computersystem.md), [**Win32 \_ Processor**](win32-processor.md)und **Win32 \_ OperatingSystem** erhält, finden Sie in den Beispielen für das [**Win32- \_ Prozessor**](win32-processor.md) Thema.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1094">You can find a VBScript example that obtains operating system and processor data from [**Win32\_ComputerSystem**](win32-computersystem.md), [**Win32\_Processor**](win32-processor.md), and **Win32\_OperatingSystem** in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="eb6d5-1095">Im Beispiel " [Generieren von Exchange-Umgebungs Berichten mithilfe von PowerShell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell" in der TechNet Gallery wird eine **Win32- \_ OperatingSystem** -Klasse als Teil einer größeren Anwendung verwendet, um Exchange-Umgebungs Berichte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1095">The [Generate Exchange Environment Reports using Powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell sample on TechNet Gallery uses a **Win32\_OperatingSystem** class as part of a larger application to generate exchange environment reports.</span></span>

<span data-ttu-id="eb6d5-1096">Das Beispiel [Server-Betriebszeit mithilfe von WMI (Server Betriebszeit](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) ) in der TechNet Gallery verwendet die **LastBootUpTime** -Eigenschaft, um zu bestimmen, wie lange der Server aktiv war.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1096">The [Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) sample in the TechNet Gallery uses the **LastBootupTime** property to determine how long the server has been active.</span></span> <span data-ttu-id="eb6d5-1097">Im Beispiel wird auch die Timeout Option verwendet, um sicherzustellen, dass der WMI-Befehl nicht reagiert.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1097">The sample also uses the timeout option to ensure that the WMI call does not hang.</span></span>

<span data-ttu-id="eb6d5-1098">Das VBScript-Codebeispiel für den [WMI-Informations](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) Abruf in der TechNet-Galerie verwendet die **Win32- \_ OperatingSystem** -Klasse, um Betriebssysteminformationen von einer Reihe von Remote Computern abzurufen.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1098">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_OperatingSystem** class to retrieve OS information from a number of remote computers.</span></span>

<span data-ttu-id="eb6d5-1099">Das folgende Skript ruft die Instanzen des **Win32- \_ OperatingSystems** im Standard \\ Namespace "root CIMv2" ab und zeigt dann Informationen zum Betriebssystem an.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1099">The following script obtains the instances of **Win32\_OperatingSystem** in the default "Root\\CIMv2" namespace, and then displays information about the operating system.</span></span>


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="eb6d5-1100">Im folgenden PowerShell-Codebeispiel werden alle Betriebsinformationen zum aktuellen Betriebssystem angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1100">The following PowerShell code sample displays all the operating information about the current OS.</span></span>


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a><span data-ttu-id="eb6d5-1101">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1101">Requirements</span></span>



| <span data-ttu-id="eb6d5-1102">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1102">Requirement</span></span> | <span data-ttu-id="eb6d5-1103">Wert</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1103">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb6d5-1104">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1104">Minimum supported client</span></span><br/> | <span data-ttu-id="eb6d5-1105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1105">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb6d5-1106">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1106">Minimum supported server</span></span><br/> | <span data-ttu-id="eb6d5-1107">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1107">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb6d5-1108">Namespace</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1108">Namespace</span></span><br/>                | <span data-ttu-id="eb6d5-1109">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1109">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb6d5-1110">MOF</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1110">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb6d5-1111"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="eb6d5-1111"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb6d5-1112">DLL</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1112">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb6d5-1113"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb6d5-1113"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb6d5-1114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb6d5-1115">**CIM- \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1115">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="eb6d5-1116">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1116">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="eb6d5-1117">WMI-Tasks: Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1117">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[<span data-ttu-id="eb6d5-1118">WMI-Tasks: Computer Hardware</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1118">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[<span data-ttu-id="eb6d5-1119">WMI-Tasks: Desktop Verwaltung</span><span class="sxs-lookup"><span data-stu-id="eb6d5-1119">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
