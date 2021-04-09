---
description: Die \_ WMI-Klasse von Win32 PrinterDriver stellt die Treiber für eine Win32- \_ Drucker Instanz dar.
ms.assetid: baf48bbf-60a3-4d9b-93b7-c1b22518a9c1
ms.tgt_platform: multiple
title: Win32_PrinterDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver
- Win32_PrinterDriver.Caption
- Win32_PrinterDriver.ConfigFile
- Win32_PrinterDriver.CreationClassName
- Win32_PrinterDriver.DataFile
- Win32_PrinterDriver.DefaultDataType
- Win32_PrinterDriver.DependentFiles
- Win32_PrinterDriver.Description
- Win32_PrinterDriver.DriverPath
- Win32_PrinterDriver.FilePath
- Win32_PrinterDriver.HelpFile
- Win32_PrinterDriver.InfName
- Win32_PrinterDriver.InstallDate
- Win32_PrinterDriver.MonitorName
- Win32_PrinterDriver.Name
- Win32_PrinterDriver.OEMUrl
- Win32_PrinterDriver.Started
- Win32_PrinterDriver.StartMode
- Win32_PrinterDriver.Status
- Win32_PrinterDriver.SupportedPlatform
- Win32_PrinterDriver.SystemCreationClassName
- Win32_PrinterDriver.SystemName
- Win32_PrinterDriver.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 615d6561e12f67edee34e0de84dade12f250e0f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861172"
---
# <a name="win32_printerdriver-class"></a><span data-ttu-id="7e27d-103">Win32 \_ PrinterDriver-Klasse</span><span class="sxs-lookup"><span data-stu-id="7e27d-103">Win32\_PrinterDriver class</span></span>

