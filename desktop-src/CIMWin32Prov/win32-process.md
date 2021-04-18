---
Description: Der Win32- \_ Prozess&\# 32; Die WMI-Klasse stellt einen Prozess in einem Betriebssystem dar.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Win32_Process-Klasse
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371080"
---
# <a name="win32_process-class"></a><span data-ttu-id="7aa74-103">Win32- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="7aa74-103">Win32\_Process class</span></span>

<span data-ttu-id="7aa74-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) für den **Win32- \_ Prozess** stellt einen Prozess in einem Betriebssystem dar.</span><span class="sxs-lookup"><span data-stu-id="7aa74-104">The **Win32\_Process** [WMI class](../wmisdk/retrieving-a-class.md) represents a process on an operating system.</span></span>

<span data-ttu-id="7aa74-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7aa74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

> [!NOTE]
> <span data-ttu-id="7aa74-106">Eine allgemeine Erörterung von Prozessen und Threads in Windows finden Sie im Thema [Prozesse und Threads](/ProcThread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-106">For a general discussion on Processes and Threads within Windows, please see the topic [Processes and Threads](/ProcThread/processes-and-threads.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa74-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aa74-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a><span data-ttu-id="7aa74-108">Member</span><span class="sxs-lookup"><span data-stu-id="7aa74-108">Members</span></span>

<span data-ttu-id="7aa74-109">Die **Win32- \_ Prozess** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7aa74-109">The **Win32\_Process** class has these types of members:</span></span>

-   [<span data-ttu-id="7aa74-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7aa74-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7aa74-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7aa74-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7aa74-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7aa74-112">Methods</span></span>

<span data-ttu-id="7aa74-113">Die **Win32- \_ Prozess** Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-113">The **Win32\_Process** class has these methods.</span></span>



| <span data-ttu-id="7aa74-114">Methode</span><span class="sxs-lookup"><span data-stu-id="7aa74-114">Method</span></span>                                                                   | <span data-ttu-id="7aa74-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7aa74-115">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7aa74-116">**AttachDebugger**</span><span class="sxs-lookup"><span data-stu-id="7aa74-116">**AttachDebugger**</span></span>](attachdebugger-method-in-class-win32-process.md)   | <span data-ttu-id="7aa74-117">Startet den aktuell registrierten Debugger für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="7aa74-117">Launches the currently registered debugger for a process.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="7aa74-118">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="7aa74-118">**Create**</span></span>](create-method-in-class-win32-process.md)                   | <span data-ttu-id="7aa74-119">Erstellt einen neuen Prozess.</span><span class="sxs-lookup"><span data-stu-id="7aa74-119">Creates a new process.</span></span><br/>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="7aa74-120">**Getavailablevirtualsize**</span><span class="sxs-lookup"><span data-stu-id="7aa74-120">**GetAvailableVirtualSize**</span></span>](getavailablevirtualsize-win32-process.md) | <span data-ttu-id="7aa74-121">Ruft die aktuelle Größe des freien virtuellen Adressraums in Bytes ab, der für den Prozess verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7aa74-121">Retrieves the current size, in bytes, of the free virtual address space available to the process.</span></span><br/> <span data-ttu-id="7aa74-122">**Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 und Windows Vista:** Diese Methode wird vor Windows 8.1 und Windows Server 2012 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-122">**Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 and Windows Vista:** This method is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="7aa74-123">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="7aa74-123">**GetOwner**</span></span>](getowner-method-in-class-win32-process.md)               | <span data-ttu-id="7aa74-124">Ruft den Benutzernamen und den Domänen Namen ab, unter dem der Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-124">Retrieves the user name and domain name under which the process is running.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="7aa74-125">**GetOwnerSID**</span><span class="sxs-lookup"><span data-stu-id="7aa74-125">**GetOwnerSid**</span></span>](getownersid-method-in-class-win32-process.md)         | <span data-ttu-id="7aa74-126">Ruft die Sicherheits-ID (SID) für den Besitzer eines Prozesses ab.</span><span class="sxs-lookup"><span data-stu-id="7aa74-126">Retrieves the security identifier (SID) for the owner of a process.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="7aa74-127">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="7aa74-127">**SetPriority**</span></span>](setpriority-method-in-class-win32-process.md)         | <span data-ttu-id="7aa74-128">Ändert die Ausführungs Priorität eines Prozesses.</span><span class="sxs-lookup"><span data-stu-id="7aa74-128">Changes the execution priority of a process.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="7aa74-129">**Terminate**</span><span class="sxs-lookup"><span data-stu-id="7aa74-129">**Terminate**</span></span>](terminate-method-in-class-win32-process.md)             | <span data-ttu-id="7aa74-130">Beendet einen Prozess und alle zugehörigen Threads.</span><span class="sxs-lookup"><span data-stu-id="7aa74-130">Terminates a process and all of its threads.</span></span><br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="7aa74-131">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7aa74-131">Properties</span></span>

<span data-ttu-id="7aa74-132">Die **Win32- \_ Prozess** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7aa74-132">The **Win32\_Process** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7aa74-133">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7aa74-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-136">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7aa74-136">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-137">Kurze Beschreibung eines Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7aa74-137">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="7aa74-138">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-139">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="7aa74-139">**CommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-142">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Befehlszeile zum Starten des Prozesses")</span><span class="sxs-lookup"><span data-stu-id="7aa74-142">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Command Line To Start Process")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-143">Die Befehlszeile, mit der ein bestimmter Prozess gestartet wird, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="7aa74-143">Command line used to start a specific process, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-144">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="7aa74-144">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-147">Qualifizierer: [**CIM- \_ Taste**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Klassen Name")</span><span class="sxs-lookup"><span data-stu-id="7aa74-147">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-148">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-148">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7aa74-149">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-149">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7aa74-150">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-150">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-151">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="7aa74-151">**CreationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-152">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7aa74-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-154">Qualifizierer: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("up date")</span><span class="sxs-lookup"><span data-stu-id="7aa74-154">Qualifiers: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-155">Datum, an dem die Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-155">Date the process begins executing.</span></span>

<span data-ttu-id="7aa74-156">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-156">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-157">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7aa74-157">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-160">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Name der Computer System Klasse ")</span><span class="sxs-lookup"><span data-stu-id="7aa74-160">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-161">Der Name der Erstellungs Klasse des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="7aa74-161">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="7aa74-162">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-162">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-163">**CSName**</span><span class="sxs-lookup"><span data-stu-id="7aa74-163">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-166">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Csname**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")</span><span class="sxs-lookup"><span data-stu-id="7aa74-166">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Name")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-167">Name des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="7aa74-167">Name of the scoping computer system.</span></span>

