---
description: Die CIM- \_ directoryspecification-Klasse erfasst die Hauptverzeichnis Struktur eines Software Elements. Diese Klasse wird verwendet, um die Dateien eines Software Elements in verwaltbaren Einheiten zu organisieren, die auf einem Computersystem verschoben werden können.
ms.assetid: faeab356-e470-477b-97d2-1a19ce1d8d21
ms.tgt_platform: multiple
title: CIM_DirectorySpecification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification
- CIM_DirectorySpecification.CheckID
- CIM_DirectorySpecification.Caption
- CIM_DirectorySpecification.Description
- CIM_DirectorySpecification.CheckMode
- CIM_DirectorySpecification.Name
- CIM_DirectorySpecification.TargetOperatingSystem
- CIM_DirectorySpecification.Version
- CIM_DirectorySpecification.SoftwareElementID
- CIM_DirectorySpecification.SoftwareElementState
- CIM_DirectorySpecification.DirectoryPath
- CIM_DirectorySpecification.DirectoryType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6a7eb6ae627c8ed9b5639e573e1d2d89132698ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127185"
---
# <a name="cim_directoryspecification-class"></a><span data-ttu-id="60275-104">CIM- \_ directoryspecification-Klasse</span><span class="sxs-lookup"><span data-stu-id="60275-104">CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="60275-105">Die **CIM- \_ directoryspecification** -Klasse erfasst die Hauptverzeichnis Struktur eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="60275-105">The **CIM\_DirectorySpecification** class captures the major directory structure of a software element.</span></span> <span data-ttu-id="60275-106">Diese Klasse wird verwendet, um die Dateien eines Software Elements in verwaltbaren Einheiten zu organisieren, die auf einem Computersystem verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="60275-106">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60275-107">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="60275-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="60275-108">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="60275-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="60275-109">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="60275-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="60275-110">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="60275-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="60275-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="60275-111">Syntax</span></span>

``` syntax
[UUID("{A524EE6E-DB29-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_DirectorySpecification : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  string  DirectoryPath;
  uint16  DirectoryType;
};
```

## <a name="members"></a><span data-ttu-id="60275-112">Member</span><span class="sxs-lookup"><span data-stu-id="60275-112">Members</span></span>

<span data-ttu-id="60275-113">Die **CIM- \_ directoryspecification** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="60275-113">The **CIM\_DirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="60275-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="60275-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="60275-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60275-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60275-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="60275-116">Methods</span></span>

<span data-ttu-id="60275-117">Die **CIM- \_ directoryspecification** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="60275-117">The **CIM\_DirectorySpecification** class has these methods.</span></span>



| <span data-ttu-id="60275-118">Methode</span><span class="sxs-lookup"><span data-stu-id="60275-118">Method</span></span>                                                              | <span data-ttu-id="60275-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60275-119">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="60275-120">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="60275-120">**Invoke**</span></span>](invoke-method-in-class-cim-directoryspecification.md) | <span data-ttu-id="60275-121">Wertet eine bestimmte Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="60275-121">Evaluates a particular check.</span></span> <span data-ttu-id="60275-122">Diese Methode wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="60275-122">This method is not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="60275-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="60275-123">Properties</span></span>

<span data-ttu-id="60275-124">Die **CIM- \_ directoryspecification** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60275-124">The **CIM\_DirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60275-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="60275-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60275-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60275-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-128">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="60275-128">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="60275-129">Eine kurze Textbeschreibung des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="60275-129">A short textual description of the subject.</span></span>

<span data-ttu-id="60275-130">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-130">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="60275-131">**CheckId**</span><span class="sxs-lookup"><span data-stu-id="60275-131">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60275-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60275-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-134">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="60275-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="60275-135">Bezeichner, der in Verbindung mit anderen Schlüsseln zum eindeutigen Identifizieren der Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60275-135">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="60275-136">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="60275-137">**Checkmode**</span><span class="sxs-lookup"><span data-stu-id="60275-137">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-138">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="60275-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60275-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60275-140">Wenn der Wert **true** ist, wird erwartet, dass die Bedingung in der Umgebung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="60275-140">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="60275-141">Beispielsweise wird erwartet, dass eine Datei auf einem System ausgeführt wird, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="60275-141">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="60275-142">Wenn der Wert **false** ist, wird erwartet, dass die Bedingung nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="60275-142">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="60275-143">Eine Datei befindet sich z. b. nicht in einem System, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="60275-143">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="60275-144">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="60275-145">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60275-145">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60275-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60275-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60275-148">Eine Beschreibung der-Objekte.</span><span class="sxs-lookup"><span data-stu-id="60275-148">A description of the objects.</span></span>

