---
description: Stellt ein Gerät dar, das mit einem Computer verbunden ist, auf dem unter einem Microsoft Windows-Betriebssystem ausgeführt wird, das ein gedruckte Bild oder einen Text auf einem Papier oder einem anderen Medium
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Win32_Printer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48fc170cb3e85d44dc3e01140fe2c881a7ec975b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214162"
---
# <a name="win32_printer-class"></a><span data-ttu-id="ef0b8-103">Win32- \_ Drucker Klasse</span><span class="sxs-lookup"><span data-stu-id="ef0b8-103">Win32\_Printer class</span></span>

<span data-ttu-id="ef0b8-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) des **Win32- \_ Druckers** stellt ein Gerät dar, das mit einem Computer verbunden ist, der unter einem Microsoft Windows-Betriebssystem ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="ef0b8-104">The **Win32\_Printer** [WMI class](../wmisdk/retrieving-a-class.md) represents a device connected to a computer running on a Microsoft Windows operating system that can produce a printed image or text on paper or other medium.</span></span>

<span data-ttu-id="ef0b8-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0b8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef0b8-106">Syntax</span></span>

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a><span data-ttu-id="ef0b8-107">Member</span><span class="sxs-lookup"><span data-stu-id="ef0b8-107">Members</span></span>

<span data-ttu-id="ef0b8-108">Die **Win32- \_ Drucker** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ef0b8-108">The **Win32\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="ef0b8-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="ef0b8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="ef0b8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef0b8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ef0b8-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="ef0b8-111">Methods</span></span>

<span data-ttu-id="ef0b8-112">Die **Win32- \_ Drucker** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-112">The **Win32\_Printer** class has these methods.</span></span>