<span data-ttu-id="7aa74-168">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-168">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-169">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7aa74-169">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-172">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7aa74-172">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-173">Die Beschreibung eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="7aa74-173">Description of an object.</span></span>

<span data-ttu-id="7aa74-174">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-175">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="7aa74-175">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-176">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-177">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-178">Qualifizierer: [**Berechtigungen**](../wmisdk/standard-wmi-qualifiers.md) ("Einstellungs Verzeichnis"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szexepath"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Pfad der ausführbaren Datei")</span><span class="sxs-lookup"><span data-stu-id="7aa74-178">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tool Help Structures\|[**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)\|szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Executable Path")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-179">Pfad zur ausführbaren Datei des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="7aa74-179">Path to the executable file of the process.</span></span>

<span data-ttu-id="7aa74-180">Beispiel: "C: \\ Windows \\ System \\Explorer.Exe"</span><span class="sxs-lookup"><span data-stu-id="7aa74-180">Example: "C:\\Windows\\System\\Explorer.Exe"</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-181">**ExecutionState**</span><span class="sxs-lookup"><span data-stu-id="7aa74-181">**ExecutionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7aa74-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-184">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Ausführungs Status")</span><span class="sxs-lookup"><span data-stu-id="7aa74-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Execution State")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-185">Aktueller Betriebszustand des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="7aa74-185">Current operating condition of the process.</span></span>

<span data-ttu-id="7aa74-186">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-186">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7aa74-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="7aa74-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7aa74-188">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="7aa74-188">Unknown</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7aa74-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="7aa74-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7aa74-190">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="7aa74-190">Other</span></span>

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span data-ttu-id="7aa74-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Bereit** (2)</span><span class="sxs-lookup"><span data-stu-id="7aa74-191"><span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Ready** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="7aa74-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="7aa74-192"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span data-ttu-id="7aa74-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blockiert** (4)</span><span class="sxs-lookup"><span data-stu-id="7aa74-193"><span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Blocked** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7aa74-194">Gesperrt</span><span class="sxs-lookup"><span data-stu-id="7aa74-194">Blocked</span></span>

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span data-ttu-id="7aa74-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Gesperrt** (5)</span><span class="sxs-lookup"><span data-stu-id="7aa74-195"><span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspended Blocked** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span data-ttu-id="7aa74-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>Angeh **alten (6** )</span><span class="sxs-lookup"><span data-stu-id="7aa74-196"><span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspended Ready** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="7aa74-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Beendet** (7)</span><span class="sxs-lookup"><span data-stu-id="7aa74-197"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="7aa74-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Beendet** (8)</span><span class="sxs-lookup"><span data-stu-id="7aa74-198"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span data-ttu-id="7aa74-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Wächst** (9)</span><span class="sxs-lookup"><span data-stu-id="7aa74-199"><span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Growing** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7aa74-200">**Handle**</span><span class="sxs-lookup"><span data-stu-id="7aa74-200">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-201">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-202">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-203">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) ("handle")</span><span class="sxs-lookup"><span data-stu-id="7aa74-203">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-204">Prozess Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7aa74-204">Process identifier.</span></span>

<span data-ttu-id="7aa74-205">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-205">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-206">**HandleCount**</span><span class="sxs-lookup"><span data-stu-id="7aa74-206">**HandleCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-207">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-209">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| Lenker"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("handle count")</span><span class="sxs-lookup"><span data-stu-id="7aa74-209">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle Count")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-210">Die Gesamtanzahl der geöffneten Handles im Besitz des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="7aa74-210">Total number of open handles owned by the process.</span></span> <span data-ttu-id="7aa74-211">" **Lenker count** " ist die Summe der Handles, die zurzeit von jedem Thread in diesem Prozess geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-211">**HandleCount** is the sum of the handles currently open by each thread in this process.</span></span> <span data-ttu-id="7aa74-212">Ein Handle wird verwendet, um die Systemressourcen zu überprüfen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7aa74-212">A handle is used to examine or modify the system resources.</span></span> <span data-ttu-id="7aa74-213">Jedes Handle verfügt über einen Eintrag in einer Tabelle, der intern verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-213">Each handle has an entry in a table that is maintained internally.</span></span> <span data-ttu-id="7aa74-214">Einträge enthalten die Adressen der Ressourcen und Daten zur Identifizierung des Ressourcentyps.</span><span class="sxs-lookup"><span data-stu-id="7aa74-214">Entries contain the addresses of the resources and data to identify the resource type.</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7aa74-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-216">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7aa74-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-218">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="7aa74-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-219">Datum, an dem ein Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7aa74-219">Date an object is installed.</span></span> <span data-ttu-id="7aa74-220">Das-Objekt kann installiert werden, ohne dass ein Wert in diese Eigenschaft geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-220">The object may be installed without a value being written to this property.</span></span>