<span data-ttu-id="60275-149">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-149">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="60275-150">**DirectoryPath**</span><span class="sxs-lookup"><span data-stu-id="60275-150">**DirectoryPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60275-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60275-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-153">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="60275-153">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="60275-154">Verzeichnisname.</span><span class="sxs-lookup"><span data-stu-id="60275-154">Directory name.</span></span> <span data-ttu-id="60275-155">Der von einem Anwendungsanbieter bereitgestellte Wert ist ein standardmäßiger oder empfohlener Pfadname.</span><span class="sxs-lookup"><span data-stu-id="60275-155">The value supplied by an application provider is a default or recommended path name.</span></span> <span data-ttu-id="60275-156">Der Wert kann für eine bestimmte Umgebung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="60275-156">The value can be changed for a particular environment.</span></span>

</dd> <dt>

<span data-ttu-id="60275-157">**Directerytype**</span><span class="sxs-lookup"><span data-stu-id="60275-157">**DirectoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-158">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60275-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60275-159">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-160">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speicherort \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="60275-160">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Location\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="60275-161">Der Typ des Verzeichnisses, das beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="60275-161">Type of directory being described.</span></span>

<dt>

<span id="Product_base_directory"></span><span id="product_base_directory"></span><span id="PRODUCT_BASE_DIRECTORY"></span>

<span data-ttu-id="60275-162">**Produktbasis Verzeichnis** (0)</span><span class="sxs-lookup"><span data-stu-id="60275-162">**Product base directory** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_executable_directory"></span><span id="product_executable_directory"></span><span id="PRODUCT_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="60275-163">**Ausführbares Produktverzeichnis** (1)</span><span class="sxs-lookup"><span data-stu-id="60275-163">**Product executable directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_library_directory"></span><span id="product_library_directory"></span><span id="PRODUCT_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="60275-164">**Produkt Bibliotheksverzeichnis** (2)</span><span class="sxs-lookup"><span data-stu-id="60275-164">**Product library directory** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_configuration_directory"></span><span id="product_configuration_directory"></span><span id="PRODUCT_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="60275-165">**Produkt Konfigurationsverzeichnis** (3)</span><span class="sxs-lookup"><span data-stu-id="60275-165">**Product configuration directory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_include_directory"></span><span id="product_include_directory"></span><span id="PRODUCT_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="60275-166">**Produkt Include-Verzeichnis** (4)</span><span class="sxs-lookup"><span data-stu-id="60275-166">**Product include directory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_working_directory"></span><span id="product_working_directory"></span><span id="PRODUCT_WORKING_DIRECTORY"></span>

<span data-ttu-id="60275-167">**Produkt Arbeitsverzeichnis** (5)</span><span class="sxs-lookup"><span data-stu-id="60275-167">**Product working directory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Product_log_directory"></span><span id="product_log_directory"></span><span id="PRODUCT_LOG_DIRECTORY"></span>

<span data-ttu-id="60275-168">**Produkt Protokoll Verzeichnis** (6)</span><span class="sxs-lookup"><span data-stu-id="60275-168">**Product log directory** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_base_directory"></span><span id="shared_base_directory"></span><span id="SHARED_BASE_DIRECTORY"></span>

<span data-ttu-id="60275-169">Frei gegebenes **Basisverzeichnis** (7)</span><span class="sxs-lookup"><span data-stu-id="60275-169">**Shared base directory** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_executable_directory"></span><span id="shared_executable_directory"></span><span id="SHARED_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="60275-170">Frei gegebenes **Verzeichnis** (8)</span><span class="sxs-lookup"><span data-stu-id="60275-170">**Shared executable directory** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_library_directory"></span><span id="shared_library_directory"></span><span id="SHARED_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="60275-171">**Verzeichnis für freigegebene Bibliotheken** (9)</span><span class="sxs-lookup"><span data-stu-id="60275-171">**Shared library directory** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Shared_include_directory"></span><span id="shared_include_directory"></span><span id="SHARED_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="60275-172">**Shared Include-Verzeichnis** (10)</span><span class="sxs-lookup"><span data-stu-id="60275-172">**Shared include directory** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="System_base_directory"></span><span id="system_base_directory"></span><span id="SYSTEM_BASE_DIRECTORY"></span>