<span data-ttu-id="7e27d-104">Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) von **Win32 \_ PrinterDriver** stellt die Treiber für eine [**Win32- \_ Drucker**](win32-printer.md) Instanz dar.</span><span class="sxs-lookup"><span data-stu-id="7e27d-104">The **Win32\_PrinterDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the drivers for a [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="7e27d-105">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften, schließt jedoch Methoden aus.</span><span class="sxs-lookup"><span data-stu-id="7e27d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties, but excludes methods.</span></span> <span data-ttu-id="7e27d-106">Referenzinformationen zu Methoden finden Sie in der Tabelle mit den Methoden in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="7e27d-106">For reference information about methods, see the table of methods in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e27d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e27d-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriver : CIM_Service
{
  string   Caption;
  string   ConfigFile;
  string   CreationClassName;
  string   DataFile;
  string   DefaultDataType;
  string   DependentFiles[];
  string   Description;
  string   DriverPath;
  string   FilePath;
  string   HelpFile;
  string   InfName;
  datetime InstallDate;
  string   MonitorName;
  string   Name;
  string   OEMUrl;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SupportedPlatform;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Version;
};
```

## <a name="members"></a><span data-ttu-id="7e27d-108">Member</span><span class="sxs-lookup"><span data-stu-id="7e27d-108">Members</span></span>

<span data-ttu-id="7e27d-109">Die **Win32 \_ PrinterDriver** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7e27d-109">The **Win32\_PrinterDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="7e27d-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="7e27d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7e27d-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e27d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7e27d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="7e27d-112">Methods</span></span>

<span data-ttu-id="7e27d-113">Die **Win32 \_ PrinterDriver** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="7e27d-113">The **Win32\_PrinterDriver** class has these methods.</span></span>



| <span data-ttu-id="7e27d-114">Methode</span><span class="sxs-lookup"><span data-stu-id="7e27d-114">Method</span></span>                                                                           | <span data-ttu-id="7e27d-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e27d-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="7e27d-116">**Addprinterdriver**</span><span class="sxs-lookup"><span data-stu-id="7e27d-116">**AddPrinterDriver**</span></span>](addprinterdriver-method-in-class-win32-printerdriver.md) | <span data-ttu-id="7e27d-117">Erstellt einen neuen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-117">Creates a new printer driver.</span></span><br/> |
| [<span data-ttu-id="7e27d-118">**Start Service**</span><span class="sxs-lookup"><span data-stu-id="7e27d-118">**StartService**</span></span>](startservice-method-in-class-win32-printerdriver.md)         | <span data-ttu-id="7e27d-119">Startet den Druckdienst.</span><span class="sxs-lookup"><span data-stu-id="7e27d-119">Starts print service.</span></span><br/>         |
| [<span data-ttu-id="7e27d-120">**Stop Service**</span><span class="sxs-lookup"><span data-stu-id="7e27d-120">**StopService**</span></span>](stopservice-method-in-class-win32-printerdriver.md)           | <span data-ttu-id="7e27d-121">Beendet den Druckdienst.</span><span class="sxs-lookup"><span data-stu-id="7e27d-121">Stops print service.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="7e27d-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7e27d-122">Properties</span></span>

<span data-ttu-id="7e27d-123">Die **Win32 \_ PrinterDriver** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7e27d-123">The **Win32\_PrinterDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e27d-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7e27d-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-127">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7e27d-127">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-128">Kurze Beschreibung des Objekts – eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7e27d-128">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="7e27d-129">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-130">**ConfigFile**</span><span class="sxs-lookup"><span data-stu-id="7e27d-130">**ConfigFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-133">Konfigurationsdatei für diesen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-133">Configuration file for this printer driver.</span></span>

<span data-ttu-id="7e27d-134">Beispiel: "pscrptui.dll"</span><span class="sxs-lookup"><span data-stu-id="7e27d-134">Example: "pscrptui.dll"</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-135">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="7e27d-135">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-138">Qualifizierer: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Class Name")</span><span class="sxs-lookup"><span data-stu-id="7e27d-138">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-139">Der Name der Klasse oder der Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7e27d-139">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="7e27d-140">Wenn diese Eigenschaft mit den anderen Schlüsseleigenschaften dieser Klasse verwendet wird, können alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7e27d-140">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7e27d-141">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-141">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-142">**Datendatei**</span><span class="sxs-lookup"><span data-stu-id="7e27d-142">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-143">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-145">Qualifizierer: [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) (CIM \_ datafile. filename)</span><span class="sxs-lookup"><span data-stu-id="7e27d-145">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.FileName)</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-146">Die Datendatei für diesen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-146">Data file for this printer driver.</span></span>

<span data-ttu-id="7e27d-147">Beispiel: "qms810. PPD"</span><span class="sxs-lookup"><span data-stu-id="7e27d-147">Example: "qms810.ppd"</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-148">**Defaultdatatype**</span><span class="sxs-lookup"><span data-stu-id="7e27d-148">**DefaultDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-151">Der Standard Datentyp für diesen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-151">Default data type for this printer driver.</span></span>

<span data-ttu-id="7e27d-152">Beispiel: "EMF"</span><span class="sxs-lookup"><span data-stu-id="7e27d-152">Example: "EMF"</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-153">**Dependentfiles**</span><span class="sxs-lookup"><span data-stu-id="7e27d-153">**DependentFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-154">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="7e27d-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-156">Array abhängiger Dateien für diesen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-156">Array of dependent files for this printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-157">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7e27d-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-158">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-160">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="7e27d-160">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-161">Kommentar, der den Link beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-161">Comment that describes the link.</span></span>

<span data-ttu-id="7e27d-162">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-163">**DriverPath "**</span><span class="sxs-lookup"><span data-stu-id="7e27d-163">**DriverPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-165">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-166">Qualifizierer: [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) (CIM \_ datafile. Path)</span><span class="sxs-lookup"><span data-stu-id="7e27d-166">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.Path)</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-167">Der Pfad für diesen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-167">Path for this printer driver.</span></span>

<span data-ttu-id="7e27d-168">Beispiel: "C: \\ \\ Drivers \\ \\pscript.dll"</span><span class="sxs-lookup"><span data-stu-id="7e27d-168">Example: "C:\\\\drivers\\\\pscript.dll"</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-169">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="7e27d-169">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-170">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-171">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e27d-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-172">Der Pfad zur verwendeten INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="7e27d-172">Path to the INF file being used.</span></span>

<span data-ttu-id="7e27d-173">Beispiel: "c: \\ \\ Temp \\ \\ Driver"</span><span class="sxs-lookup"><span data-stu-id="7e27d-173">Example: "c:\\\\temp\\\\driver"</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-174">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="7e27d-174">**HelpFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-177">Hilfedatei für diesen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-177">Help file for this printer driver.</span></span>

<span data-ttu-id="7e27d-178">Beispiel: "PSCRPTUI. hlp"</span><span class="sxs-lookup"><span data-stu-id="7e27d-178">Example: "pscrptui.hlp"</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-179">**InfName**</span><span class="sxs-lookup"><span data-stu-id="7e27d-179">**InfName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-180">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-181">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e27d-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-182">Der Name der verwendeten INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="7e27d-182">Name of the INF file being used.</span></span> <span data-ttu-id="7e27d-183">Standardmäßig wird eine vom Betriebssystem bereitgestellte Drucker-INF-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="7e27d-183">The default is to use an operating system provided printer INF file.</span></span> <span data-ttu-id="7e27d-184">Ein anderer Dateiname wird verwendet, wenn der Treiber direkt vom Hersteller des Druckers und nicht vom Betriebssystem bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7e27d-184">A different file name is used if the driver is provided directly by the manufacturer of the printer and not the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-185">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7e27d-185">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-186">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="7e27d-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-188">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](../wmisdk/standard-qualifiers.md) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="7e27d-188">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-189">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="7e27d-189">Date and time the object is installed.</span></span> <span data-ttu-id="7e27d-190">Diese Eigenschaft erfordert keinen Wert, um anzugeben, dass das-Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="7e27d-190">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7e27d-191">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-192">**MonitorName**</span><span class="sxs-lookup"><span data-stu-id="7e27d-192">**MonitorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-193">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-195">Der Name des Monitors für diesen Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-195">Name of the monitor for this printer driver.</span></span>

<span data-ttu-id="7e27d-196">Beispiel: "PJL-Monitor"</span><span class="sxs-lookup"><span data-stu-id="7e27d-196">Example: "PJL monitor"</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-197">**Name**</span><span class="sxs-lookup"><span data-stu-id="7e27d-197">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-198">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-199">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-200">Qualifizierer: [ **Schlüssel**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="7e27d-200">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-201">Treiber Name für diesen Drucker.</span><span class="sxs-lookup"><span data-stu-id="7e27d-201">Driver name for this printer.</span></span> <span data-ttu-id="7e27d-202">Dabei handelt es sich um einen zusammengesetzten Schlüssel, der aus den Werten **Name**, **Version** und **SupportedPlatform** besteht.</span><span class="sxs-lookup"><span data-stu-id="7e27d-202">This is a compound key composed of the **Name**, **Version**, and **SupportedPlatform** values.</span></span>

<span data-ttu-id="7e27d-203">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) geerbt und überschreibt die **namens** Definition in dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="7e27d-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) and overrides the **Name** definition in that class.</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-204">**Oemurl**</span><span class="sxs-lookup"><span data-stu-id="7e27d-204">**OEMUrl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-205">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-207">World Wide Web (www) Link zur Website des Druckerherstellers.</span><span class="sxs-lookup"><span data-stu-id="7e27d-207">World Wide Web (WWW) link to the printer manufacturer's website.</span></span> <span data-ttu-id="7e27d-208">Beachten Sie, dass diese Eigenschaft nicht aufgefüllt wird, wenn die Win32. inf-Datei verwendet wird, und gilt nur für Treiber, die direkt vom Hersteller bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7e27d-208">Note that this property is not populated when the Win32.inf file is used, and is only applicable for drivers provided directly from the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-209">**Gestartet**</span><span class="sxs-lookup"><span data-stu-id="7e27d-209">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-210">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="7e27d-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-211">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-212">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="7e27d-212">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-213">**True** gibt an, dass der Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7e27d-213">If **TRUE**, the service is started.</span></span> <span data-ttu-id="7e27d-214">Wenn der Wert **false** ist, wird der Dienst beendet.</span><span class="sxs-lookup"><span data-stu-id="7e27d-214">If **FALSE**, the service is stopped.</span></span>

<span data-ttu-id="7e27d-215">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-215">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-216">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="7e27d-216">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-217">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-219">Qualifizierer: [**Display Name**](../wmisdk/standard-qualifiers.md) ("Start Modus")</span><span class="sxs-lookup"><span data-stu-id="7e27d-219">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-220">Der Start Modus des Dienstanbieter wird automatisch von einem Betriebssystem gestartet oder nur bei Anforderung gestartet.</span><span class="sxs-lookup"><span data-stu-id="7e27d-220">Start mode of the service is automatically started by an operating system, or only started when requested.</span></span>

<span data-ttu-id="7e27d-221">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-221">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="7e27d-222">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="7e27d-222">The following are possible values:</span></span>

<dl> <dd><span data-ttu-id="7e27d-223">Schem</span><span class="sxs-lookup"><span data-stu-id="7e27d-223">"Automatic"</span></span></dd> <dd><span data-ttu-id="7e27d-224">Manual</span><span class="sxs-lookup"><span data-stu-id="7e27d-224">"Manual"</span></span></dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="7e27d-225">**Automatisch** ("automatisch")</span><span class="sxs-lookup"><span data-stu-id="7e27d-225">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="7e27d-226">**Manuell** ("manuell")</span><span class="sxs-lookup"><span data-stu-id="7e27d-226">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e27d-227">**Status**</span><span class="sxs-lookup"><span data-stu-id="7e27d-227">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-228">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-230">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**Display Name**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="7e27d-230">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-231">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7e27d-231">Current status of the object.</span></span> <span data-ttu-id="7e27d-232">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7e27d-232">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7e27d-233">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="7e27d-233">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7e27d-234">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="7e27d-234">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7e27d-235">Der letztere Dienst kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e27d-235">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7e27d-236">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="7e27d-236">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7e27d-237">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7e27d-238">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="7e27d-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7e27d-239">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7e27d-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7e27d-240">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="7e27d-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7e27d-241">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="7e27d-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e27d-242">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="7e27d-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7e27d-243">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7e27d-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7e27d-244">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="7e27d-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7e27d-245">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="7e27d-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7e27d-246">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="7e27d-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7e27d-247">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="7e27d-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7e27d-248">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="7e27d-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7e27d-249">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="7e27d-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7e27d-250">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="7e27d-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e27d-251">**SupportedPlatform**</span><span class="sxs-lookup"><span data-stu-id="7e27d-251">**SupportedPlatform**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-252">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-253">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e27d-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-254">Betriebsumgebungen, für die der Treiber vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="7e27d-254">Operating environments that the driver is intended for.</span></span>

<span data-ttu-id="7e27d-255">Beispiel: "Windows NT x86".</span><span class="sxs-lookup"><span data-stu-id="7e27d-255">Example: "Windows NT x86".</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-256">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="7e27d-256">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-257">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-258">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-259">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**CIM- \_ Schlüssel**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) ("System Klassenname")</span><span class="sxs-lookup"><span data-stu-id="7e27d-259">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-260">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="7e27d-260">Scoping system's creation class name.</span></span>

<span data-ttu-id="7e27d-261">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-262">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="7e27d-262">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-263">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7e27d-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7e27d-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-265">Qualifizierer [**: weiter**](../wmisdk/standard-qualifiers.md) gegeben ("[**CIM- \_ System**](cim-system.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**Display Name**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="7e27d-265">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-266">Der Name des Systems, das den Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="7e27d-266">Name of the system that hosts this service.</span></span>

<span data-ttu-id="7e27d-267">Diese Eigenschaft wird vom [**CIM- \_ Dienst**](cim-service.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7e27d-267">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e27d-268">**Version**</span><span class="sxs-lookup"><span data-stu-id="7e27d-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e27d-269">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e27d-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e27d-270">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7e27d-270">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7e27d-271">Betriebssystemversion für den Druckertreiber.</span><span class="sxs-lookup"><span data-stu-id="7e27d-271">Operating system version for the printer driver.</span></span>

<dt>

<span id="3"></span>

<span data-ttu-id="7e27d-272"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="7e27d-272"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="7e27d-273">Win2k</span><span class="sxs-lookup"><span data-stu-id="7e27d-273">Win2k</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e27d-274">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e27d-274">Remarks</span></span>

<span data-ttu-id="7e27d-275">Die **Win32-Klasse \_ PrinterDriver** wird vom [**CIM- \_ Dienst**](cim-service.md) abgeleitet, der von [**CIM \_ LogicalElement**](cim-logicalelement.md)abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7e27d-275">The **Win32\_PrinterDriver** class is derived from [**CIM\_Service**](cim-service.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="7e27d-276">Benutzer können einen Druckertreiber deinstallieren, indem Sie eine entsprechende Instanz dieser Klasse löschen.</span><span class="sxs-lookup"><span data-stu-id="7e27d-276">Users can uninstall a printer driver by deleting a corresponding instance of this class.</span></span> <span data-ttu-id="7e27d-277">Zu diesem Zweck muss für den aufrufenden Prozess die **SeLoadDriverPrivilege** -Berechtigung festgelegt sein, um eine Instanz dieser Klasse löschen zu können.</span><span class="sxs-lookup"><span data-stu-id="7e27d-277">To do so, the calling process must have the **SeLoadDriverPrivilege** privilege set to delete an instance of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="7e27d-278">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e27d-278">Examples</span></span>

<span data-ttu-id="7e27d-279">Im VBScript-Beispiel zum [Verwalten von Drucker-und Druckertreibern](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) werden Druckertreiber und Drucker Anschlüsse verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7e27d-279">The [Manage Printer and Printer Drivers](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) VBScript sample manages printer drivers and printer ports.</span></span>

<span data-ttu-id="7e27d-280">In den [TechNet-Foren](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) wird beschrieben, wie ein Drucker erstellt und Treiber von einem Server hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="7e27d-280">The following [discussion on the TechNet forums](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) describes how to create a printer and upload drivers from a server.</span></span>

<span data-ttu-id="7e27d-281">Im folgenden VBScript-Beispiel werden alle Druckertreiber aufgelistet, die auf einem Computer installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7e27d-281">The following VBScript sample lists all the printer drivers that have been installed on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrinterDriver") 
 
For each objPrinter in colInstalledPrinters 
    Wscript.Echo "Configuration File: " & objPrinter.ConfigFile 
    Wscript.Echo "Data File: " & objPrinter.DataFile 
    Wscript.Echo "Description: " & objPrinter.Description 
    Wscript.Echo "Driver Path: " & objPrinter.DriverPath 
    Wscript.Echo "File Path: " & objPrinter.FilePath 
    Wscript.Echo "Help File: " & objPrinter.HelpFile 
    Wscript.Echo "INF Name: " & objPrinter.InfName 
    Wscript.Echo "Monitor Name: " & objPrinter.MonitorName 
    Wscript.Echo "Name: " & objPrinter.Name 
    Wscript.Echo "OEM Url: " & objPrinter.OEMUrl 
    Wscript.Echo "Supported Platform: " & objPrinter.SupportedPlatform 
    Wscript.Echo "Version: " & objPrinter.Version 
Next 
```



## <a name="requirements"></a><span data-ttu-id="7e27d-282">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e27d-282">Requirements</span></span>



| <span data-ttu-id="7e27d-283">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e27d-283">Requirement</span></span> | <span data-ttu-id="7e27d-284">Wert</span><span class="sxs-lookup"><span data-stu-id="7e27d-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e27d-285">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e27d-285">Minimum supported client</span></span><br/> | <span data-ttu-id="7e27d-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e27d-286">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7e27d-287">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e27d-287">Minimum supported server</span></span><br/> | <span data-ttu-id="7e27d-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e27d-288">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7e27d-289">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e27d-289">Namespace</span></span><br/>                | <span data-ttu-id="7e27d-290">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7e27d-290">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="7e27d-291">MOF</span><span class="sxs-lookup"><span data-stu-id="7e27d-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e27d-292"><dt>Win32 \_ Printer. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7e27d-292"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e27d-293">DLL</span><span class="sxs-lookup"><span data-stu-id="7e27d-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e27d-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e27d-294"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7e27d-295">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e27d-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e27d-296">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="7e27d-296">**CIM\_Service**</span></span>](./cim-service.md)
</dt> <dt>

[<span data-ttu-id="7e27d-297">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="7e27d-297">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