<span data-ttu-id="7aa74-221">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-222">**Kernelmodetime**</span><span class="sxs-lookup"><span data-stu-id="7aa74-222">**KernelModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-223">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-225">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("kernelmodetime"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="7aa74-225">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-226">Zeit im Kernel Modus in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-226">Time in kernel mode, in milliseconds.</span></span> <span data-ttu-id="7aa74-227">Wenn diese Informationen nicht verfügbar sind, verwenden Sie den Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7aa74-227">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="7aa74-228">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-228">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-229">**Maximumworkingsetsize**</span><span class="sxs-lookup"><span data-stu-id="7aa74-229">**MaximumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-230">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-232">Qualifizierer: [**Berechtigungen**](../wmisdk/standard-wmi-qualifiers.md) ("" \* "," \* "), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" Win32 \| Winnt ". H- \| Kontingent \_ Limits \| maximumworkingsetsize "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" maximale Workingsetgröße "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="7aa74-232">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MaximumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Maximum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-233">Maximale Workingsetgröße des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="7aa74-233">Maximum working set size of the process.</span></span> <span data-ttu-id="7aa74-234">Der Arbeits Satz eines Prozesses ist der Satz von Speicherseiten, die für den Prozess im physischen RAM sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="7aa74-234">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="7aa74-235">Diese Seiten sind residente und können von einer Anwendung verwendet werden, ohne dass ein Seiten Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-235">These pages are resident, and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="7aa74-236">Beispiel: 1413120</span><span class="sxs-lookup"><span data-stu-id="7aa74-236">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-237">**MinimumWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="7aa74-237">**MinimumWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-238">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-238">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-239">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-240">Qualifizierer: [**Berechtigungen**](../wmisdk/standard-wmi-qualifiers.md) ("" \* "," \* "), [**mappingstrings**](../wmisdk/standard-qualifiers.md) (" Win32 \| Winnt ". H \| Kontingent \_ Limits \| MinimumWorkingSetSize "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" minimale Workingsetgröße "), [**Einheiten**](../wmisdk/standard-qualifiers.md) (" Kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="7aa74-240">Qualifiers: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\|WINNT.H\|QUOTA\_LIMITS\|MinimumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Minimum Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-241">Minimale Workingsetgröße des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="7aa74-241">Minimum working set size of the process.</span></span> <span data-ttu-id="7aa74-242">Der Arbeits Satz eines Prozesses ist der Satz von Speicherseiten, die für den Prozess im physischen RAM sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="7aa74-242">The working set of a process is the set of memory pages visible to the process in physical RAM.</span></span> <span data-ttu-id="7aa74-243">Diese Seiten sind residente und können für eine Anwendung verwendet werden, ohne dass ein Seiten Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-243">These pages are resident and available for an application to use without triggering a page fault.</span></span>

<span data-ttu-id="7aa74-244">Beispiel: 20480</span><span class="sxs-lookup"><span data-stu-id="7aa74-244">Example: 20480</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-245">**Name**</span><span class="sxs-lookup"><span data-stu-id="7aa74-245">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-246">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-247">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-248">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7aa74-248">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-249">Der Name der für den Prozessverantwortlichen ausführbaren Datei, die der Eigenschaft Image Name im Task-Manager entspricht.</span><span class="sxs-lookup"><span data-stu-id="7aa74-249">Name of the executable file responsible for the process, equivalent to the Image Name property in Task Manager.</span></span>

<span data-ttu-id="7aa74-250">Wenn Sie von einer Unterklasse geerbt wird, kann die-Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-250">When inherited by a subclass, the property can be overridden to be a key property.</span></span> <span data-ttu-id="7aa74-251">Der Name ist in der Anwendung selbst hart codiert und wird durch Ändern des Datei namens nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-251">The name is hard-coded into the application itself and is not affected by changing the file name.</span></span> <span data-ttu-id="7aa74-252">Wenn Sie z. b. Calc.exe umbenennen, wird der Name Calc.exe weiterhin im Task-Manager und in WMI-Skripts angezeigt, die den Prozessnamen abrufen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-252">For example, even if you rename Calc.exe, the name Calc.exe will still appear in Task Manager and in any WMI scripts that retrieve the process name.</span></span>

<span data-ttu-id="7aa74-253">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-253">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-254">**Oscreationclassname**</span><span class="sxs-lookup"><span data-stu-id="7aa74-254">**OSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-257">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Betriebs System-Klassenname")</span><span class="sxs-lookup"><span data-stu-id="7aa74-257">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-258">Der Name der Erstellungs Klasse des Bereichs bezogenen Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="7aa74-258">Creation class name of the scoping operating system.</span></span>

<span data-ttu-id="7aa74-259">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-259">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-260">**OSName**</span><span class="sxs-lookup"><span data-stu-id="7aa74-260">**OSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-261">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-263">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Betriebs System Name ")</span><span class="sxs-lookup"><span data-stu-id="7aa74-263">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Name")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-264">Der Name des Bereichs bezogenen Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="7aa74-264">Name of the scoping operating system.</span></span>

<span data-ttu-id="7aa74-265">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-265">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-266">**Otheroperationcount**</span><span class="sxs-lookup"><span data-stu-id="7aa74-266">**OtherOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-267">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-268">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-269">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| otheroperationcount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Other Operation count")</span><span class="sxs-lookup"><span data-stu-id="7aa74-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-270">Anzahl der durchgeführten e/a-Vorgänge, die keine Lese-oder Schreibvorgänge sind.</span><span class="sxs-lookup"><span data-stu-id="7aa74-270">Number of I/O operations performed that are not read or write operations.</span></span>

<span data-ttu-id="7aa74-271">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-271">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-272">**Othertransfercount**</span><span class="sxs-lookup"><span data-stu-id="7aa74-272">**OtherTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-273">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-273">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-274">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-275">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| othertransfercount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Other Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="7aa74-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-276">Datenmenge, die bei Vorgängen übertragen wird, die keine Lese-oder Schreibvorgänge sind.</span><span class="sxs-lookup"><span data-stu-id="7aa74-276">Amount of data transferred during operations that are not read or write operations.</span></span>

<span data-ttu-id="7aa74-277">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-277">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-278">**PageFaults**</span><span class="sxs-lookup"><span data-stu-id="7aa74-278">**PageFaults**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-279">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-280">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-281">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| pagefehlercount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("number of Page Faults")</span><span class="sxs-lookup"><span data-stu-id="7aa74-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Number Of Page Faults")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-282">Anzahl der Seiten Fehler, die von einem Prozess generiert werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-282">Number of page faults that a process generates.</span></span>

<span data-ttu-id="7aa74-283">Beispiel: 10</span><span class="sxs-lookup"><span data-stu-id="7aa74-283">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-284">**PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="7aa74-284">**PageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-285">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-287">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PageFileUsage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Auslagerungs Datei Verwendung"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="7aa74-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-288">Der Umfang des Auslagerungs Datei-Speicherplatzes, den ein Prozess zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="7aa74-288">Amount of page file space that a process is using currently.</span></span> <span data-ttu-id="7aa74-289">Dieser Wert entspricht dem **vmsize** -Wert in TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="7aa74-289">This value is consistent with the **VMSize** value in TaskMgr.exe.</span></span>

<span data-ttu-id="7aa74-290">Beispiel: 102435</span><span class="sxs-lookup"><span data-stu-id="7aa74-290">Example: 102435</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-291">**"Parametriprocessid"**</span><span class="sxs-lookup"><span data-stu-id="7aa74-291">**ParentProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-292">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-293">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-294">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| vereritedfromuniqueprocessid"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Parent Process ID")</span><span class="sxs-lookup"><span data-stu-id="7aa74-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Parent Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-295">Eindeutiger Bezeichner des Prozesses, von dem ein Prozess erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-295">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="7aa74-296">Die prozesbezeichnernummern werden wieder verwendet, sodass Sie nur einen Prozess für die Lebensdauer dieses Prozesses identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7aa74-296">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="7aa74-297">Es ist möglich, dass der durch " **parameterprocessid** " identifizierte Prozess beendet wird, sodass " **parameterprocessid** " möglicherweise nicht auf einen laufenden Prozess verweist.</span><span class="sxs-lookup"><span data-stu-id="7aa74-297">It is possible that the process identified by **ParentProcessId** is terminated, so **ParentProcessId** may not refer to a running process.</span></span> <span data-ttu-id="7aa74-298">Es ist auch möglich, dass " **paramedprocessid** " fälschlicherweise auf einen Prozess verweist, der einen Prozess Bezeichner wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="7aa74-298">It is also possible that **ParentProcessId** incorrectly refers to a process that reuses a process identifier.</span></span> <span data-ttu-id="7aa74-299">Sie können mit der Eigenschaft " **kreationdate** " bestimmen, ob das angegebene übergeordnete Element erstellt wurde, nachdem der von dieser **Win32- \_ Prozess** Instanz dargestellte Prozess erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7aa74-299">You can use the **CreationDate** property to determine whether the specified parent was created after the process represented by this **Win32\_Process** instance was created.</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-300">**"Peer Page File Usage"**</span><span class="sxs-lookup"><span data-stu-id="7aa74-300">**PeakPageFileUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-301">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-302">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-303">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakPageFileUsage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Top Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("Kilobytes")</span><span class="sxs-lookup"><span data-stu-id="7aa74-303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-304">Maximale Menge an Auslagerungs Dateispeicher Platz, die während der Lebensdauer eines Prozesses verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-304">Maximum amount of page file space used during the life of a process.</span></span>