<span data-ttu-id="60275-173">**System Basisverzeichnis** (11)</span><span class="sxs-lookup"><span data-stu-id="60275-173">**System base directory** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="System_executable_directory"></span><span id="system_executable_directory"></span><span id="SYSTEM_EXECUTABLE_DIRECTORY"></span>

<span data-ttu-id="60275-174">**Ausführbares System Verzeichnis** (12)</span><span class="sxs-lookup"><span data-stu-id="60275-174">**System executable directory** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="System_library_directory"></span><span id="system_library_directory"></span><span id="SYSTEM_LIBRARY_DIRECTORY"></span>

<span data-ttu-id="60275-175">**System Bibliotheksverzeichnis** (13)</span><span class="sxs-lookup"><span data-stu-id="60275-175">**System library directory** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="System_configuration_directory"></span><span id="system_configuration_directory"></span><span id="SYSTEM_CONFIGURATION_DIRECTORY"></span>

<span data-ttu-id="60275-176">**Systemkonfigurationsverzeichnis** (14)</span><span class="sxs-lookup"><span data-stu-id="60275-176">**System configuration directory** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="System_include_directory"></span><span id="system_include_directory"></span><span id="SYSTEM_INCLUDE_DIRECTORY"></span>

<span data-ttu-id="60275-177">**System Include-Verzeichnis** (15)</span><span class="sxs-lookup"><span data-stu-id="60275-177">**System include directory** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="System_log_directory"></span><span id="system_log_directory"></span><span id="SYSTEM_LOG_DIRECTORY"></span>

<span data-ttu-id="60275-178">**System Protokoll Verzeichnis** (16)</span><span class="sxs-lookup"><span data-stu-id="60275-178">**System log directory** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="60275-179">**Sonstige** (17)</span><span class="sxs-lookup"><span data-stu-id="60275-179">**Other** (17)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60275-180">**Name**</span><span class="sxs-lookup"><span data-stu-id="60275-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-181">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60275-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60275-182">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-183">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="60275-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="60275-184">Der Name, der zum Identifizieren des Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="60275-184">Name used to identify the software element</span></span>

<span data-ttu-id="60275-185">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="60275-186">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="60275-186">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-187">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60275-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60275-188">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-189">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="60275-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="60275-190">Dies ist ein Bezeichner für dieses Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="60275-190">This is an identifier for this software element.</span></span>

<span data-ttu-id="60275-191">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="60275-192">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="60275-192">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-193">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60275-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60275-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-195">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="60275-195">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="60275-196">Der Softwareelement Zustand eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="60275-196">The software element state of a software element.</span></span>

<span data-ttu-id="60275-197">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-197">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="60275-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="60275-198"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="60275-199">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60275-199">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="60275-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="60275-200"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="60275-201">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60275-201">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="60275-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="60275-202"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="60275-203">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60275-203">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="60275-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="60275-204"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="60275-205">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="60275-205">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="60275-206">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="60275-206">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-207">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60275-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60275-208">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-209">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="60275-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="60275-210">Ziel Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="60275-210">Target operating system of the software element.</span></span>