| <span data-ttu-id="ef0b8-113">Methode</span><span class="sxs-lookup"><span data-stu-id="ef0b8-113">Method</span></span>                                                                               | <span data-ttu-id="ef0b8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef0b8-114">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef0b8-115">**"AddPrinterConnection"**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-115">**AddPrinterConnection**</span></span>](addprinterconnection-method-in-class-win32-printer.md)   | <span data-ttu-id="ef0b8-116">Fügt eine Verbindung zum Drucker hinzu.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-116">Adds a connection to the printer.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="ef0b8-117">**Cancelalljobs**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-117">**CancelAllJobs**</span></span>](cancelalljobs-method-in-class-win32-printer.md)                 | <span data-ttu-id="ef0b8-118">Bricht alle Aufträge ab.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-118">Cancels all jobs.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="ef0b8-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-119">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="ef0b8-120">Gibt die Sicherheits Beschreibung zurück, die den Zugriff auf den Drucker steuert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-120">Returns the security descriptor that controls access to the printer.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="ef0b8-121">**Anhalten**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-121">**Pause**</span></span>](pause-method-in-class-win32-printer.md)                                 | <span data-ttu-id="ef0b8-122">Hält die Druckwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-122">Pauses the print queue.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="ef0b8-123">**PrintTestpage**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-123">**PrintTestPage**</span></span>](printtestpage-method-in-class-win32-printer.md)                 | <span data-ttu-id="ef0b8-124">Druckt eine Testseite.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-124">Prints a test page.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="ef0b8-125">**Renameprinter**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-125">**RenamePrinter**</span></span>](renameprinter-method-in-class-win32-printer.md)                 | <span data-ttu-id="ef0b8-126">Benennt einen Drucker um.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-126">Renames a printer.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="ef0b8-127">**Zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-127">**Reset**</span></span>                                                                            | <span data-ttu-id="ef0b8-128">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-128">Not implemented.</span></span> <span data-ttu-id="ef0b8-129">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**Reset**](reset-method-in-class-cim-controller.md) -Methode im [**CIM- \_ Drucker**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="ef0b8-129">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/>                 |
| [<span data-ttu-id="ef0b8-130">**Fortsetzen**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-130">**Resume**</span></span>](resume-method-in-class-win32-printer.md)                               | <span data-ttu-id="ef0b8-131">Setzt die angehaltene Drucker Warteschlange fort.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-131">Resumes paused print queue.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="ef0b8-132">**Methode SetDefaultPrinter auf**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-132">**SetDefaultPrinter**</span></span>](setdefaultprinter-method-in-class-win32-printer.md)         | <span data-ttu-id="ef0b8-133">Legt den Standarddrucker fest.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-133">Sets the default printer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="ef0b8-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-134">**SetPowerState**</span></span>                                                                    | <span data-ttu-id="ef0b8-135">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-135">Not implemented.</span></span> <span data-ttu-id="ef0b8-136">Weitere Informationen zur Implementierung dieser Methode finden Sie unter der [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode im [**CIM- \_ Drucker**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="ef0b8-136">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/> |
| [<span data-ttu-id="ef0b8-137">**SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-137">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="ef0b8-138">Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Drucker steuert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-138">Writes an updated version of the security descriptor that controls access to the printer.</span></span><br/>                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="ef0b8-139">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ef0b8-139">Properties</span></span>

<span data-ttu-id="ef0b8-140">Die **Win32- \_ Drucker** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-140">The **Win32\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef0b8-141">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-141">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-144">Bitmap von Attributen für ein Windows-basiertes Druck Gerät.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-144">Bitmap of attributes for a Windows-based printing device.</span></span>

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span data-ttu-id="ef0b8-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**Drucker \_ Attribut in \_ Warteschlange eingereiht** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**PRINTER\_ATTRIBUTE\_QUEUED** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-146">In Warteschlange</span><span class="sxs-lookup"><span data-stu-id="ef0b8-146">Queued</span></span>

<span data-ttu-id="ef0b8-147">Druckaufträge werden gepuffert und in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-147">Print jobs are buffered and queued.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span data-ttu-id="ef0b8-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**Drucker \_ Attribut \_ direkt** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**PRINTER\_ATTRIBUTE\_DIRECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-149">Direkt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-149">Direct</span></span>

<span data-ttu-id="ef0b8-150">Das Dokument, das direkt an den Drucker gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-150">Document to be sent directly to the printer.</span></span> <span data-ttu-id="ef0b8-151">Dieser Wert wird verwendet, wenn Druckaufträge nicht ordnungsgemäß in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-151">This value is used if print jobs are not queued correctly.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span data-ttu-id="ef0b8-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**Drucker \_ \_Standard Attribut** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**PRINTER\_ATTRIBUTE\_DEFAULT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-153">Standard</span><span class="sxs-lookup"><span data-stu-id="ef0b8-153">Default</span></span>

<span data-ttu-id="ef0b8-154">Standarddrucker auf einem Computer.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-154">Default printer on a computer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span data-ttu-id="ef0b8-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**Drucker \_ Attribut frei \_ gegeben** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**PRINTER\_ATTRIBUTE\_SHARED** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-156">Shared</span><span class="sxs-lookup"><span data-stu-id="ef0b8-156">Shared</span></span>

<span data-ttu-id="ef0b8-157">Verfügbar als freigegebene Netzwerkressource.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-157">Available as a shared network resource.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span data-ttu-id="ef0b8-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**Drucker \_ Attribut \_ Netzwerk** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**PRINTER\_ATTRIBUTE\_NETWORK** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-159">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="ef0b8-159">Network</span></span>

<span data-ttu-id="ef0b8-160">An ein Netzwerk angefügt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-160">Attached to a network.</span></span> <span data-ttu-id="ef0b8-161">Wenn sowohl lokale als auch Netzwerk Bits festgelegt sind, weist dies auf einen Netzwerkdrucker hin.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-161">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span data-ttu-id="ef0b8-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**Drucker \_ Attribut \_ ausgeblendet** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**PRINTER\_ATTRIBUTE\_HIDDEN** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-163">Ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="ef0b8-163">Hidden</span></span>

<span data-ttu-id="ef0b8-164">Bei einigen Benutzern im Netzwerk ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-164">Hidden from some users on the network.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span data-ttu-id="ef0b8-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**Drucker \_ \_Lokales Attribut** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**PRINTER\_ATTRIBUTE\_LOCAL** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-166">Lokal</span><span class="sxs-lookup"><span data-stu-id="ef0b8-166">Local</span></span>

<span data-ttu-id="ef0b8-167">Direkt mit einem Computer verbunden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-167">Directly connected to a computer.</span></span> <span data-ttu-id="ef0b8-168">Wenn sowohl lokale als auch Netzwerk Bits festgelegt sind, weist dies auf einen Netzwerkdrucker hin.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-168">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span data-ttu-id="ef0b8-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**Drucker \_ Attribut \_ EnableDevq** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**PRINTER\_ATTRIBUTE\_ENABLEDEVQ** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-170">EnableDevq</span><span class="sxs-lookup"><span data-stu-id="ef0b8-170">EnableDevQ</span></span>

<span data-ttu-id="ef0b8-171">Aktivieren Sie die Warteschlange auf dem Drucker, falls verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-171">Enable the queue on the printer if available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span data-ttu-id="ef0b8-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**Drucker \_ Attribut \_ KeepPrintedJobs** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-173">KeepPrintedJobs</span><span class="sxs-lookup"><span data-stu-id="ef0b8-173">KeepPrintedJobs</span></span>

<span data-ttu-id="ef0b8-174">Der Spooler sollte Dokumente nach dem Drucken nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-174">Spooler should not delete documents after they are printed.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span data-ttu-id="ef0b8-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**Drucker \_ Das Attribut ist \_ \_ \_ zuerst fertig** gestellt (512 (0x200)).</span><span class="sxs-lookup"><span data-stu-id="ef0b8-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-176">Docompletefirst</span><span class="sxs-lookup"><span data-stu-id="ef0b8-176">DoCompleteFirst</span></span>

<span data-ttu-id="ef0b8-177">Startet Aufträge, für die zuerst das Spoolvorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-177">Start jobs that are finished spooling first.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span data-ttu-id="ef0b8-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**Drucker \_ Attribut \_ funktioniert \_ Offline** (1024 (0x400))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**PRINTER\_ATTRIBUTE\_WORK\_OFFLINE** (1024 (0x400))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-179">WorkOffline</span><span class="sxs-lookup"><span data-stu-id="ef0b8-179">WorkOffline</span></span>

<span data-ttu-id="ef0b8-180">Warteschlangen Druckaufträge, wenn kein Drucker verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-180">Queue print jobs when a printer is not available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span data-ttu-id="ef0b8-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**Drucker \_ \_ \_ Bidi-Attribut aktivieren** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**PRINTER\_ATTRIBUTE\_ENABLE\_BIDI** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-182">EnableBIDI</span><span class="sxs-lookup"><span data-stu-id="ef0b8-182">EnableBIDI</span></span>

<span data-ttu-id="ef0b8-183">Aktivieren von bidirektionalem drucken.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-183">Enable bidirectional printing.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span data-ttu-id="ef0b8-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**Drucker \_ \_ \_ Nur** unformatierte Attribute (4096 (0x1000))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**PRINTER\_ATTRIBUTE\_RAW\_ONLY** (4096 (0x1000))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-185">Zulassen, dass nur unformatierte Datentyp Aufträge gespoolte werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-185">Allow only raw data type jobs to be spooled.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span data-ttu-id="ef0b8-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**Drucker \_ \_Veröffentlichtes Attribut** (8192 (0x2000))</span><span class="sxs-lookup"><span data-stu-id="ef0b8-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**PRINTER\_ATTRIBUTE\_PUBLISHED** (8192 (0x2000))</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-187">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="ef0b8-187">Published</span></span>

<span data-ttu-id="ef0b8-188">Veröffentlicht im Netzwerk Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-188">Published in the network directory service.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-189">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-189">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-190">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-191">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-192">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| Betriebsstatus \| 003,5 "," MIB. IETF \| Host-Resources-MIB. hrdevicestatus ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-193">Verfügbarkeit und Status des Geräts.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-193">Availability and status of the device.</span></span>

<span data-ttu-id="ef0b8-194">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ef0b8-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-198">Ausführung oder vollständiger Stromversorgung</span><span class="sxs-lookup"><span data-stu-id="ef0b8-198">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ef0b8-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warnung** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ef0b8-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ef0b8-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ef0b8-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Ausschalten** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ef0b8-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ef0b8-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off-Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ef0b8-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>Herunter **gestuft (10** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ef0b8-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Nicht installiert** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ef0b8-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Installationsfehler** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ef0b8-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Energiespeicher-unbekannt** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-209">Es ist bekannt, dass sich das Gerät in einem Energiesparmodus befindet, aber der genaue Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-209">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ef0b8-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Energiesparmodus-niedriger Energie Modus** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-211">Das Gerät befindet sich in einem Energiespar Zustand, funktioniert jedoch noch nicht, und die Leistung kann beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-211">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ef0b8-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Energiesparmodus-Standby** (15)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-213">Das Gerät funktioniert nicht, kann jedoch schnell in den vollständigen Energiespar Betrieb gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-213">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ef0b8-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Energie Zyklen** (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ef0b8-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Energiespar Speicher-Warnung** (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-216">Das Gerät befindet sich in einem Warn Status, auch wenn es sich im Energiesparmodus befindet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-216">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ef0b8-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angeh** alten (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-218">Das Gerät wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-218">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ef0b8-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Nicht bereit** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-220">Das Gerät ist nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-220">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ef0b8-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Nicht konfiguriert** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-222">Das Gerät ist nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-222">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ef0b8-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>Inaktiven **Status (21** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-224">Das Gerät ist in Ruhe.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-224">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-225">**Availablejobsheets**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-225">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-226">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-226">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-227">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-228">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. Requirements djobsheets")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-228">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-229">Array aller auf einem Drucker verfügbaren Auftrags Blätter.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-229">Array of all the job sheets available on a printer.</span></span> <span data-ttu-id="ef0b8-230">Kann auch verwendet werden, um das Banner zu beschreiben, das ein Drucker am Anfang jedes Auftrags oder andere vom Benutzer angegebene Optionen bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-230">Can also be used to describe the banner that a printer might provide at the beginning of each job, or other user-specified options.</span></span>

<span data-ttu-id="ef0b8-231">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-231">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-232">**AveragePagesPerMinute**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-232">**AveragePagesPerMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-233">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-234">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-235">Die Druck Rate (durchschnittliche Anzahl der Seiten pro Minute), die ein Drucker ausgeben kann.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-235">Printing rate, in average number of pages per minute, that a printer can produce output.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-236">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-236">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-237">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-237">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-239">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)". Capabilitybeschreibungen "," CIM \_ PrintJob. Finish "," CIM \_ printservice. Funktionalitäten ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-239">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-240">Array von Druckerfunktionen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-240">Array of printer capabilities.</span></span>

<span data-ttu-id="ef0b8-241">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-241">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="ef0b8-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="ef0b8-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Druck** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="ef0b8-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="ef0b8-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="ef0b8-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Heften (6** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="ef0b8-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenz Druck** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="ef0b8-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punsch** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="ef0b8-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Abdeckung** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="ef0b8-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="ef0b8-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-und weiß Druck** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="ef0b8-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Eine Seite** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-255">One-Sided</span><span class="sxs-lookup"><span data-stu-id="ef0b8-255">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="ef0b8-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-257">Two-Sided Long-Edge</span><span class="sxs-lookup"><span data-stu-id="ef0b8-257">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="ef0b8-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiges kurzes Edge** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-259">Two-Sided Short Edge</span><span class="sxs-lookup"><span data-stu-id="ef0b8-259">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="ef0b8-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>Hoch **Format (15** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="ef0b8-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Quer** Format (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="ef0b8-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes** Hochformat (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="ef0b8-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrtes quer** Format (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="ef0b8-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Hohe Qualität** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="ef0b8-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality normal** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="ef0b8-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-267">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-267">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-268">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-270">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-270">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-271">Array von Freiform-Zeichen folgen, die ausführliche Erläuterungen **zu den im Funktions Array angegebenen** Drucker Features bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-271">Array of free-form strings that provide detailed explanations for the printer features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="ef0b8-272">Jeder Eintrag dieses Arrays bezieht sich auf einen Eintrag im **Funktions Array, der sich** im selben Index befindet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-272">Each entry of this array is related to an entry in the **Capabilities** array that is located in the same index.</span></span>

<span data-ttu-id="ef0b8-273">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-273">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-274">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-274">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-275">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-276">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-277">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-278">Kurze Beschreibung eines Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-278">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="ef0b8-279">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-279">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-280">**Char* unterstützt*\*</span><span class="sxs-lookup"><span data-stu-id="ef0b8-280">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-281">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-281">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-282">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-283">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. Charset"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| -Drucker-MIB. prtlocalizationcharakterisezeichensatz ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-283">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-284">Array verfügbarer Zeichensätze für die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-284">Array of available character sets for output.</span></span> <span data-ttu-id="ef0b8-285">Zeichen folgen, die in dieser Eigenschaft bereitgestellt werden, müssen der Semantik und Syntax entsprechen, die in RFC 2046 (MIME-Teil 2) und in der IANA-Zeichensatz Registrierung angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-285">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="ef0b8-286">Beispiele hierfür sind "UTF-8", "US-ASCII" und "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="ef0b8-286">Examples include, "UTF-8", "us-ASCII", and "iso-8859-1".</span></span>

<span data-ttu-id="ef0b8-287">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-287">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-288">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-288">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-289">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-290">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-291">Kommentar für eine Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-291">Comment for a print queue.</span></span>

<span data-ttu-id="ef0b8-292">Beispiel: Farbdrucker</span><span class="sxs-lookup"><span data-stu-id="ef0b8-292">Example: Color printer</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-293">**Configmanagererrorcode**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-293">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-294">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-295">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-296">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-297">Win32-Configuration Manager Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-297">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ef0b8-298">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ef0b8-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Dieses Gerät funktioniert ordnungsgemäß.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ef0b8-300"> (0)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-300">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-301">Das Gerät funktioniert ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-301">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ef0b8-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Dieses Gerät ist nicht ordnungsgemäß konfiguriert.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ef0b8-303">(1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-303">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-304">Das Gerät ist nicht ordnungsgemäß konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-304">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ef0b8-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Der Treiber für dieses Gerät kann nicht geladen werden.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ef0b8-306">(2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-306">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ef0b8-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt über wenig Arbeitsspeicher oder andere Ressourcen.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ef0b8-308">(3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-308">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-309">Der Treiber für dieses Gerät ist möglicherweise beschädigt, oder das System verfügt möglicherweise nicht über genügend Arbeitsspeicher oder andere Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-309">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ef0b8-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß. Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ef0b8-311">(4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-311">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-312">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-312">Device is not working properly.</span></span> <span data-ttu-id="ef0b8-313">Einer der Treiber oder die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-313">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ef0b8-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Der Treiber für dieses Gerät benötigt eine Ressource, die von Windows nicht verwaltet werden kann.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ef0b8-315">(5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-315">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-316">Der Treiber für das Gerät erfordert eine Ressource, die von Windows nicht verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-316">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ef0b8-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Die Startkonfiguration für dieses Gerät steht in Konflikt mit anderen Geräten.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ef0b8-318"> (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-318">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-319">Die Startkonfiguration für das Gerät steht in Konflikt mit anderen Geräten.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-319">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ef0b8-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Kann nicht gefiltert werden.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ef0b8-321">(7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-321">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ef0b8-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Das Treiber Lade Modul für das Gerät fehlt.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ef0b8-323">(8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-323">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-324">Das Treiber Lade Modul für das Gerät fehlt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-324">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ef0b8-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da die Steuerungs Firmware die Ressourcen für das Gerät falsch meldet.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ef0b8-326">(9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-326">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-327">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-327">Device is not working properly.</span></span> <span data-ttu-id="ef0b8-328">Die Steuerungs Firmware meldet nicht korrekt die Ressourcen für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-328">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ef0b8-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Dieses Gerät kann nicht gestartet werden.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ef0b8-330">(10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-330">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-331">Das Gerät kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-331">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ef0b8-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Dieses Gerät ist fehlgeschlagen.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ef0b8-333">(11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-333">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-334">Fehler beim Gerät.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-334">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ef0b8-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Auf diesem Gerät können nicht genügend kostenfreie Ressourcen gefunden werden.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ef0b8-336">(12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-336">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-337">Das Gerät kann nicht genug freie Ressourcen für die Verwendung finden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-337">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ef0b8-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Die Ressourcen dieses Geräts können von Windows nicht überprüft werden.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ef0b8-339">(13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-339">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-340">Die Geräte Ressourcen können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-340">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ef0b8-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Dieses Gerät funktioniert erst ordnungsgemäß, wenn Sie den Computer neu starten.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ef0b8-342">(14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-342">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-343">Das Gerät kann erst ordnungsgemäß funktionieren, wenn der Computer neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-343">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ef0b8-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da wahrscheinlich ein Problem mit der erneuten Aufzählung vorliegt.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ef0b8-345">(15)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-345">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-346">Das Gerät funktioniert aufgrund eines möglichen erneuten Aufzählungs Problems nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-346">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ef0b8-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Es können nicht alle von diesem Gerät verwendeten Ressourcen identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ef0b8-348">(16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-348">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-349">In Windows können nicht alle Ressourcen identifiziert werden, die vom Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-349">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ef0b8-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Dieses Gerät fragt nach einem unbekannten Ressourcentyp.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ef0b8-351">(17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-351">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-352">Das Gerät fordert einen unbekannten Ressourcentyp an.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-352">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ef0b8-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Installieren Sie die Treiber für dieses Gerät neu.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ef0b8-354">(18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-354">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-355">Gerätetreiber müssen neu installiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-355">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ef0b8-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Fehler bei Verwendung des VXD-Lade Moduls.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ef0b8-357">(19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-357">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ef0b8-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Möglicherweise ist die Registrierung beschädigt.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ef0b8-359">(20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-359">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-360">Die Registrierung ist möglicherweise beschädigt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-360">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ef0b8-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation. Dieses Gerät wird von Windows entfernt.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ef0b8-362">(21)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-362">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-363">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-363">System failure.</span></span> <span data-ttu-id="ef0b8-364">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-364">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ef0b8-365">Das Gerät wird von Windows entfernt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-365">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ef0b8-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Dieses Gerät ist deaktiviert.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ef0b8-367">(22)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-367">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-368">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-368">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ef0b8-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System Fehler: versuchen Sie, den Treiber für dieses Gerät zu ändern. Wenn dies nicht funktioniert, finden Sie weitere Informationen in der Hardware Dokumentation.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ef0b8-370">(23)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-370">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-371">System Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-371">System failure.</span></span> <span data-ttu-id="ef0b8-372">Wenn das Ändern des Gerätetreibers nicht wirksam ist, lesen Sie die Hardware Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-372">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ef0b8-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Dieses Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ef0b8-374">(24)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-374">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-375">Das Gerät ist nicht vorhanden, funktioniert nicht ordnungsgemäß, oder es sind nicht alle Treiber installiert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-375">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ef0b8-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ef0b8-377">(25)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-377">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-378">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-378">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ef0b8-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Das Gerät wird weiterhin von Windows eingerichtet.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ef0b8-380">(26)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-380">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-381">Das Gerät wird weiterhin von Windows eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-381">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ef0b8-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Dieses Gerät verfügt nicht über eine gültige Protokoll Konfiguration.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ef0b8-383">(27)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-383">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-384">Das Gerät verfügt nicht über eine gültige Protokoll Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-384">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ef0b8-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Die Treiber für dieses Gerät sind nicht installiert.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ef0b8-386">(28)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-386">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-387">Gerätetreiber sind nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-387">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ef0b8-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Dieses Gerät ist deaktiviert, da die Firmware des Geräts ihm nicht die erforderlichen Ressourcen erteilt hat.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ef0b8-389">(29)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-389">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-390">Das Gerät ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-390">Device is disabled.</span></span> <span data-ttu-id="ef0b8-391">Die Gerätefirmware hat nicht die erforderlichen Ressourcen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-391">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ef0b8-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Dieses Gerät verwendet eine interruptanforderungs-Ressource (UNQ), die von einem anderen Gerät verwendet wird.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ef0b8-393">(30)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-393">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-394">Das Gerät verwendet eine UNQ-Ressource, die von einem anderen Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-394">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ef0b8-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Dieses Gerät funktioniert nicht ordnungsgemäß, da Windows die für dieses Gerät erforderlichen Treiber nicht laden kann.**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ef0b8-396">31,5</span><span class="sxs-lookup"><span data-stu-id="ef0b8-396">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-397">Das Gerät funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-397">Device is not working properly.</span></span> <span data-ttu-id="ef0b8-398">Die erforderlichen Gerätetreiber können nicht geladen werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-398">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-399">**Configmanageruserconfig**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-399">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-400">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-401">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-402">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-402">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-403">**True** gibt an, dass das Gerät eine benutzerdefinierte Konfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-403">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ef0b8-404">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-404">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-405">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-405">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-406">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-407">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-408">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-408">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-409">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die zum Erstellen einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-409">Name of the first concrete class to appear in the inheritance chain used to create an instance.</span></span> <span data-ttu-id="ef0b8-410">Bei Verwendung mit anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-410">When used with other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="ef0b8-411">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-412">**Currentfunktionalitäten**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-412">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-413">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-413">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-414">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-415">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-415">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-416">Ein Array von Druckerfunktionen, die derzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-416">Array of printer capabilities that are being used currently.</span></span> <span data-ttu-id="ef0b8-417">Ein Eintrag in dieser Eigenschaft muss ebenfalls im **Funktions Array aufgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-417">An entry in this property must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="ef0b8-418">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-418">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="ef0b8-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="ef0b8-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Druck** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="ef0b8-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="ef0b8-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="ef0b8-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Heften (6** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="ef0b8-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenz Druck** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="ef0b8-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punsch** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="ef0b8-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Abdeckung** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="ef0b8-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="ef0b8-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-und weiß Druck** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="ef0b8-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Eine Seite** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-432">One-Sided</span><span class="sxs-lookup"><span data-stu-id="ef0b8-432">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="ef0b8-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-434">Two-Sided Long-Edge</span><span class="sxs-lookup"><span data-stu-id="ef0b8-434">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="ef0b8-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiges kurzes Edge** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-436">Two-Sided Short Edge</span><span class="sxs-lookup"><span data-stu-id="ef0b8-436">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="ef0b8-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>Hoch **Format (15** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="ef0b8-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Quer** Format (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="ef0b8-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes** Hochformat (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="ef0b8-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrtes quer** Format (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="ef0b8-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Hohe Qualität** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="ef0b8-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality normal** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="ef0b8-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-444">**Currentcharset**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-444">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-445">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-447">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".\**Char* unterstützt\*\*")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-447">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-448">Der Zeichensatz, der derzeit für die Ausgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-448">The character set currently used for output.</span></span> <span data-ttu-id="ef0b8-449">Zeichen folgen, die in dieser Eigenschaft bereitgestellt werden, müssen der Semantik und Syntax entsprechen, die in RFC 2046 (MIME-Teil 2) und in der IANA-Zeichensatz Registrierung angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-449">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="ef0b8-450">Beispiele hierfür sind "UTF-8", "US-ASCII" und "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="ef0b8-450">Examples include "utf-8", "us-ASCII", and iso-8859-1.</span></span>

<span data-ttu-id="ef0b8-451">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-451">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-452">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-452">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-453">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-454">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-455">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)". LanguagesSupported ","**CIM- \_ Drucker**.**Currentmimetype**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-455">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**CurrentMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-456">Aktuell verwendete Druckersprache.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-456">Printer language currently used.</span></span> <span data-ttu-id="ef0b8-457">Die verwendete Sprache muss in der **LanguagesSupported** -Eigenschaft aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-457">The language used must be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="ef0b8-458">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-458">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="ef0b8-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="ef0b8-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="ef0b8-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="ef0b8-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="ef0b8-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**Psprinter** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="ef0b8-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="ef0b8-467"><span id="PPDS"></span><span id="ppds"></span>**Ppds** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="ef0b8-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**Escapep** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="ef0b8-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="ef0b8-470"><span id="DDIF"></span><span id="ddif"></span>**Ddif** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="ef0b8-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**InterPress** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="ef0b8-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="ef0b8-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Zeilendaten** (15)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-474">Linedata</span><span class="sxs-lookup"><span data-stu-id="ef0b8-474">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="ef0b8-475"><span id="MODCA"></span><span id="modca"></span>**Modca** (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-476">Dodca</span><span class="sxs-lookup"><span data-stu-id="ef0b8-476">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="ef0b8-477"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-477"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="ef0b8-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="ef0b8-479"><span id="SPDL"></span><span id="spdl"></span>**Spdl** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="ef0b8-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="ef0b8-481"><span id="PDS"></span><span id="pds"></span>Physischer **(21** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="ef0b8-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="ef0b8-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="ef0b8-484"><span id="DSCDSE"></span><span id="dscdse"></span>**Dscdse** (24)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="ef0b8-485"><span id="WPS"></span><span id="wps"></span>**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="ef0b8-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="ef0b8-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="ef0b8-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="ef0b8-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="ef0b8-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**Decppl** (30)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="ef0b8-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Einfacher Text** (31)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-492">SimpleText</span><span class="sxs-lookup"><span data-stu-id="ef0b8-492">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="ef0b8-493"><span id="NPAP"></span><span id="npap"></span>**Npap** (32)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="ef0b8-494"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-494"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="ef0b8-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**beeindrucken** (34)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="ef0b8-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="ef0b8-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="ef0b8-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ef0b8-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch** (38)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="ef0b8-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Seiten** (39)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="ef0b8-501"><span id="LIPS"></span><span id="lips"></span>**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-501"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="ef0b8-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="ef0b8-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (42)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="ef0b8-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CAPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="ef0b8-505"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-505"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="ef0b8-506"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-506"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="ef0b8-507"><span id="XES"></span><span id="xes"></span>**XEs** (46)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-507"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="ef0b8-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="ef0b8-509">48</span><span class="sxs-lookup"><span data-stu-id="ef0b8-509">48</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-510">XPS</span><span class="sxs-lookup"><span data-stu-id="ef0b8-510">XPS</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-511">49</span><span class="sxs-lookup"><span data-stu-id="ef0b8-511">49</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-512">HPGL2</span><span class="sxs-lookup"><span data-stu-id="ef0b8-512">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-513">50</span><span class="sxs-lookup"><span data-stu-id="ef0b8-513">50</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-514">Pclxl</span><span class="sxs-lookup"><span data-stu-id="ef0b8-514">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-515">**Currentmimetype**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-515">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-516">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-517">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-518">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-518">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-519">Der MIME-Typ, der zurzeit verwendet wird, wenn **CurrentLanguage** ein MIME-Typ ist (Wert = 47).</span><span class="sxs-lookup"><span data-stu-id="ef0b8-519">MIME type currently being used if the **CurrentLanguage** is a MIME type (value = 47).</span></span>

<span data-ttu-id="ef0b8-520">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-520">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-521">**Currentnaturallanguage**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-521">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-522">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-523">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-524">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**Naturallanguagessupported**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-524">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-525">Die Sprache, die der Drucker zurzeit für die Verwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-525">Language that the printer is using for management currently.</span></span> <span data-ttu-id="ef0b8-526">Die hier aufgeführte Sprache muss auch in der Eigenschaft **naturallanguagessupported** aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-526">The language listed here must also be listed in the **NaturalLanguagesSupported** property.</span></span>

<span data-ttu-id="ef0b8-527">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-527">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-528">**Currentpapertype**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-528">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-529">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-530">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-531">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**Taschen typesavailable**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-531">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-532">Der Typ des Papiers, das der Drucker verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-532">Type of paper the printer is using.</span></span> <span data-ttu-id="ef0b8-533">Muss in der von der ISO/IEC 10175-Dokument Druckanwendung (dpa) angegebenen Form ausgedrückt werden, die in Anhang C von RFC 1759 (Drucker-MIB) zusammengefasst ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-533">Must be expressed in the form specified by the ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

<span data-ttu-id="ef0b8-534">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-534">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-535">**Standard**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-535">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-536">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-536">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-537">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-538">**True** gibt an, dass der Drucker der Standarddrucker ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-538">If **TRUE**, the printer is the default printer.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-539">**Default-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-539">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-540">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-540">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-541">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-542">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-542">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-543">Ein Array der standardmäßig verwendeten Druckerfunktionen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-543">Array of the printer capabilities used by default.</span></span> <span data-ttu-id="ef0b8-544">Jeder Eintrag im **default-** Funktions Array muss ebenfalls im **Funktions Array aufgeführt** werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-544">Each entry in the **DefaultCapabilities** array must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="ef0b8-545">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-545">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="ef0b8-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Farbdruck** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="ef0b8-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Druck** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="ef0b8-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Kopien** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="ef0b8-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Sortierung** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="ef0b8-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Heften (6** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="ef0b8-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparenz Druck** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="ef0b8-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punsch** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="ef0b8-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Abdeckung** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="ef0b8-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binden** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="ef0b8-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Schwarz-und weiß Druck** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="ef0b8-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Eine Seite** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-559">One-Sided</span><span class="sxs-lookup"><span data-stu-id="ef0b8-559">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="ef0b8-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Zweiseitiger langer Rand** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-561">Two-Sided Long-Edge</span><span class="sxs-lookup"><span data-stu-id="ef0b8-561">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="ef0b8-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Zweiseitiges kurzes Edge** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-563">Two-Sided Short Edge</span><span class="sxs-lookup"><span data-stu-id="ef0b8-563">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="ef0b8-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>Hoch **Format (15** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="ef0b8-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Quer** Format (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="ef0b8-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Umgekehrtes** Hochformat (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="ef0b8-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Umgekehrtes quer** Format (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="ef0b8-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Hohe Qualität** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="ef0b8-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality normal** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="ef0b8-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualität niedrig** (21)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-571">**Defaultkopien**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-571">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-572">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-572">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-573">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-574">Anzahl der Kopien, die für einen Auftrag erstellt wurden – sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-574">Number of copies produced for one job—unless otherwise specified.</span></span>

<span data-ttu-id="ef0b8-575">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-575">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-576">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-576">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-577">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-577">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-578">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-579">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)". LanguagesSupported ","**CIM- \_ Drucker**.**Defaultmimetype**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-579">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**DefaultMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-580">Standarddrucker Sprache.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-580">Default printer language.</span></span> <span data-ttu-id="ef0b8-581">Die hier aufgeführte Sprache muss auch in der **LanguagesSupported** -Eigenschaft aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-581">The language listed here must also be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="ef0b8-582">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-582">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="ef0b8-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="ef0b8-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="ef0b8-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="ef0b8-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="ef0b8-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**Psprinter** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="ef0b8-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="ef0b8-591"><span id="PPDS"></span><span id="ppds"></span>**Ppds** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="ef0b8-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**Escapep** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="ef0b8-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="ef0b8-594"><span id="DDIF"></span><span id="ddif"></span>**Ddif** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="ef0b8-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**InterPress** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="ef0b8-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="ef0b8-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Zeilendaten** (15)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-598">Linedata</span><span class="sxs-lookup"><span data-stu-id="ef0b8-598">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="ef0b8-599"><span id="MODCA"></span><span id="modca"></span>**Modca** (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-600">Dodca</span><span class="sxs-lookup"><span data-stu-id="ef0b8-600">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="ef0b8-601"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-601"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="ef0b8-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="ef0b8-603"><span id="SPDL"></span><span id="spdl"></span>**Spdl** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="ef0b8-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="ef0b8-605"><span id="PDS"></span><span id="pds"></span>Physischer **(21** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="ef0b8-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="ef0b8-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="ef0b8-608"><span id="DSCDSE"></span><span id="dscdse"></span>**Dscdse** (24)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="ef0b8-609"><span id="WPS"></span><span id="wps"></span>**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="ef0b8-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="ef0b8-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="ef0b8-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="ef0b8-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="ef0b8-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**Decppl** (30)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="ef0b8-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Einfacher Text** (31)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-616">SimpleText</span><span class="sxs-lookup"><span data-stu-id="ef0b8-616">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="ef0b8-617"><span id="NPAP"></span><span id="npap"></span>**Npap** (32)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="ef0b8-618"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-618"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="ef0b8-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**beeindrucken** (34)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="ef0b8-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="ef0b8-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="ef0b8-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ef0b8-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch** (38)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="ef0b8-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Seiten** (39)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="ef0b8-625"><span id="LIPS"></span><span id="lips"></span>**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-625"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="ef0b8-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="ef0b8-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (42)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="ef0b8-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CAPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="ef0b8-629"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-629"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="ef0b8-630"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-630"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="ef0b8-631"><span id="XES"></span><span id="xes"></span>**XEs** (46)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-631"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="ef0b8-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="ef0b8-633">48</span><span class="sxs-lookup"><span data-stu-id="ef0b8-633">48</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-634">XPS</span><span class="sxs-lookup"><span data-stu-id="ef0b8-634">XPS</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-635">49</span><span class="sxs-lookup"><span data-stu-id="ef0b8-635">49</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-636">HPGL2</span><span class="sxs-lookup"><span data-stu-id="ef0b8-636">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-637">50</span><span class="sxs-lookup"><span data-stu-id="ef0b8-637">50</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-638">Pclxl</span><span class="sxs-lookup"><span data-stu-id="ef0b8-638">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-639">**Defaultmimetype**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-639">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-640">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-641">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-642">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-642">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-643">MIME-Typ, der zurzeit verwendet wird, wenn der **defaultLanguage** -Wert ein MIME-Typ ist (Wert = 47).</span><span class="sxs-lookup"><span data-stu-id="ef0b8-643">MIME type currently being used, if the **DefaultLanguage** value is a MIME type (value = 47).</span></span>

<span data-ttu-id="ef0b8-644">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-644">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-645">**Defaultnummerieren**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-645">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-646">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-646">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-647">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-648">Anzahl der Druckdaten Strom Seiten, die der Drucker auf einem Medien Blatt rendert – es sei denn, ein Auftrag gibt andernfalls an.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-648">Number of print-stream pages that the printer renders on one media sheet—unless a job specifies otherwise.</span></span>

<span data-ttu-id="ef0b8-649">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-649">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-650">**Defaultpapertype**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-650">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-651">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-652">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-653">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**Taschen typesavailable**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-653">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-654">Papiertyp, den der Drucker verwendet – es sei denn, ein Druckauftrag gibt einen anderen Papiertyp an.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-654">Paper type that the printer uses—unless a print job specifies a different paper type.</span></span> <span data-ttu-id="ef0b8-655">Die Zeichenfolge muss in dem Format ausgedrückt werden, das von der ISO/IEC 1017-Dokument Druckanwendung (dpa) angegeben wird, die in Anhang C von [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Drucker-MIB) zusammengefasst ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-655">The string must be expressed in the form specified by ISO/IEC 1017 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span>

<span data-ttu-id="ef0b8-656">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-656">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-657">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-657">**DefaultPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-658">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-658">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-659">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-659">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-660">Der jedem Druckauftrag zugewiesene Standard Prioritätswert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-660">Default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-661">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-661">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-662">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-663">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-664">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-664">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-665">Die Beschreibung eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-665">Description of an object.</span></span>

<span data-ttu-id="ef0b8-666">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-666">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-667">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-667">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-668">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-668">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-669">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-669">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-670">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**ErrorInformation**"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" MIB. IETF \| -Drucker-MIB. hrprinterdetectederrorstate ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-670">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-671">Drucker Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-671">Printer error information.</span></span>

<span data-ttu-id="ef0b8-672">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-672">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-673">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-673">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-674">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-674">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="ef0b8-675">**Kein Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-675">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="ef0b8-676">**Niedriges Papier** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-676">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="ef0b8-677">**Kein Papier** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-677">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="ef0b8-678">**Niedriger Toner** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-678">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="ef0b8-679">**Kein Toner** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-679">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="ef0b8-680">**Tür geöffnet** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-680">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="ef0b8-681">**Jammed** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-681">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="ef0b8-682">**Offline** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-682">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="ef0b8-683">**Angeforderter Dienst** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-683">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="ef0b8-684">**Ausgabe bin voll** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-684">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-685">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-685">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-686">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-687">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-688">Qualifizierer: [ **CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-688">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-689">Eindeutiger Bezeichner des Druckers auf einem System.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-689">Unique identifier of the printer on a system.</span></span>

<span data-ttu-id="ef0b8-690">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-690">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-691">**Direkt**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-691">**Direct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-692">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-692">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-693">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-693">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-694">Wenn der Wert **true** ist, wird der Druckauftrag direkt an den Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-694">If **TRUE**, the print job is sent directly to the printer.</span></span> <span data-ttu-id="ef0b8-695">Wenn der Wert **false** ist, wird der Druckauftrag gespoolte.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-695">If **FALSE**, the print job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-696">**Docompletefirst**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-696">**DoCompleteFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-697">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-697">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-698">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-698">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-699">**True** gibt an, dass der Drucker Aufträge startet, die das Spoolvorgang abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-699">If **TRUE**, the printer starts jobs that are finished spooling.</span></span> <span data-ttu-id="ef0b8-700">Wenn der Wert **false** ist, startet der Drucker Aufträge in der Reihenfolge, in der die Aufträge empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-700">If **FALSE**, the printer starts jobs in the order that the jobs are received.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-701">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-701">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-702">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-702">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-703">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-703">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-704">Der Name des Windows-Druckertreibers.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-704">Name of the Windows printer driver.</span></span>

<span data-ttu-id="ef0b8-705">Beispiel: Windows-Faxtreiber</span><span class="sxs-lookup"><span data-stu-id="ef0b8-705">Example: Windows Fax Driver</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-706">**EnableBIDI**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-706">**EnableBIDI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-707">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-707">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-708">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-708">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-709">**True** gibt an, dass der Drucker bidirektional drucken kann.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-709">If **TRUE**, the printer can print bidirectionally.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-710">**Enabledevqueryprint**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-710">**EnableDevQueryPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-711">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-711">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-712">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-712">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-713">**True** gibt an, dass der Drucker Dokumente in der Warteschlange speichert, wenn Dokument-und Drucker Einrichtung nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-713">If **TRUE**, the printer holds documents in the queue when document and printer setups do not match.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-714">**Errorgelöscht**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-714">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-715">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-715">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-716">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-716">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-717">**True** gibt an, dass der in **LastErrorCode** gemeldete Fehler gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-717">If **TRUE**, the error reported in **LastErrorCode** has been cleared.</span></span>

<span data-ttu-id="ef0b8-718">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-718">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-719">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-719">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-720">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-720">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-721">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-721">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-722">Informationen über den Fehler, der in **LastErrorCode** aufgezeichnet wurde, sowie Informationen zu Korrekturmaßnahmen, die ergriffen werden können.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-722">Information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="ef0b8-723">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-723">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-724">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-724">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-725">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-725">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-726">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-726">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-727">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)".**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-727">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-728">Array zusätzlicher Informationen für den aktuellen Fehlerstatus, der in **DetectedErrorState** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-728">Array of supplemental information for the current error state indicated in **DetectedErrorState**.</span></span>

<span data-ttu-id="ef0b8-729">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-729">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-730">**ExtendedDetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-730">**ExtendedDetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-731">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-731">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-732">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-732">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-733">Meldet Standardfehler Informationen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-733">Reports standard error information.</span></span> <span data-ttu-id="ef0b8-734">Zusätzliche Informationen sollten in **DetectedErrorState** aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-734">Additional information should be recorded in **DetectedErrorState**.</span></span>

<span data-ttu-id="ef0b8-735">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="ef0b8-735">Values are:</span></span>

<dt>

<span data-ttu-id="ef0b8-736">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-736">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-737">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-737">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-738">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-738">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-739">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="ef0b8-739">Other</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-740">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-740">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-741">Kein Fehler</span><span class="sxs-lookup"><span data-stu-id="ef0b8-741">No Error</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-742">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-742">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-743">Wenig Papier</span><span class="sxs-lookup"><span data-stu-id="ef0b8-743">Low Paper</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-744">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-744">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-745">Kein Papier</span><span class="sxs-lookup"><span data-stu-id="ef0b8-745">No Paper</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-746">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-746">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-747">Wenig Toner</span><span class="sxs-lookup"><span data-stu-id="ef0b8-747">Low Toner</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-748">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-748">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-749">Kein Toner</span><span class="sxs-lookup"><span data-stu-id="ef0b8-749">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-750">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-750">7 (0x7)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-751">Gerät geöffnet</span><span class="sxs-lookup"><span data-stu-id="ef0b8-751">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-752">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-752">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-753">Papierstau</span><span class="sxs-lookup"><span data-stu-id="ef0b8-753">Jammed</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-754">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-754">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-755">Angeforderter Dienst</span><span class="sxs-lookup"><span data-stu-id="ef0b8-755">Service Requested</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-756">10 (0xa)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-756">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-757">Ausgabeschacht voll</span><span class="sxs-lookup"><span data-stu-id="ef0b8-757">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-758">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-758">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-759">Papier Problem</span><span class="sxs-lookup"><span data-stu-id="ef0b8-759">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-760">12 (0xc)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-760">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-761">Seite kann nicht gedruckt werden</span><span class="sxs-lookup"><span data-stu-id="ef0b8-761">Cannot Print Page</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-762">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-762">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-763">Benutzereingriff erforderlich</span><span class="sxs-lookup"><span data-stu-id="ef0b8-763">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-764">14 (0xe)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-764">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-765">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="ef0b8-765">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-766">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-766">15 (0xF)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-767">Unbekannter Server</span><span class="sxs-lookup"><span data-stu-id="ef0b8-767">Server Unknown</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-768">**Extendedprinterstatus**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-768">**ExtendedPrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-769">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-769">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-770">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-770">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-771">Status Informationen für einen Drucker, der sich von den in der **Availability** -Eigenschaft angegebenen Informationen unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-771">Status information for a printer that is different from information specified in the **Availability** property.</span></span>

<dt>

<span data-ttu-id="ef0b8-772">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-772">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-773">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="ef0b8-773">Other</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-774">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-774">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-775">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-775">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-776">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-776">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-777">Idle</span><span class="sxs-lookup"><span data-stu-id="ef0b8-777">Idle</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-778">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-778">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-779">Drucken</span><span class="sxs-lookup"><span data-stu-id="ef0b8-779">Printing</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-780">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-780">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-781">Aufwärmphase</span><span class="sxs-lookup"><span data-stu-id="ef0b8-781">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-782">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-782">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-783">Druckvorgang wurde beendet</span><span class="sxs-lookup"><span data-stu-id="ef0b8-783">Stopped Printing</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-784">7</span><span class="sxs-lookup"><span data-stu-id="ef0b8-784">7</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-785">Offline</span><span class="sxs-lookup"><span data-stu-id="ef0b8-785">Offline</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-786">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-786">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-787">Angehalten</span><span class="sxs-lookup"><span data-stu-id="ef0b8-787">Paused</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-788">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-788">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-789">Fehler</span><span class="sxs-lookup"><span data-stu-id="ef0b8-789">Error</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-790">10 (0xa)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-790">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-791">Busy</span><span class="sxs-lookup"><span data-stu-id="ef0b8-791">Busy</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-792">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-792">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-793">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-793">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-794">12 (0xc)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-794">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-795">Warten</span><span class="sxs-lookup"><span data-stu-id="ef0b8-795">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-796">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-796">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-797">Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="ef0b8-797">Processing</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-798">14 (0xe)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-798">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-799">Initialisierung</span><span class="sxs-lookup"><span data-stu-id="ef0b8-799">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-800">15</span><span class="sxs-lookup"><span data-stu-id="ef0b8-800">15</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-801">Energiespar Speicher</span><span class="sxs-lookup"><span data-stu-id="ef0b8-801">Power Save</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-802">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-802">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-803">Löschen steht aus</span><span class="sxs-lookup"><span data-stu-id="ef0b8-803">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-804">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-804">17 (0x11)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-805">E/a aktiv</span><span class="sxs-lookup"><span data-stu-id="ef0b8-805">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-806">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-806">18 (0x12)</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-807">Manueller Feed</span><span class="sxs-lookup"><span data-stu-id="ef0b8-807">Manual Feed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-808">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-808">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-809">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-809">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-810">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-810">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-811">**True** gibt an, dass der Drucker für Netzwerk Benutzer ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-811">If **TRUE**, the printer is hidden from network users.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-812">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-812">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-813">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-813">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-814">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-814">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-815">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Pixel pro Zoll")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-815">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-816">Horizontale Auflösung des Druckers – in Pixel pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-816">Horizontal resolution of the printer—in pixels per inch.</span></span>

<span data-ttu-id="ef0b8-817">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-817">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-818">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-818">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-819">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-819">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-820">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-820">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-821">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-821">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-822">Datum und Uhrzeit der Installation eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-822">Date and time an object was installed.</span></span> <span data-ttu-id="ef0b8-823">Das-Objekt kann installiert werden, ohne dass ein Wert in diese Eigenschaft geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-823">The object may be installed without a value being written to this property.</span></span> <span data-ttu-id="ef0b8-824">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-824">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-825">**Jobzählset**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-825">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-826">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-826">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-827">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-827">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-828">Qualifizierer: **Counter**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-828">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-829">Anzahl der Druckaufträge seit dem letzten Zurücksetzen des Druckers.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-829">Number of print jobs since the printer was last reset.</span></span>

<span data-ttu-id="ef0b8-830">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-830">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-831">**KeepPrintedJobs**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-831">**KeepPrintedJobs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-832">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-832">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-833">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-833">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-834">**True** gibt an, dass der Druck Spooler die abgeschlossenen Aufträge nicht löscht.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-834">If **TRUE**, the print spooler does not delete the completed jobs.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-835">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-835">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-836">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-836">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-837">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-837">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-838">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| -Drucker-MIB. prtinterpreterlangfamily ") [**, modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)". Mimetypessupported "," CIM \_ PrintJob. language "," CIM \_ printservice. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-838">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-839">Array der Druck Sprachen, das nativ unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-839">Array of the print languages natively supported.</span></span>

<span data-ttu-id="ef0b8-840">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-840">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="ef0b8-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="ef0b8-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="ef0b8-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="ef0b8-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="ef0b8-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**Psprinter** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="ef0b8-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="ef0b8-849"><span id="PPDS"></span><span id="ppds"></span>**Ppds** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="ef0b8-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**Escapep** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="ef0b8-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="ef0b8-852"><span id="DDIF"></span><span id="ddif"></span>**Ddif** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="ef0b8-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**InterPress** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="ef0b8-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="ef0b8-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Zeilendaten** (15)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-856">Linedata</span><span class="sxs-lookup"><span data-stu-id="ef0b8-856">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="ef0b8-857"><span id="MODCA"></span><span id="modca"></span>**Modca** (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-858">Dodca</span><span class="sxs-lookup"><span data-stu-id="ef0b8-858">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="ef0b8-859"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-859"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="ef0b8-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="ef0b8-861"><span id="SPDL"></span><span id="spdl"></span>**Spdl** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="ef0b8-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="ef0b8-863"><span id="PDS"></span><span id="pds"></span>Physischer **(21** )</span><span class="sxs-lookup"><span data-stu-id="ef0b8-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="ef0b8-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="ef0b8-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="ef0b8-866"><span id="DSCDSE"></span><span id="dscdse"></span>**Dscdse** (24)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="ef0b8-867"><span id="WPS"></span><span id="wps"></span>**Wps** (25)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="ef0b8-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="ef0b8-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="ef0b8-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="ef0b8-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="ef0b8-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**Decppl** (30)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="ef0b8-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Einfacher Text** (31)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-874">SimpleText</span><span class="sxs-lookup"><span data-stu-id="ef0b8-874">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="ef0b8-875"><span id="NPAP"></span><span id="npap"></span>**Npap** (32)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="ef0b8-876"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-876"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="ef0b8-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**beeindrucken** (34)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="ef0b8-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="ef0b8-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="ef0b8-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ef0b8-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch** (38)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="ef0b8-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Seiten** (39)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="ef0b8-883"><span id="LIPS"></span><span id="lips"></span>**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-883"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="ef0b8-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="ef0b8-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnose** (42)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="ef0b8-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CAPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="ef0b8-887"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-887"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="ef0b8-888"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-888"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="ef0b8-889"><span id="XES"></span><span id="xes"></span>**XEs** (46)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-889"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="ef0b8-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="ef0b8-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="ef0b8-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="ef0b8-893"><span id="PCLXL"></span><span id="pclxl"></span>**Pclxl** (50)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-894">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-894">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-895">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-895">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-896">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-896">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-897">Der letzte Fehlercode, den das logische Gerät meldet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-897">Last error code that the logical device reports.</span></span>

<span data-ttu-id="ef0b8-898">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-898">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-899">**Lokal**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-899">**Local**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-900">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-900">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-901">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-901">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-902">**True** gibt an, dass der Drucker nicht an ein Netzwerk angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-902">If **TRUE**, the printer is not attached to a network.</span></span> <span data-ttu-id="ef0b8-903">Wenn sowohl die **lokale** als auch die **Netzwerk** Eigenschaft auf **true** festgelegt ist, ist der Drucker ein Netzwerkdrucker.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-903">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-904">**Location**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-904">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-905">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-905">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-906">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-906">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-907">Physischer Speicherort des Druckers.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-907">Physical location of the printer.</span></span>

<span data-ttu-id="ef0b8-908">Beispiel: Bldg.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-908">Example: Bldg.</span></span> <span data-ttu-id="ef0b8-909">38, Raum 1164</span><span class="sxs-lookup"><span data-stu-id="ef0b8-909">38, Room 1164</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-910">**Markingtechnology**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-910">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-911">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-911">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-912">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-913">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| -Drucker-MIB. prtmarkermarktech ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-913">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-914">Markierungs Technologie, die der Drucker verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-914">Marking technology the printer uses.</span></span>

<span data-ttu-id="ef0b8-915">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-915">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-916">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-916">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-917">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-917">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="ef0b8-918">**Elektrophotoled** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-918">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="ef0b8-919">**Elektrofotolaser** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-919">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="ef0b8-920">**Anderes elektrophotographic** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-920">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="ef0b8-921">**Auswirkung verschiebenden Head-Punkt Matrix 9pin** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-921">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="ef0b8-922">Auswirkung der Verschieb **enden Kopf Punkt Matrix 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-922">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="ef0b8-923">Auswirkung der Verschieb **enden Hauptpunkt Matrix** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-923">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="ef0b8-924">Auswirkung der Verschiebungs **Kopfzeile vollständig geformt** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-924">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="ef0b8-925">**Auswirkungs Band** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-925">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="ef0b8-926">**Sonstige Auswirkung** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-926">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="ef0b8-927">**Inkjet-Aqueous** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-927">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="ef0b8-928">**Vollstrahl-Solid** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-928">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="ef0b8-929">**Anderes Inkjet** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-929">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="ef0b8-930">**Stift** (15)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-930">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="ef0b8-931">**Thermische Übertragung** (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-931">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="ef0b8-932">**Thermische sensible** (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-932">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="ef0b8-933">**Thermische Diffusion** (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-933">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="ef0b8-934">**Anderes thermisches** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-934">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="ef0b8-935">**Elektroerosion** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-935">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="ef0b8-936">**Elektrostatisch** (21)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-936">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="ef0b8-937">**Fotomikrofiche** (22)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-937">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="ef0b8-938">**Fotografische imagesesse** (23)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-938">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="ef0b8-939">**Anderes Foto** (24)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-939">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="ef0b8-940">**Ionen Ablage** (25)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-940">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="ef0b8-941">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-941">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="ef0b8-942">**Typesetter** (27)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-942">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-943">**Maxkopien**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-943">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-944">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-944">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-945">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-945">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-946">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. Kopien")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-946">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-947">Maximale Anzahl von Kopien, die der Drucker für einen Auftrag verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-947">Maximum number of copies the printer can produce for one job.</span></span>

<span data-ttu-id="ef0b8-948">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-948">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-949">**Maximal zulässige Anzahl**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-949">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-950">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-950">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-951">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-952">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. numup")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-952">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-953">Maximale Anzahl von Druckdaten Strom Seiten, die der Drucker auf einem Medien Blatt, z. b. Papier, darstellen kann.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-953">Maximum number of print-stream pages the printer can render on one media sheet, such as paper.</span></span>

<span data-ttu-id="ef0b8-954">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-954">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-955">**Maxsizesupportiert**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-955">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-956">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-956">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-957">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-958">Qualifizierer: [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. JobSize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-958">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.JobSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-959">Der größte Auftrag als Bytestream in Kilobyte, den der Drucker annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-959">Largest job as a byte stream, in kilobytes, that the printer can accept.</span></span> <span data-ttu-id="ef0b8-960">Der Wert 0 (null) gibt an, dass keine Begrenzung festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-960">A value of 0 (zero) indicates that no limit is set.</span></span>

<span data-ttu-id="ef0b8-961">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-961">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-962">**Mimetypessupported**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-962">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-963">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-963">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-964">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-964">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-965">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ Drucker**](cim-printer.md)". LanguagesSupported "," CIM \_ PrintJob. mimeTypes "," CIM \_ printservice. mimetypessupported ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-965">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-966">Array detaillierter MIME-Typen Erklärungen, die der Drucker unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-966">Array of detailed MIME-type explanations that the printer supports.</span></span> <span data-ttu-id="ef0b8-967">Wenn Daten bereitgestellt werden, muss der Wert 47 ("MIME") in der **LanguagesSupported** -Eigenschaft enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-967">If data is provided, then the value 47 ("MIME") must be included in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="ef0b8-968">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-968">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-969">**Name**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-969">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-970">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-970">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-971">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-971">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-972">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-972">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-973">Der Name des Druckers.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-973">Name of the printer.</span></span>

<span data-ttu-id="ef0b8-974">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-974">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-975">**Naturallanguagessupported**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-975">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-976">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-976">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-977">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-977">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-978">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| -Drucker-MIB. prtlocalizationlanguage ") [**, modelcorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. NaturalLanguage ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-978">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-979">Array von Sprachen, die für Zeichen folgen unterstützt werden, die der Drucker für die Ausgabe von Verwaltungsinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-979">Array of languages supported for strings that the printer uses for output of management information.</span></span> <span data-ttu-id="ef0b8-980">Muss [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt)entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-980">Must conform to [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span></span> <span data-ttu-id="ef0b8-981">Beispielsweise wird "en" für Englisch verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-981">For example, "en" is used for English.</span></span>

<span data-ttu-id="ef0b8-982">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-982">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-983">**Network**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-983">**Network**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-984">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-984">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-985">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-985">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-986">**True** gibt an, dass der Drucker ein Netzwerkdrucker ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-986">If **TRUE**, the printer is a network printer.</span></span> <span data-ttu-id="ef0b8-987">Wenn sowohl die **lokale** als auch die **Netzwerk** Eigenschaft auf **true** festgelegt ist, ist der Drucker ein Netzwerkdrucker.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-987">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-988">**Unterstützt unterstützt**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-988">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-989">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-989">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-990">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-990">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-991">Array der Papiertypen, die der Drucker unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-991">Array of the paper types that the printer supports.</span></span>

<span data-ttu-id="ef0b8-992">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-992">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="ef0b8-995"><span id="A"></span><span id="a"></span>**A** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-995"><span id="A"></span><span id="a"></span>**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="ef0b8-996"><span id="B"></span><span id="b"></span>**B** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-996"><span id="B"></span><span id="b"></span>**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="ef0b8-997"><span id="C"></span><span id="c"></span>**C** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-997"><span id="C"></span><span id="c"></span>**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="ef0b8-998"><span id="D"></span><span id="d"></span>**D** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-998"><span id="D"></span><span id="d"></span>**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="ef0b8-999"><span id="E"></span><span id="e"></span>**E** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-999"><span id="E"></span><span id="e"></span>**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="ef0b8-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Buchstabe** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="ef0b8-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**Na-10x13-Umschlag** (9)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Na-9x12-Umschlag** (10)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**Na-Number-10-Umschlag** (11)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**Na-7x9-Umschlag** (12)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**Na-9x11-Umschlag** (13)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Na-10x14-Umschlag** (14)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**Na-Number-9-Umschlag** (15)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**Na-6x9-Umschlag** (16)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Na-10x15-Umschlag** (17)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="ef0b8-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="ef0b8-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="ef0b8-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="ef0b8-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="ef0b8-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="ef0b8-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="ef0b8-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="ef0b8-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="ef0b8-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="ef0b8-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="ef0b8-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="ef0b8-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="ef0b8-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="ef0b8-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="ef0b8-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="ef0b8-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="ef0b8-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="ef0b8-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="ef0b8-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="ef0b8-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="ef0b8-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="ef0b8-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="ef0b8-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="ef0b8-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1035">C2</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1035">C2</span></span>

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="ef0b8-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1037">C3</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1037">C3</span></span>

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="ef0b8-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1039">C4</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1039">C4</span></span>

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="ef0b8-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1041">C5</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1041">C5</span></span>

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="ef0b8-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1043">C6</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1043">C6</span></span>

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="ef0b8-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1045">C7</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1045">C7</span></span>

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="ef0b8-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-bestimmt** (47)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-Designated** (47)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1047">C8</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1047">C8</span></span>

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="ef0b8-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1049">ISO-Designated</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1049">ISO-Designated</span></span>

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="ef0b8-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1051">JIS B0</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1051">JIS B0</span></span>

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="ef0b8-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1053">JIS B1</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1053">JIS B1</span></span>

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="ef0b8-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1055">JIS B2</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1055">JIS B2</span></span>

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="ef0b8-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1057">JIS B3</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1057">JIS B3</span></span>

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="ef0b8-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1059">JIS B4</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1059">JIS B4</span></span>

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="ef0b8-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1061">JIS B5</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1061">JIS B5</span></span>

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="ef0b8-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1063">JIS B6</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1063">JIS B6</span></span>

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="ef0b8-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS-B8** (56)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1065">JIS B7</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1065">JIS B7</span></span>

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="ef0b8-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1067">JIS-B8</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1067">JIS B8</span></span>

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="ef0b8-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS-B10** (58)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1069">JIS-B9</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1069">JIS B9</span></span>

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="ef0b8-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Na-Buchstabe** (59)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-Letter** (59)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1071">JIS-B10</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1071">JIS B10</span></span>

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="ef0b8-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**Na-legal** (60)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Umschlag** (61)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Umschlag** (62)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Umschlag** (63)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Umschlag** (64)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Umschlag** (65)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Umschlag** (66)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>Festgelegt **-langer Umschlag** (67)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="ef0b8-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-Umschlag** (68)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="ef0b8-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="ef0b8-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folien** (70)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="ef0b8-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Rechnung** (71)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="ef0b8-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="ef0b8-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-1086">**Taschenbuch verfügbar**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1086">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1087">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1087">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1088">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1088">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1089">Qualifizierer: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indiziert"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. Requirements dtaschen Type", "CIM \_ printservice. papertypesavailable"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| -Drucker-MIB. prtinputmedianame ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1089">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1090">Ein Array von Papiertypen, die zurzeit auf dem Drucker verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1090">Array of paper types that are currently available on the printer.</span></span> <span data-ttu-id="ef0b8-1091">Jede Zeichenfolge muss in dem Format ausgedrückt werden, das von der ISO/IEC 10175-Dokument Druckanwendung (dpa) angegeben wird. Dies wird in Anhang C von [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Drucker-MIB) zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1091">Each string must be expressed in the format specified by ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span> <span data-ttu-id="ef0b8-1092">Jedes Papierformat, das in dieser Eigenschaft identifiziert wird, muss auch in der Eigenschaft "Eigenschaft von" **unterstützt werden** .</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1092">Any paper size identified in this property must also appear in the **PaperSizesSupported** property.</span></span>

<span data-ttu-id="ef0b8-1093">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1093">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<span data-ttu-id="ef0b8-1094">Beispiel: ISO-A4-farbig</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1094">Example: iso-a4-colored</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1095">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1095">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1096">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1096">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1097">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1097">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1098">Optionale Parameter für den Druck Prozessor.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1098">Optional parameters for the print processor.</span></span>

<span data-ttu-id="ef0b8-1099">Beispiel: "Kopien = 2"</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1099">Example: "Copies=2"</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1100">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1100">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1101">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1101">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1102">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1102">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1103">Qualifizierer: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1103">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1104">Windows Plug & Play Geräte Bezeichner des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1104">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="ef0b8-1105">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1105">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ef0b8-1106">Beispiel: \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1106">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1107">**Portname**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1107">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1108">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1108">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1109">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1109">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1110">Port, der zum Übertragen von Daten an einen Drucker verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1110">Port that is used to transmit data to a printer.</span></span> <span data-ttu-id="ef0b8-1111">Wenn ein Drucker mit mehr als einem Port verbunden ist, werden die Namen der einzelnen Ports durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1111">If a printer is connected to more than one port, the names of each port are separated by commas.</span></span>

<span data-ttu-id="ef0b8-1112">Beispiel: LPT1:, LPT2:, LPT3:</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1112">Example: LPT1:, LPT2:, LPT3:</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1113">**Powermanagementfunktionen**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1113">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1114">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1116">Array der spezifischen energiebezogenen Funktionen eines logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1116">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ef0b8-1117">Diese Eigenschaft wird von **CIM \_ LogicalDevice** geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1117">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ef0b8-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ef0b8-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ef0b8-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1122">Die Energie Verwaltungsfunktionen sind zurzeit aktiviert, aber der genaue Featuresatz ist unbekannt, oder die Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1122">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ef0b8-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Automatisch eingegebene Energiespar Modi** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1124">Das Gerät kann seinen Energiezustand basierend auf der Verwendung oder anderen Kriterien ändern.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1124">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ef0b8-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Einsetzbaren Energiezustand** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1126">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1126">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ef0b8-1127">Diese Methode wird in der übergeordneten **CIM \_ LogicalDevice** -Klasse gefunden und kann implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1127">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ef0b8-1128">Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1128">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ef0b8-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Unterstützung für Power Cycling** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1130">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1130">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ef0b8-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Unterstützte Unterstützung** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1132">Zeitgesteuerte Power-On unterstützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1132">Timed Power-On Supported</span></span>

<span data-ttu-id="ef0b8-1133">Die [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) -Methode kann aufgerufen werden, wenn der *PowerState* -Parameter auf 5 (Power Cycle) und die *Uhrzeit* auf ein bestimmtes Datum und eine bestimmte Uhrzeit bzw. ein bestimmtes Intervall festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1133">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-1134">**Powermanagementsupported**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1134">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1135">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1137">Wenn der Wert **true** ist, kann die Leistungsfähigkeit des Geräts verwaltet werden, was bedeutet, dass es in den Unterbrechungs Modus versetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1137">If **TRUE**, the power of the device can be managed, which means that it can be put into suspend mode.</span></span> <span data-ttu-id="ef0b8-1138">Die-Eigenschaft gibt nicht an, dass die Energie Verwaltungsfunktionen aktiviert sind, sondern nur, dass das logische Gerät für die Energie Verwaltung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1138">The property does not indicate that power management features are enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="ef0b8-1139">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1140">**Printerpapernames**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1140">**PrinterPaperNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1141">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1143">Array von Papiergrößen, die vom Drucker unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1143">Array of paper sizes supported by the printer.</span></span> <span data-ttu-id="ef0b8-1144">Die druckerspezifischen Namen werden zur Darstellung unterstützter Papiergrößen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1144">The printer-specified names are used to represent supported paper sizes.</span></span>

<span data-ttu-id="ef0b8-1145">Beispiel: B5 (JIS)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1145">Example: B5 (JIS)</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1146">**PrinterState**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1146">**PrinterState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1149">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1149">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1150">Einer der möglichen Zustände im Zusammenhang mit diesem Drucker.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1150">One of the possible states relating to this printer.</span></span> <span data-ttu-id="ef0b8-1151">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1151">This property is obsolete.</span></span> <span data-ttu-id="ef0b8-1152">Verwenden Sie anstelle dieser Eigenschaft **printerstatus**.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1152">In place of this property, use **PrinterStatus**.</span></span>

<dt>

<span data-ttu-id="ef0b8-1153">0</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1153">0</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1154">Im Leerlauf: Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1154">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1155">1</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1155">1</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1156">Angehalten</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1156">Paused</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1157">2</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1157">2</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1158">Fehler</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1158">Error</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1159">3</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1159">3</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1160">Löschen steht aus</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1160">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1161">4</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1161">4</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1162">Papierstau</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1162">Paper Jam</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1163">5</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1163">5</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1164">Papier out</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1164">Paper Out</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1165">6</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1165">6</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1166">Manueller Feed</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1166">Manual Feed</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1167">7</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1167">7</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1168">Papier Problem</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1168">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1169">8</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1169">8</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1170">Offline</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1170">Offline</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1171">9</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1171">9</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1172">E/a aktiv</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1172">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1173">10</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1173">10</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1174">Busy</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1174">Busy</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1175">11</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1175">11</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1176">Drucken</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1176">Printing</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1177">12</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1177">12</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1178">Ausgabeschacht voll</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1178">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1179">13</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1179">13</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1180">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1180">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1181">14</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1181">14</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1182">Warten</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1182">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1183">15</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1183">15</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1184">Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1184">Processing</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1185">16</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1185">16</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1186">Initialisierung</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1186">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1187">17</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1187">17</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1188">Aufwärmphase</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1188">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1189">18</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1189">18</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1190">Toner niedrig</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1190">Toner Low</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1191">19</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1191">19</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1192">Kein Toner</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1192">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1193">20</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1193">20</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1194">Seiten Punt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1194">Page Punt</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1195">21</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1195">21</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1196">Benutzereingriff erforderlich</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1196">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1197">22</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1197">22</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1198">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1198">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1199">23</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1199">23</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1200">Gerät geöffnet</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1200">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1201">24</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1201">24</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1202">\_Unbekannter Server</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1202">Server\_Unknown</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1203">25</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1203">25</span></span>
</dt> <dd>

<span data-ttu-id="ef0b8-1204">Energiespar Speicher</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1204">Power Save</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-1205">**Printerstatus**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1205">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1206">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1207">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1208">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| -Drucker-MIB. hrprinterstatus ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1209">Status Informationen für einen Drucker, der sich von den in der **Verfügbarkeits** Eigenschaft logischer Geräte angegebenen Informationen unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1209">Status information for a printer that is different from information specified in the logical device **Availability** property.</span></span>

<span data-ttu-id="ef0b8-1210">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1210">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="ef0b8-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>Im **Leerlauf** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1214">Im Leerlauf: Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1214">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="ef0b8-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Drucken** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="ef0b8-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Aufwärm** Dauer (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Warmup** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ef0b8-1217">Aufwärmphase</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1217">Warming Up</span></span>

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="ef0b8-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Druck beendet** (6)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="ef0b8-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-1220">**PrintJobDataType**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1220">**PrintJobDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1222">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1223">Der Datentyp eines Druckauftrags, der auf das Windows-basierte Druck Gerät wartet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1223">Data type of a print job waiting for the Windows-based printing device.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1224">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1224">**PrintProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1225">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1226">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1227">Der Name des Druck Spoolers, der Druckaufträge verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1227">Name of the print spooler that handles print jobs.</span></span>

<span data-ttu-id="ef0b8-1228">Beispiel: SPOOLSS.DLL</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1228">Example: SPOOLSS.DLL</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1229">**Priority**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1229">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1230">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1231">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1232">Priorität des Druckers.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1232">Priority of the printer.</span></span> <span data-ttu-id="ef0b8-1233">Aufträge mit einem Drucker höherer Priorität werden zuerst geplant.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1233">Jobs on a higher priority printer are scheduled first.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1234">**Enes**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1234">**Published**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1235">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1236">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1237">**True** gibt an, dass der Drucker im Netzwerk Verzeichnisdienst veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1237">If **TRUE**, the printer is published in the network directory service.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1238">**In Warteschlange**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1238">**Queued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1239">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1240">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1241">**True** gibt an, dass Druckaufträge vom Drucker gepuffert und in Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1241">If **TRUE**, the printer buffers and queues print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1242">**Raweinzierl**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1242">**RawOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1243">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1244">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1245">**True** gibt an, dass der Drucker nur unformatierte Daten für die spoolunterstützung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1245">If **TRUE**, the printer accepts only raw data to be spooled.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1246">**SeparatorFile**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1246">**SeparatorFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1247">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1248">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1249">Der Name der Datei, die zum Erstellen einer Trenn Zeichenseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1249">Name of the file used to create a separator page.</span></span> <span data-ttu-id="ef0b8-1250">Diese Seite wird verwendet, um Druckaufträge, die an den Drucker gesendet werden, zu trennen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1250">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1251">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1251">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1253">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1254">Der Name des Servers, der den Drucker steuert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1254">Name of the server that controls the printer.</span></span> <span data-ttu-id="ef0b8-1255">Wenn diese Zeichenfolge **null** ist, wird der Drucker lokal gesteuert.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1255">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1256">**Freigegeben**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1256">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1257">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1258">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1258">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1259">**True** gibt an, dass der Drucker als freigegebene Netzwerkressource verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1259">If **TRUE**, the printer is available as a shared network resource.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1260">**ShareName**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1260">**ShareName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1262">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1263">Der Freigabe Name des Windows-basierten Druck Geräts.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1263">Share name of the Windows-based printing device.</span></span>

<span data-ttu-id="ef0b8-1264">Beispiel: " \\ \\ PRINTSERVER1 \\ printer2"</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1264">Example: "\\\\PRINTSERVER1\\PRINTER2"</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1265">**Spoolfähig**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1265">**SpoolEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1266">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1267">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1268">Qualifizierer: [ **veraltet**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1268">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1269">Diese Eigenschaft ist veraltet. Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1269">This property is obsolete; do not use.</span></span> <span data-ttu-id="ef0b8-1270">**True** gibt an, dass Spoolvorgang für den Drucker aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1270">If **TRUE**, spooling is enabled for printer.</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1271">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1271">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1272">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1272">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1273">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1273">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1274">Das Datum und die Uhrzeit, zu der ein Drucker mit dem Drucken eines Auftrags beginnen kann –, wenn der Drucker zu bestimmten Zeiten auf den Druck beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1274">Date and time that a printer can start to print a job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="ef0b8-1275">Dieser Wert wird als die verstrichene Zeit seit 12:00 Uhr GMT (Greenwich Mean Time) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1275">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1276">**Status**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1276">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1277">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1278">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1279">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1279">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1280">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1280">Current status of the object.</span></span> <span data-ttu-id="ef0b8-1281">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1281">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ef0b8-1282">Betriebsstatus sind: **OK**, **herab** gestuft und **pred** -Fehler (ein Element, z. b. ein intelligent-fähiges Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1282">Operational statuses include: **OK**, **Degraded**, and **Pred Fail** (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ef0b8-1283">Nicht operative Status sind: **Fehler**, **starten**, **Beenden** und **Dienst**.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1283">Nonoperational statuses include: **Error**, **Starting**, **Stopping**, and **Service**.</span></span> <span data-ttu-id="ef0b8-1284">Der letztere **Dienst** kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1284">The latter, **Service**, could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ef0b8-1285">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder **OK** noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1285">Not all such work is online, yet the managed element is neither **OK** nor in one of the other states.</span></span>

<span data-ttu-id="ef0b8-1286">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1286">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ef0b8-1287">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1287">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ef0b8-1288">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1288">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ef0b8-1289">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1289">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ef0b8-1290">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1290">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-1291">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1291">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ef0b8-1292">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1292">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ef0b8-1293">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1293">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ef0b8-1294">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1294">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ef0b8-1295">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1295">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ef0b8-1296">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1296">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ef0b8-1297">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1297">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ef0b8-1298">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1298">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ef0b8-1299">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1299">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-1300">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1300">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1301">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1303">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". \|Betriebsstatus DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1304">Der Status des logischen Geräts.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1304">State of the logical device.</span></span> <span data-ttu-id="ef0b8-1305">Wenn diese Eigenschaft nicht für das logische Gerät gilt, sollte der Wert 5 (**nicht zutreffend**) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1305">If this property does not apply to the logical device, the value 5 (**Not Applicable**) should be used.</span></span>

<span data-ttu-id="ef0b8-1306">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ef0b8-1307">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1307">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ef0b8-1308">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1308">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ef0b8-1309">**Aktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1309">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ef0b8-1310">**Deaktiviert** (4)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1310">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ef0b8-1311">**Nicht zutreffend** (5)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1311">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ef0b8-1312">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1312">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1313">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1314">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1315">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1315">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1316">Der Wert der Eigenschaft " **kreationclassname** " des Bereichs Computers.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1316">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="ef0b8-1317">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1318">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1318">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1319">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1320">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1321">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1321">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1322">Der Name des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1322">Name of the scoping system.</span></span>

<span data-ttu-id="ef0b8-1323">Diese Eigenschaft wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1324">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1324">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1325">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1326">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1327">Datum und Uhrzeit der letzten zurück setzung des Druckers.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1327">Date and time the printer was last reset.</span></span>

<span data-ttu-id="ef0b8-1328">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1328">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1329">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1329">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1330">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1331">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1331">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1332">Datum und Uhrzeit, zu der ein Drucker den letzten Auftrag drucken kann –, wenn der Drucker zu bestimmten Zeitpunkten auf den Druck beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1332">Date and time that a printer can print the last job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="ef0b8-1333">Dieser Wert wird als die verstrichene Zeit seit 12:00 Uhr GMT (Greenwich Mean Time) ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1333">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1334">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1334">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1335">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1337">Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Pixel pro Zoll")</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1337">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1338">Vertikale Auflösung des Druckers in Pixel pro Zoll.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1338">Vertical resolution, in pixels-per-inch, of the printer.</span></span>

<span data-ttu-id="ef0b8-1339">Diese Eigenschaft wird vom [**CIM- \_ Drucker**](cim-printer.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1339">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef0b8-1340">**WorkOffline**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1340">**WorkOffline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef0b8-1341">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ef0b8-1342">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1342">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ef0b8-1343">Bei " **true**" können Druckaufträge in die Warteschlange eingereiht werden, wenn der Drucker offline ist.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1343">If **TRUE**, you can queue print jobs on the computer when the printer is offline.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef0b8-1344">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1344">Remarks</span></span>

<span data-ttu-id="ef0b8-1345">Die **Win32- \_ Drucker** Klasse wird vom [**CIM- \_ Drucker**](cim-printer.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1345">The **Win32\_Printer** class is derived from [**CIM\_Printer**](cim-printer.md).</span></span> <span data-ttu-id="ef0b8-1346">Vor dem Aufrufen von " [**\_ errbewbject. Put**](../wmisdk/swbemobject-put-.md) " oder " [**IWbemServices::P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) " für eine **Win32- \_ Drucker** Instanz muss die **SeLoadDriverPrivilege** -Berechtigung (**wbemprivilegeloaddriver** für Visual Basic und LoadDriver für skriptingmoniker) aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1346">Before calling [**SWbemObject.Put\_**](../wmisdk/swbemobject-put-.md) or [**IWbemServices::PutInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) for a **Win32\_Printer** instance, the **SeLoadDriverPrivilege** privilege (**wbemPrivilegeLoadDriver** for Visual Basic and LoadDriver for scripting monikers) must be enabled.</span></span> <span data-ttu-id="ef0b8-1347">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](../wmisdk/privilege-constants.md) und [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1347">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span> <span data-ttu-id="ef0b8-1348">Im folgenden VBScript-Codebeispiel wird gezeigt, wie die **setloaddriverprivilege** -Berechtigung im Skript aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1348">The following VBScript code example shows how to enable the **SetLoadDriverPrivilege** privilege in script.</span></span>

<span data-ttu-id="ef0b8-1349">Verwenden Sie zum Arbeiten mit MSCS-Drucker Clustern die prnadmin.dll-Assembly oder andernfalls den .NET Framework [System. Printing](/dotnet/api/system.printing) -Namespace.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1349">For working with MSCS Printer clusters, use the prnadmin.dll assembly, or else the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



<span data-ttu-id="ef0b8-1350">Windows verwendet die Anmelde Informationen des Benutzers, auf dem das Skript ausgeführt wird, um die verfügbaren Drucker zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1350">Windows uses the credentials of the user running the script to determine what the available printers are.</span></span> <span data-ttu-id="ef0b8-1351">Wenn Sie ein Skript Remote ausführen, können Sie daher nur auf alle Drucker zugreifen, die für Ihr Benutzerkonto auf diesem Remote System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1351">Therefore, if you are running a script remotely, you may only be able to access any printer that is available to your user account on that remote system.</span></span>

<span data-ttu-id="ef0b8-1352">Die **Win32- \_ Drucker** Klasse kann nicht für Drucker in einem MSCS-Druck Cluster verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1352">You cannot use the **Win32\_Printer** class for printers on an MSCS print cluster.</span></span> <span data-ttu-id="ef0b8-1353">Stattdessen müssen Sie möglicherweise entweder das Tool "printeradmin" (PrnAdmin.dll) oder den .NET Framework [System. Printing](/dotnet/api/system.printing) -Namespace verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1353">Instead, you may need to use either the PrinterAdmin tool (PrnAdmin.dll) or the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="ef0b8-1354">Wenn Sie " **printerstatus** = 3" oder " **PrinterState** = 0" abrufen, werden von dem Druckertreiber möglicherweise keine genauen Informationen in die WMI-Datei übertragen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1354">If you are retrieving **PrinterStatus** = 3 or **PrinterState** = 0, the printer driver may not be feeding accurate information into WMI.</span></span> <span data-ttu-id="ef0b8-1355">WMI Ruft die Drucker Informationen aus dem spoolsv.exe Prozess ab.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1355">WMI retrieves the printer information from the spoolsv.exe process.</span></span> <span data-ttu-id="ef0b8-1356">Es ist möglich, dass der Druckertreiber seinen Status nicht an den Spooler meldet.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1356">It is possible the printer driver does not report its status to the spooler.</span></span> <span data-ttu-id="ef0b8-1357">In diesem Fall meldet der **Win32- \_ Drucker** den Drucker als **Leerlauf**.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1357">In this case, **Win32\_Printer** reports the printer as **Idle**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ef0b8-1358">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1358">Examples</span></span>

<span data-ttu-id="ef0b8-1359">Das Beispiel [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell in der TechNet Gallery verwendet den **Win32- \_ Drucker** für die Interaktion mit dem Visio-Automatisierungs Modell, um eine Visio-Zeichnung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1359">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_Printer** to interact with Visio automation model to create a Visio drawing.</span></span>

<span data-ttu-id="ef0b8-1360">Das [PowerShell-Remote-PC](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) -Informations Skript verwendet eine Reihe von Klassen, einschließlich **Win32- \_ Druckern**, um Informationen zu einem Remote Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1360">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) uses a number of classes, including **Win32\_Printer**, to retrieve information about a remote computer.</span></span>

<span data-ttu-id="ef0b8-1361">Im folgenden PowerShell-Codebeispiel wird gezeigt, wie der Standarddrucker des lokalen Computers bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1361">The following PowerShell code sample shows how to determine the default printer of the local computer.</span></span>


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



<span data-ttu-id="ef0b8-1362">Im folgenden VBScript-Codebeispiel wird beschrieben, wie Drucker Statistiken aus Instanzen von **Win32- \_ Druckern** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1362">The following VBScript code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



<span data-ttu-id="ef0b8-1363">Im folgenden perl-Codebeispiel wird beschrieben, wie Drucker Statistiken aus Instanzen von **Win32- \_ Druckern** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1363">The following Perl code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="ef0b8-1364">Im folgenden VBScript-Codebeispiel wird gezeigt, wie der Name des Standard Druckers für einen Computer abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1364">The following VBScript code example shows how to obtain the name of the default printer for a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="ef0b8-1365">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1365">Requirements</span></span>



| <span data-ttu-id="ef0b8-1366">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1366">Requirement</span></span> | <span data-ttu-id="ef0b8-1367">Wert</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1367">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0b8-1368">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1368">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0b8-1369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1369">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ef0b8-1370">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1370">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0b8-1371">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1371">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ef0b8-1372">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1372">Namespace</span></span><br/>                | <span data-ttu-id="ef0b8-1373">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1373">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="ef0b8-1374">MOF</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1374">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef0b8-1375"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ef0b8-1375"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef0b8-1376">DLL</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1376">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef0b8-1377"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef0b8-1377"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ef0b8-1378">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1378">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef0b8-1379">**CIM- \_ Drucker**</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1379">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dt>

[<span data-ttu-id="ef0b8-1380">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1380">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ef0b8-1381">WMI-Tasks: Drucker und Drucken</span><span class="sxs-lookup"><span data-stu-id="ef0b8-1381">WMI Tasks: Printers and Printing</span></span>](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