<span data-ttu-id="7aa74-305">Beispiel: 102367</span><span class="sxs-lookup"><span data-stu-id="7aa74-305">Example: 102367</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-306">**Peakvirtualsize**</span><span class="sxs-lookup"><span data-stu-id="7aa74-306">**PeakVirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-307">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-307">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-308">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-309">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| peakvirtualsize"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("maximale Auslastung des virtuellen Adressraums"), [**Einheiten**](../wmisdk/standard-qualifiers.md) (Bytes)</span><span class="sxs-lookup"><span data-stu-id="7aa74-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-310">Maximaler virtueller Adressraum, der von einem Prozess zu einem beliebigen Zeitpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-310">Maximum virtual address space a process uses at any one time.</span></span> <span data-ttu-id="7aa74-311">Die Verwendung von virtuellem Adressraum impliziert nicht notwendigerweise die entsprechende Verwendung von Datenträger-oder Hauptspeicher Seiten.</span><span class="sxs-lookup"><span data-stu-id="7aa74-311">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="7aa74-312">Der virtuelle Speicherplatz ist jedoch begrenzt, und der Prozess kann möglicherweise nicht in der Lage sein, Bibliotheken zu laden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-312">However, virtual space is finite, and by using too much the process might not be able to load libraries.</span></span>

<span data-ttu-id="7aa74-313">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-313">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-314">**PeakWorkingSetSize**</span><span class="sxs-lookup"><span data-stu-id="7aa74-314">**PeakWorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-315">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-316">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-317">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PeakWorkingSetSize"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("maximale Workingsetgröße"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="7aa74-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-318">Maximale Workingsetgröße eines Prozesses.</span><span class="sxs-lookup"><span data-stu-id="7aa74-318">Peak working set size of a process.</span></span>

<span data-ttu-id="7aa74-319">Beispiel: 1413120</span><span class="sxs-lookup"><span data-stu-id="7aa74-319">Example: 1413120</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-320">**Priority**</span><span class="sxs-lookup"><span data-stu-id="7aa74-320">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-321">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-322">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-323">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Priorität"), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| BasePriority"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Priority")</span><span class="sxs-lookup"><span data-stu-id="7aa74-323">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-324">Planen der Priorität eines Prozesses in einem Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="7aa74-324">Scheduling priority of a process within an operating system.</span></span> <span data-ttu-id="7aa74-325">Je höher der Wert ist, desto höher wird ein Prozess von einem Prozess empfangen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-325">The higher the value, the higher priority a process receives.</span></span> <span data-ttu-id="7aa74-326">Prioritätswerte liegen im Bereich von 0 (null). Dies ist die niedrigste Priorität von 31 (höchste Priorität).</span><span class="sxs-lookup"><span data-stu-id="7aa74-326">Priority values can range from 0 (zero), which is the lowest priority to 31, which is highest priority.</span></span>

<span data-ttu-id="7aa74-327">Beispiel: 7</span><span class="sxs-lookup"><span data-stu-id="7aa74-327">Example: 7</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-328">**PrivatePageCount**</span><span class="sxs-lookup"><span data-stu-id="7aa74-328">**PrivatePageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-329">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-330">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-331">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| PrivatePageCount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("private Page count")</span><span class="sxs-lookup"><span data-stu-id="7aa74-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private Page Count")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-332">Aktuelle Anzahl der zugeordneten Seiten, auf die nur für den von dieser **Win32- \_ Prozess** Instanz dargestellten Prozess zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7aa74-332">Current number of pages allocated that are only accessible to the process represented by this **Win32\_Process** instance.</span></span>

<span data-ttu-id="7aa74-333">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-334">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="7aa74-334">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-335">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-336">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-337">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**Process \_ Information**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| dwProcessId"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="7aa74-337">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)\|dwProcessId "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-338">Numerischer Bezeichner zum unterscheiden eines Prozesses von einem anderen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-338">Numeric identifier used to distinguish one process from another.</span></span> <span data-ttu-id="7aa74-339">Processids sind ab dem Prozess Erstellungs Zeitpunkt für die Prozess Beendigung gültig.</span><span class="sxs-lookup"><span data-stu-id="7aa74-339">ProcessIDs are valid from process creation time to process termination.</span></span> <span data-ttu-id="7aa74-340">Bei Beendigung kann derselbe numerische Bezeichner auf einen neuen Prozess angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-340">Upon termination, that same numeric identifier can be applied to a new process.</span></span>

<span data-ttu-id="7aa74-341">Dies bedeutet, dass Sie ProcessID nicht allein verwenden können, um einen bestimmten Prozess zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-341">This means that you cannot use ProcessID alone to monitor a particular process.</span></span> <span data-ttu-id="7aa74-342">Beispielsweise könnte eine Anwendung eine ProcessID von 7 aufweisen und dann fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-342">For example, an application could have a ProcessID of 7, and then fail.</span></span> <span data-ttu-id="7aa74-343">Wenn ein neuer Prozess gestartet wird, kann der neue Prozess ProcessID 7 zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-343">When a new process is started, the new process could be assigned ProcessID 7.</span></span> <span data-ttu-id="7aa74-344">Ein Skript, das nur auf eine angegebene ProcessID geprüft wurde, könnte daher "täuschen", wenn die ursprüngliche Anwendung noch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-344">A script that checked only for a specified ProcessID could thus be "fooled" into thinking that the original application was still running.</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-345">**Quotanonpgedpoolusage**</span><span class="sxs-lookup"><span data-stu-id="7aa74-345">**QuotaNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-346">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-347">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-348">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| quotanonpgedpoolusage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("nicht auslageres Pool Nutzungs Kontingent")</span><span class="sxs-lookup"><span data-stu-id="7aa74-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-349">Kontingent Betrag der nicht auslagerungspoolverwendung für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="7aa74-349">Quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="7aa74-350">Beispiel: 15</span><span class="sxs-lookup"><span data-stu-id="7aa74-350">Example: 15</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-351">**Quotapgedpoolusage**</span><span class="sxs-lookup"><span data-stu-id="7aa74-351">**QuotaPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-352">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-353">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-354">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| quotapaargedpoolusage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Kontingent für Auslagerungs Pool Nutzung")</span><span class="sxs-lookup"><span data-stu-id="7aa74-354">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-355">Kontingent Betrag der auslagerungspoolverwendung für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="7aa74-355">Quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="7aa74-356">Beispiel: 22</span><span class="sxs-lookup"><span data-stu-id="7aa74-356">Example: 22</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-357">**Quotapeaknonpgedpoolusage**</span><span class="sxs-lookup"><span data-stu-id="7aa74-357">**QuotaPeakNonPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-358">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-359">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-360">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| quotapeaknonpfgedpoolusage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Maximum Non-Auslagerungs Pool Usage Quota")</span><span class="sxs-lookup"><span data-stu-id="7aa74-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Non-Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-361">Maximale Kontingent Kontingent Menge der nicht ausgelagerten Pool Nutzung für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="7aa74-361">Peak quota amount of nonpaged pool usage for a process.</span></span>