<span data-ttu-id="60275-211">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-211">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60275-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="60275-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="60275-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="60275-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="60275-214"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="60275-214"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="60275-215">Mac OS</span><span class="sxs-lookup"><span data-stu-id="60275-215">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="60275-216"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="60275-216"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="60275-217">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="60275-217">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="60275-218"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="60275-218"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="60275-219"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="60275-219"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="60275-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="60275-220"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="60275-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="60275-221"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="60275-222">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="60275-222">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="60275-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="60275-223"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="60275-224">HP-UX</span><span class="sxs-lookup"><span data-stu-id="60275-224">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="60275-225"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="60275-225"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="60275-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="60275-226"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="60275-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="60275-227"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="60275-228"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="60275-228"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="60275-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="60275-229"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="60275-230">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="60275-230">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="60275-231"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="60275-231"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="60275-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="60275-232"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="60275-233">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="60275-233">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="60275-234"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="60275-234"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="60275-235">Windows 95</span><span class="sxs-lookup"><span data-stu-id="60275-235">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="60275-236"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="60275-236"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="60275-237">Windows 98</span><span class="sxs-lookup"><span data-stu-id="60275-237">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="60275-238"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="60275-238"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="60275-239">Windows NT</span><span class="sxs-lookup"><span data-stu-id="60275-239">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="60275-240"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="60275-240"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="60275-241">Windows CE</span><span class="sxs-lookup"><span data-stu-id="60275-241">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="60275-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="60275-242"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="60275-243">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="60275-243">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="60275-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="60275-244"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="60275-245"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="60275-245"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="60275-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="60275-246"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="60275-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="60275-247"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="60275-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="60275-248"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="60275-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="60275-249"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="60275-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="60275-250"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="60275-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="60275-251"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="60275-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="60275-252"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="60275-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="60275-253"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="60275-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="60275-254"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="60275-255"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="60275-255"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="60275-256">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="60275-256">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="60275-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="60275-257"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="60275-258">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="60275-258">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="60275-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="60275-259"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="60275-260">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="60275-260">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="60275-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="60275-261"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="60275-262">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="60275-262">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="60275-263"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="60275-263"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="60275-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="60275-264"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="60275-265"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="60275-265"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="60275-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="60275-266"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="60275-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="60275-267"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="60275-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="60275-268"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="60275-269">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="60275-269">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="60275-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="60275-270"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="60275-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="60275-271"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="60275-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="60275-272"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="60275-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="60275-273"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="60275-274">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="60275-274">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="60275-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="60275-275"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="60275-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="60275-276"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="60275-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="60275-277"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="60275-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="60275-278"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="60275-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="60275-279"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="60275-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="60275-280"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="60275-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="60275-281"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="60275-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="60275-282"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="60275-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="60275-283"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="60275-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="60275-284"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="60275-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="60275-285"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="60275-286">Palm OS</span><span class="sxs-lookup"><span data-stu-id="60275-286">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="60275-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="60275-287"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="60275-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="60275-288"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="60275-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="60275-289"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="60275-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="60275-290"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="60275-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="60275-291"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60275-292">**Version**</span><span class="sxs-lookup"><span data-stu-id="60275-292">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60275-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="60275-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60275-294">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="60275-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60275-295">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="60275-295">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="60275-296">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="60275-296">Version of the operation.</span></span>

<span data-ttu-id="60275-297">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="60275-297">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="60275-298"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="60275-298"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="60275-299"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="60275-299"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="60275-300">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="60275-300">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60275-301">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60275-301">Remarks</span></span>

<span data-ttu-id="60275-302">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="60275-302">WMI does not implement this class.</span></span> <span data-ttu-id="60275-303">Informationen zu Klassen, die von **CIM \_ directoryspecification** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="60275-303">For classes derived from **CIM\_DirectorySpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="60275-304">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="60275-304">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="60275-305">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="60275-305">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="60275-306">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60275-306">Requirements</span></span>



| <span data-ttu-id="60275-307">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60275-307">Requirement</span></span> | <span data-ttu-id="60275-308">Wert</span><span class="sxs-lookup"><span data-stu-id="60275-308">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60275-309">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60275-309">Minimum supported client</span></span><br/> | <span data-ttu-id="60275-310">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60275-310">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60275-311">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60275-311">Minimum supported server</span></span><br/> | <span data-ttu-id="60275-312">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60275-312">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60275-313">Namespace</span><span class="sxs-lookup"><span data-stu-id="60275-313">Namespace</span></span><br/>                | <span data-ttu-id="60275-314">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="60275-314">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60275-315">MOF</span><span class="sxs-lookup"><span data-stu-id="60275-315">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60275-316"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="60275-316"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60275-317">DLL</span><span class="sxs-lookup"><span data-stu-id="60275-317">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60275-318"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60275-318"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60275-319">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60275-319">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60275-320">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="60275-320">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