<span data-ttu-id="7aa74-362">Beispiel: 31</span><span class="sxs-lookup"><span data-stu-id="7aa74-362">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-363">**Quotapeakpgedpoolusage**</span><span class="sxs-lookup"><span data-stu-id="7aa74-363">**QuotaPeakPagedPoolUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-364">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-365">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-366">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| quotapeakpgedpoolusage"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Kontingent für Auslagerungs Pool-Nutzungs Kontingent")</span><span class="sxs-lookup"><span data-stu-id="7aa74-366">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Paged Pool Usage Quota")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-367">Maximale Kontingent Kontingent Menge der ausgelagerten Pool Nutzung für einen Prozess.</span><span class="sxs-lookup"><span data-stu-id="7aa74-367">Peak quota amount of paged pool usage for a process.</span></span>

<span data-ttu-id="7aa74-368">Beispiel: 31</span><span class="sxs-lookup"><span data-stu-id="7aa74-368">Example: 31</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-369">**"Read operationcount"**</span><span class="sxs-lookup"><span data-stu-id="7aa74-369">**ReadOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-370">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-371">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-372">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| leseoperationcount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Anzahl der Lesevorgänge")</span><span class="sxs-lookup"><span data-stu-id="7aa74-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-373">Anzahl der ausgeführten Lesevorgänge.</span><span class="sxs-lookup"><span data-stu-id="7aa74-373">Number of read operations performed.</span></span>

<span data-ttu-id="7aa74-374">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-374">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-375">**Read Transfer count**</span><span class="sxs-lookup"><span data-stu-id="7aa74-375">**ReadTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-376">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-376">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-377">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-378">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| lesetransfercount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Read Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="7aa74-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-379">Menge der gelesenen Daten.</span><span class="sxs-lookup"><span data-stu-id="7aa74-379">Amount of data read.</span></span>

<span data-ttu-id="7aa74-380">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-381">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="7aa74-381">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-382">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-383">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-384">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| SessionID"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Sitzungs-ID")</span><span class="sxs-lookup"><span data-stu-id="7aa74-384">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|SessionId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Session Id")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-385">Eindeutiger Bezeichner, den ein Betriebssystem generiert, wenn eine Sitzung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-385">Unique identifier that an operating system generates when a session is created.</span></span> <span data-ttu-id="7aa74-386">Eine Sitzung erstreckt sich vor der Anmeldung von einem bestimmten System aus über eine bestimmte Zeitspanne.</span><span class="sxs-lookup"><span data-stu-id="7aa74-386">A session spans a period of time from logon until logoff from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-387">**Status**</span><span class="sxs-lookup"><span data-stu-id="7aa74-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-388">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-389">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-390">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7aa74-390">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-391">Diese Eigenschaft ist nicht implementiert und wird für keine Instanz dieser Klasse aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-391">This property is not implemented and does not get populated for any instance of this class.</span></span> <span data-ttu-id="7aa74-392">Es ist immer **null**.</span><span class="sxs-lookup"><span data-stu-id="7aa74-392">It is always **NULL**.</span></span>

<span data-ttu-id="7aa74-393">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-393">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7aa74-394">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="7aa74-394">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7aa74-395">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7aa74-395">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7aa74-396">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7aa74-396">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7aa74-397">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7aa74-397">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7aa74-398">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7aa74-398">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7aa74-399">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7aa74-399">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7aa74-400">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7aa74-400">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7aa74-401">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="7aa74-401">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7aa74-402">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7aa74-402">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7aa74-403">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="7aa74-403">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7aa74-404">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="7aa74-404">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7aa74-405">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="7aa74-405">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7aa74-406">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="7aa74-406">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7aa74-407">**TerminationDate**</span><span class="sxs-lookup"><span data-stu-id="7aa74-407">**TerminationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-408">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7aa74-408">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-409">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-410">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Beendigungs Datum")</span><span class="sxs-lookup"><span data-stu-id="7aa74-410">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Termination Date")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-411">Der Prozess wurde beendet oder beendet.</span><span class="sxs-lookup"><span data-stu-id="7aa74-411">Process was stopped or terminated.</span></span> <span data-ttu-id="7aa74-412">Um die Beendigungs Zeit zu erhalten, muss ein Handle für den Prozess offen gehalten werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-412">To get the termination time, a handle to the process must be held open.</span></span> <span data-ttu-id="7aa74-413">Andernfalls gibt diese Eigenschaft **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="7aa74-413">Otherwise, this property returns **NULL**.</span></span>

<span data-ttu-id="7aa74-414">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-414">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-415">**Thread Anzahl**</span><span class="sxs-lookup"><span data-stu-id="7aa74-415">**ThreadCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-416">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7aa74-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-417">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-418">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| numofthreads"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Thread Anzahl")</span><span class="sxs-lookup"><span data-stu-id="7aa74-418">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Thread Count")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-419">Anzahl der aktiven Threads in einem Prozess.</span><span class="sxs-lookup"><span data-stu-id="7aa74-419">Number of active threads in a process.</span></span> <span data-ttu-id="7aa74-420">Eine Anweisung ist die grundlegende Einheit der Ausführung in einem Prozessor, und ein Thread ist das Objekt, das eine Anweisung ausführt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-420">An instruction is the basic unit of execution in a processor, and a thread is the object that executes an instruction.</span></span> <span data-ttu-id="7aa74-421">Jeder laufende Prozess verfügt über mindestens einen Thread.</span><span class="sxs-lookup"><span data-stu-id="7aa74-421">Each running process has at least one thread.</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-422">**UserModeTime**</span><span class="sxs-lookup"><span data-stu-id="7aa74-422">**UserModeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-423">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-423">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-424">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-425">Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("UserModeTime"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span><span class="sxs-lookup"><span data-stu-id="7aa74-425">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-426">Zeit im Benutzermodus in 100 Nanosekunden-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="7aa74-426">Time in user mode, in 100 nanosecond units.</span></span> <span data-ttu-id="7aa74-427">Wenn diese Informationen nicht verfügbar sind, verwenden Sie den Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7aa74-427">If this information is not available, use a value of 0 (zero).</span></span>

<span data-ttu-id="7aa74-428">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-428">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-429">**VirtualSize**</span><span class="sxs-lookup"><span data-stu-id="7aa74-429">**VirtualSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-430">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-431">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-432">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status \| System \_ Process \_ Information \| VirtualSize"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space use"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="7aa74-432">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process Status\|SYSTEM\_PROCESS\_INFORMATION\|VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-433">Die aktuelle Größe des virtuellen Adressraums, der von einem Prozess verwendet wird, nicht der physische oder virtuelle Speicher, der tatsächlich vom Prozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-433">Current size of the virtual address space that a process is using, not the physical or virtual memory actually used by the process.</span></span> <span data-ttu-id="7aa74-434">Die Verwendung von virtuellem Adressraum impliziert nicht notwendigerweise die entsprechende Verwendung von Datenträger-oder Hauptspeicher Seiten.</span><span class="sxs-lookup"><span data-stu-id="7aa74-434">Using virtual address space does not necessarily imply corresponding use of either disk or main memory pages.</span></span> <span data-ttu-id="7aa74-435">Der virtuelle Speicherplatz ist begrenzt. Wenn Sie zu viel verwenden, ist der Prozess möglicherweise nicht in der Lage, Bibliotheken zu laden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-435">Virtual space is finite, and by using too much, the process might not be able to load libraries.</span></span> <span data-ttu-id="7aa74-436">Dieser Wert entspricht dem, was Sie in Perfmon.exe sehen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-436">This value is consistent with what you see in Perfmon.exe.</span></span>

<span data-ttu-id="7aa74-437">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-437">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-438">**WindowsVersion**</span><span class="sxs-lookup"><span data-stu-id="7aa74-438">**WindowsVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-439">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7aa74-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-440">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-441">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Functions \| getprocessversion"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Windows Version")</span><span class="sxs-lookup"><span data-stu-id="7aa74-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-442">Version von Windows, in der der Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-442">Version of Windows in which the process is running.</span></span>

<span data-ttu-id="7aa74-443">Beispiel: 4,0</span><span class="sxs-lookup"><span data-stu-id="7aa74-443">Example: 4.0</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-444">**Workingsetsize**</span><span class="sxs-lookup"><span data-stu-id="7aa74-444">**WorkingSetSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-445">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-446">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-447">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Workingsetgröße"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="7aa74-447">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-448">Der Arbeitsspeicher in Bytes, der für die effiziente Ausführung eines Prozesses erforderlich ist – für ein Betriebssystem, das die Seiten basierte Speicherverwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7aa74-448">Amount of memory in bytes that a process needs to execute efficiently—for an operating system that uses page-based memory management.</span></span> <span data-ttu-id="7aa74-449">Wenn das System nicht über genügend Arbeitsspeicher verfügt (weniger als die Workingsetgröße), tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7aa74-449">If the system does not have enough memory (less than the working set size), thrashing occurs.</span></span> <span data-ttu-id="7aa74-450">Wenn die Größe des Workingsets nicht bekannt ist, verwenden Sie **null** oder 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7aa74-450">If the size of the working set is not known, use **NULL** or 0 (zero).</span></span> <span data-ttu-id="7aa74-451">Wenn Workingsetdaten bereitgestellt werden, können Sie die Informationen überwachen, um die veränderlichen Arbeitsspeicher Anforderungen eines Prozesses zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-451">If working set data is provided, you can monitor the information to understand the changing memory requirements of a process.</span></span>

<span data-ttu-id="7aa74-452">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-452">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="7aa74-453">Diese Eigenschaft wird vom [**CIM- \_ Prozess**](cim-process.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-453">This property is inherited from [**CIM\_Process**](cim-process.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-454">**Schreiboperationcount**</span><span class="sxs-lookup"><span data-stu-id="7aa74-454">**WriteOperationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-455">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-455">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-456">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-456">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-457">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| Beschreib teoperationcount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Write Operation count")</span><span class="sxs-lookup"><span data-stu-id="7aa74-457">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Operation Count")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-458">Anzahl der ausgeführten Schreibvorgänge.</span><span class="sxs-lookup"><span data-stu-id="7aa74-458">Number of write operations performed.</span></span>

<span data-ttu-id="7aa74-459">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-459">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7aa74-460">**Schreib Übertragungs Zähler**</span><span class="sxs-lookup"><span data-stu-id="7aa74-460">**WriteTransferCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa74-461">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7aa74-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-462">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7aa74-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7aa74-463">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| System \_ Process \_ Information \| Beschreib tetransfercount"), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Write Transfer count"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")</span><span class="sxs-lookup"><span data-stu-id="7aa74-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|SYSTEM\_PROCESS\_INFORMATION\|WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7aa74-464">Menge der geschriebenen Daten.</span><span class="sxs-lookup"><span data-stu-id="7aa74-464">Amount of data written.</span></span>

<span data-ttu-id="7aa74-465">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-465">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7aa74-466">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aa74-466">Remarks</span></span>

<span data-ttu-id="7aa74-467">Die **Win32- \_ Prozess** Klasse wird vom [**CIM- \_ Prozess**](cim-process.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7aa74-467">The **Win32\_Process** class is derived from [**CIM\_Process**](cim-process.md).</span></span> <span data-ttu-id="7aa74-468">Der aufrufenden Prozess, der diese Klasse verwendet, muss auf dem Computer, auf dem sich die Registrierung befindet, über die Berechtigung " **SE \_ Restore \_ Name** " verfügen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-468">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="7aa74-469">Weitere Informationen finden Sie unter [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-469">For more information, see [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

### <a name="overview"></a><span data-ttu-id="7aa74-470">Übersicht</span><span class="sxs-lookup"><span data-stu-id="7aa74-470">Overview</span></span>

<span data-ttu-id="7aa74-471">Prozesse sind fast alles, was auf einem Computer passiert.</span><span class="sxs-lookup"><span data-stu-id="7aa74-471">Processes underlie almost everything that happens on a computer.</span></span> <span data-ttu-id="7aa74-472">Tatsächlich kann die Ursache der meisten Computerprobleme auf Prozesse zurückzuführen sein. Beispielsweise kann es vorkommen, dass zu viele Prozesse auf einem Computer ausgeführt werden (und Konflikte für einen begrenzten Satz von Ressourcen haben), oder ein einzelner Prozess verwendet möglicherweise mehr als seinen Ressourcen Anteil.</span><span class="sxs-lookup"><span data-stu-id="7aa74-472">In fact, the root cause of most computer problems can be traced to processes; for example, too many processes might be running on a computer (and contending for a finite set of resources), or a single process might be using more than its share of resources.</span></span> <span data-ttu-id="7aa74-473">Diese Faktoren machen es wichtig, dass Sie die auf einem Computer laufenden Prozesse genau beobachten.</span><span class="sxs-lookup"><span data-stu-id="7aa74-473">These factors make it important to keep a close watch on the processes running on a computer.</span></span> <span data-ttu-id="7aa74-474">Mit der Prozessüberwachung, der Hauptaktivität in der Prozess Verwaltung, können Sie bestimmen, was ein Computer tatsächlich tut, welche Anwendungen der Computer ausführt und wie diese Anwendungen von Änderungen in der Computerumgebung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="7aa74-474">Process monitoring, the main activity in process management, allows you to determine what a computer actually does, what applications the computer runs, and how those applications are affected by changes in the computing environment.</span></span>

### <a name="monitoring-a-process"></a><span data-ttu-id="7aa74-475">Überwachen eines Prozesses</span><span class="sxs-lookup"><span data-stu-id="7aa74-475">Monitoring a Process</span></span>

<span data-ttu-id="7aa74-476">Durch die regelmäßige Überwachung von Prozessen können Sie sicherstellen, dass ein Computer mit hoher Effizienz ausgeführt wird und seine vorgesehenen Aufgaben erwartungsgemäß ausführt.</span><span class="sxs-lookup"><span data-stu-id="7aa74-476">Monitoring processes on a regular basis helps you ensure that a computer runs at peak efficiency and that it carries out its appointed tasks as expected.</span></span> <span data-ttu-id="7aa74-477">Beispielsweise können Sie bei der Überwachung von Prozessen sofort eine beliebige Anwendung Benachrichtigen, die nicht mehr reagiert, und dann Maßnahmen ergreifen, um diesen Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-477">For example, by monitoring processes you can be notified immediately of any application that has stopped responding, and then take steps to end that process.</span></span> <span data-ttu-id="7aa74-478">Außerdem können Sie mithilfe der Prozessüberwachung Probleme erkennen, bevor Sie auftreten.</span><span class="sxs-lookup"><span data-stu-id="7aa74-478">In addition, process monitoring enables you to identify problems before they occur.</span></span> <span data-ttu-id="7aa74-479">Beispielsweise können Sie durch wiederholtes Überprüfen der von einem Prozess genutzten Arbeitsspeicher Menge einen Speicherlecks erkennen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-479">For example, by repeatedly checking the amount of memory used by a process, you can identify a memory leak.</span></span> <span data-ttu-id="7aa74-480">Sie können den Prozess beenden, bevor die fehlerhafte Anwendung den gesamten verfügbaren Arbeitsspeicher verwendet und den Computer angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-480">You can then stop the process before the errant application uses all of the available memory and brings the computer to a halt.</span></span>

<span data-ttu-id="7aa74-481">Mit der Prozessüberwachung können auch die Unterbrechungen minimiert werden, die durch geplante Ausfälle bei Upgrades und Wartungsarbeiten verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-481">Process monitoring also helps minimize the disruptions caused by planned outages for upgrades and maintenance.</span></span> <span data-ttu-id="7aa74-482">Wenn Sie z. b. den Status einer Datenbankanwendung überprüfen, die auf Client Computern ausgeführt wird, können Sie die Auswirkungen der Offline Schaltung der Datenbank ermitteln, um die Software zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7aa74-482">For example, by checking the status of a database application running on client computers, you can determine the impact of taking the database offline in order to upgrade the software.</span></span>

<span data-ttu-id="7aa74-483">Überwachen der Prozess Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="7aa74-483">Monitoring process availability.</span></span> <span data-ttu-id="7aa74-484">Misst den Prozentsatz der Zeit, zu der ein Prozess verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7aa74-484">Measures the percentage of time that a process is available.</span></span> <span data-ttu-id="7aa74-485">Die Verfügbarkeit wird in der Regel durch die Verwendung eines einfachen Tests überwacht, der meldet, ob der Prozess noch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-485">Availability is typically monitored by use of a simple probe, which reports whether the process is still running.</span></span> <span data-ttu-id="7aa74-486">Durch die Nachverfolgung der Ergebnisse der einzelnen Tests können Sie die Verfügbarkeit des Prozesses berechnen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-486">By keeping track of the results of each probe, you can calculate the availability of the process.</span></span> <span data-ttu-id="7aa74-487">Beispielsweise hat ein Prozess, bei dem 100-mal geprüft werden und auf 95 dieser Vorkommen antwortet, eine Verfügbarkeit von 95 Prozent.</span><span class="sxs-lookup"><span data-stu-id="7aa74-487">For example, a process that is probed 100 times and responds on 95 of those occasions has an availability of 95 percent.</span></span> <span data-ttu-id="7aa74-488">Diese Art der Überwachung ist in der Regel für Datenbanken, e-Mail-Programme und andere Anwendungen reserviert, die zu jedem Zeitpunkt erwartungsgemäß ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-488">This type of monitoring is typically reserved for databases, mail programs, and other applications that are expected to run at all times.</span></span> <span data-ttu-id="7aa74-489">Sie eignet sich nicht für Textverarbeitungsprogramme, Kalkulations Tabellen oder andere Anwendungen, die routinemäßig mehrmals täglich gestartet und angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-489">It is not appropriate for word processing programs, spreadsheets, or other applications that are routinely started and stopped several times a day.</span></span>

<span data-ttu-id="7aa74-490">Sie können eine Instanz der Win32-Klasse " [**\_ processstartup**](win32-processstartup.md) " erstellen, um den Prozess zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7aa74-490">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process.</span></span>

<span data-ttu-id="7aa74-491">Sie können die Prozessleistung mit der [**Win32 \_ perfformatteddata \_ perfproc \_ Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) -Klasse und einem WMI-Aktualisierungs Objekt (z. b. " [**Swap**](../wmisdk/swbemrefresher.md)-Aktualisierungs Programm") überwachen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-491">You can monitor process performance with the [**Win32\_PerfFormattedData\_PerfProc\_Process**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) class and a WMI refresher object, such as [**SWbemRefresher**](../wmisdk/swbemrefresher.md).</span></span> <span data-ttu-id="7aa74-492">Weitere Informationen finden Sie unter über [Wachen von Leistungsdaten](../wmisdk/monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="7aa74-492">For more information, see [Monitoring Performance Data](../wmisdk/monitoring-performance-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7aa74-493">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7aa74-493">Examples</span></span>

<span data-ttu-id="7aa74-494">In der [Liste der Eigenschaften von WMI-Klassen](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell-Codebeispiel in TechNet Gallery wird die **Win32- \_ Prozess** Klasse beschrieben und die Ergebnisse im Excel-Format ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="7aa74-494">The [List the Properties of WMI Classes](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) PowerShell code sample on TechNet Gallery describes the **Win32\_Process** class, and outputs the results in Excel format.</span></span>

<span data-ttu-id="7aa74-495">Der [Prozess zum Beenden der Ausführung auf mehreren Servern](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) beendet einen Prozess, der auf einem oder mehreren Computern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-495">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="7aa74-496">Im [Beispiel: Aufrufen einer Anbieter Methode](../wmisdk/example--calling-a-provider-method.md) verwendet der Code C++, um den Win32- **\_ Prozess** zum Erstellen eines Prozesses aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-496">In the [Example: Calling a Provider Method](../wmisdk/example--calling-a-provider-method.md) topic, the code uses C++ to call **Win32\_Process** to create a process.</span></span>

<span data-ttu-id="7aa74-497">Verfügbarkeit ist die einfachste Form der Prozessüberwachung: bei diesem Ansatz wird lediglich sichergestellt, dass der Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7aa74-497">Availability is the simplest form of process monitoring: with this approach, you simply ensure that the process is running.</span></span> <span data-ttu-id="7aa74-498">Wenn Sie die Prozess Verfügbarkeit überwachen, rufen Sie in der Regel eine Liste der Prozesse ab, die auf einem Computer ausgeführt werden, und überprüfen dann, ob ein bestimmter Prozess noch aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="7aa74-498">When you monitor for process availability, you typically retrieve a list of processes running on a computer and then verify that a particular process is still active.</span></span> <span data-ttu-id="7aa74-499">Wenn der Prozess aktiv ist, gilt er als verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7aa74-499">If the process is active, it is considered available.</span></span> <span data-ttu-id="7aa74-500">Wenn der Prozess nicht aktiv ist, ist er nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7aa74-500">If the process is not active, it is not available.</span></span> <span data-ttu-id="7aa74-501">Im folgenden VBScript-Beispiel wird die Prozess Verfügbarkeit überwacht, indem die Liste der auf einem Computer ausgelaufenden Prozesse überprüft und eine Benachrichtigung ausgegeben wird, wenn der Database.exe Prozess nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="7aa74-501">The following VBScript sample monitors process availability by checking the list of processes running on a computer and issuing a notification if the Database.exe process is not found.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



<span data-ttu-id="7aa74-502">Das folgende VBScript-Beispiel überwacht die Prozesserstellung mit einem temporären Ereignisconsumer.</span><span class="sxs-lookup"><span data-stu-id="7aa74-502">The following VBScript sample monitors process creation using a temporary event consumer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



<span data-ttu-id="7aa74-503">Das folgende VBScript überwacht die Prozess Leistungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-503">The following VBScript monitors process performance information.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



<span data-ttu-id="7aa74-504">Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie den Besitzer der einzelnen Prozesse auf einem lokalen Computer abrufen können.</span><span class="sxs-lookup"><span data-stu-id="7aa74-504">The following VBScript code example shows how to obtain the owner of each process on a local computer.</span></span> <span data-ttu-id="7aa74-505">Mit diesem Skript können Sie beispielsweise Daten von einem Remote Computer abrufen, um zu bestimmen, welche Benutzer über Prozesse verfügen, auf denen Terminal Server ausgeführt wird, und den Namen des Remote Computers in der ersten Zeile durch den Namen des Remote Computers ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7aa74-505">You can use this script to obtain data from a remote computer, for example, to determine which users have processes running terminal server, substitute the name of the remote computer for "." in the first line.</span></span> <span data-ttu-id="7aa74-506">Sie müssen auch Administrator auf dem Remote Computer sein.</span><span class="sxs-lookup"><span data-stu-id="7aa74-506">You must also be an administrator on the remote machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



<span data-ttu-id="7aa74-507">Im folgenden VBScript-Codebeispiel wird gezeigt, wie Sie die Anmelde Sitzung abrufen, die einem laufenden Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7aa74-507">The following VBScript code example shows how to obtain the logon session associated with a running process.</span></span> <span data-ttu-id="7aa74-508">Vor dem Starten des Skripts muss ein Prozess Notepad.exe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7aa74-508">A process must be running Notepad.exe before the script starts.</span></span> <span data-ttu-id="7aa74-509">Im Beispiel werden die Instanzen von [**Win32 \_ logonsession**](win32-logonsession.md) , die dem **Win32- \_ Prozess** zugeordnet sind, der Notepad.exe darstellt, lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="7aa74-509">The example locates the instances of [**Win32\_LogonSession**](win32-logonsession.md) associated with the **Win32\_Process** that represents Notepad.exe.</span></span> <span data-ttu-id="7aa74-510">[**Win32 \_ Sessionprocess**](win32-sessionprocess.md) wird als Association-Klasse angegeben.</span><span class="sxs-lookup"><span data-stu-id="7aa74-510">[**Win32\_SessionProcess**](win32-sessionprocess.md) is specified as the association class.</span></span> <span data-ttu-id="7aa74-511">Weitere Informationen finden Sie unter [ASSOCIATORS of Statement.](../wmisdk/associators-of-statement.md)</span><span class="sxs-lookup"><span data-stu-id="7aa74-511">For more information, see [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md).</span></span>


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a><span data-ttu-id="7aa74-512">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aa74-512">Requirements</span></span>



| <span data-ttu-id="7aa74-513">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7aa74-513">Requirement</span></span> | <span data-ttu-id="7aa74-514">Wert</span><span class="sxs-lookup"><span data-stu-id="7aa74-514">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa74-515">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7aa74-515">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa74-516">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7aa74-516">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7aa74-517">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7aa74-517">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa74-518">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7aa74-518">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7aa74-519">Namespace</span><span class="sxs-lookup"><span data-stu-id="7aa74-519">Namespace</span></span><br/>                | <span data-ttu-id="7aa74-520">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7aa74-520">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7aa74-521">MOF</span><span class="sxs-lookup"><span data-stu-id="7aa74-521">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7aa74-522"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7aa74-522"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7aa74-523">DLL</span><span class="sxs-lookup"><span data-stu-id="7aa74-523">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aa74-524"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aa74-524"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aa74-525">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aa74-525">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa74-526">**CIM- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="7aa74-526">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dt>

[<span data-ttu-id="7aa74-527">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="7aa74-527">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7aa74-528">WMI-Tasks: Prozesse</span><span class="sxs-lookup"><span data-stu-id="7aa74-528">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
