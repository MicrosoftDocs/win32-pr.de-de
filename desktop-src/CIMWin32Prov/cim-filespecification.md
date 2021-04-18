---
description: Die CIM- \_ filespecification-Klasse stellt eine Datei dar, die sich entweder in einem oder aus dem System befindet.
ms.assetid: 25d6cc79-1497-4615-9251-8e00524dff1b
ms.tgt_platform: multiple
title: CIM_FileSpecification-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileSpecification
- CIM_FileSpecification.CheckID
- CIM_FileSpecification.Caption
- CIM_FileSpecification.Description
- CIM_FileSpecification.CheckMode
- CIM_FileSpecification.TargetOperatingSystem
- CIM_FileSpecification.Version
- CIM_FileSpecification.SoftwareElementID
- CIM_FileSpecification.SoftwareElementState
- CIM_FileSpecification.Name
- CIM_FileSpecification.CheckSum
- CIM_FileSpecification.CRC1
- CIM_FileSpecification.CRC2
- CIM_FileSpecification.CreateTimeStamp
- CIM_FileSpecification.FileSize
- CIM_FileSpecification.MD5Checksum
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 503cf9678d2be7a3afb3f8c205f0d042b4bcaec2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345442"
---
# <a name="cim_filespecification-class"></a><span data-ttu-id="91dbf-103">CIM- \_ filespecification-Klasse</span><span class="sxs-lookup"><span data-stu-id="91dbf-103">CIM\_FileSpecification class</span></span>

<span data-ttu-id="91dbf-104">Die **CIM- \_ filespecification** -Klasse stellt eine Datei dar, die sich entweder in einem oder aus dem System befindet.</span><span class="sxs-lookup"><span data-stu-id="91dbf-104">The **CIM\_FileSpecification** class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="91dbf-105">Die Datei befindet sich in dem Verzeichnis, das durch die [**CIM \_ Director yspecificationfile-Zuordnung**](cim-directoryspecificationfile.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="91dbf-105">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="91dbf-106">Die [**Aufruf**](invoke-method-in-class-cim-filespecification.md) Methode verwendet die Informationen, um zu überprüfen, ob die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="91dbf-106">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="91dbf-107">Beachten Sie, dass Eigenschaften mit einem **null** -Wert nicht geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="91dbf-107">Note that properties with a **Null** value are not checked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91dbf-108">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="91dbf-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="91dbf-109">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="91dbf-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="91dbf-110">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="91dbf-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="91dbf-111">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="91dbf-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="91dbf-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="91dbf-112">Syntax</span></span>

``` syntax
[UUID("{41F377B0-DB2A-11d2-85FC-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_FileSpecification : CIM_Check
{
  string   CheckID;
  string   Caption;
  string   Description;
  boolean  CheckMode;
  uint16   TargetOperatingSystem;
  string   Version;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Name;
  uint32   CheckSum;
  uint32   CRC1;
  uint32   CRC2;
  datetime CreateTimeStamp;
  uint64   FileSize;
  string   MD5Checksum;
};
```

## <a name="members"></a><span data-ttu-id="91dbf-113">Member</span><span class="sxs-lookup"><span data-stu-id="91dbf-113">Members</span></span>

<span data-ttu-id="91dbf-114">Die **CIM- \_ filespecification** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="91dbf-114">The **CIM\_FileSpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="91dbf-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="91dbf-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="91dbf-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91dbf-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="91dbf-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="91dbf-117">Methods</span></span>

<span data-ttu-id="91dbf-118">Die **CIM- \_ filespecification** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="91dbf-118">The **CIM\_FileSpecification** class has these methods.</span></span>



| <span data-ttu-id="91dbf-119">Methode</span><span class="sxs-lookup"><span data-stu-id="91dbf-119">Method</span></span>                                                         | <span data-ttu-id="91dbf-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91dbf-120">Description</span></span>                                                      |
|:---------------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="91dbf-121">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="91dbf-121">**Invoke**</span></span>](invoke-method-in-class-cim-filespecification.md) | <span data-ttu-id="91dbf-122">Wertet eine bestimmte Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="91dbf-122">Evaluates a particular check.</span></span> <span data-ttu-id="91dbf-123">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="91dbf-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="91dbf-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="91dbf-124">Properties</span></span>

<span data-ttu-id="91dbf-125">Die **CIM- \_ filespecification** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="91dbf-125">The **CIM\_FileSpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91dbf-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="91dbf-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dbf-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-129">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="91dbf-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-130">Eine kurze Textbeschreibung des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="91dbf-130">A short textual description of the subject.</span></span>

<span data-ttu-id="91dbf-131">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-132">**CheckId**</span><span class="sxs-lookup"><span data-stu-id="91dbf-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dbf-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-135">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="91dbf-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-136">Bezeichner, der in Verbindung mit anderen Schlüsseln zum eindeutigen Identifizieren der Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91dbf-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="91dbf-137">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-138">**Checkmode**</span><span class="sxs-lookup"><span data-stu-id="91dbf-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-139">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="91dbf-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-141">Wenn der Wert **true** ist, wird erwartet, dass die Bedingung in der Umgebung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="91dbf-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="91dbf-142">Beispielsweise wird erwartet, dass eine Datei auf einem System ausgeführt wird, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="91dbf-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="91dbf-143">Wenn der Wert **false** ist, wird erwartet, dass die Bedingung nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="91dbf-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="91dbf-144">Eine Datei befindet sich z. b. nicht in einem System, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="91dbf-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="91dbf-145">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-146">**Prüfsumme**</span><span class="sxs-lookup"><span data-stu-id="91dbf-146">**CheckSum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91dbf-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-149">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Software Signatur \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="91dbf-149">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-150">Der Wert wird als 16-Bit-Summe der ersten 32 Bytes der Datei berechnet.</span><span class="sxs-lookup"><span data-stu-id="91dbf-150">Value calculated as the 16-bit sum of the file's first 32 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-151">**CRC1**</span><span class="sxs-lookup"><span data-stu-id="91dbf-151">**CRC1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-152">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91dbf-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-154">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Software Signatur \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="91dbf-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-155">CRC-Wert, berechnet mithilfe der mittleren 512 KB.</span><span class="sxs-lookup"><span data-stu-id="91dbf-155">CRC value calculated using the middle 512 KB.</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-156">**CRC2**</span><span class="sxs-lookup"><span data-stu-id="91dbf-156">**CRC2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-157">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91dbf-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-159">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Software Signatur \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="91dbf-159">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Signature\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-160">CRC-Wert für die mittlere 512 KB der Datei, Modulo 3.</span><span class="sxs-lookup"><span data-stu-id="91dbf-160">CRC value for the middle 512 KB of the file, modulo 3.</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-161">**"Kreatetimestamp"**</span><span class="sxs-lookup"><span data-stu-id="91dbf-161">**CreateTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-162">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="91dbf-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-163">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-164">Qualifizierer: [ **korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91dbf-164">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-165">Datum und Uhrzeit der Dateierstellung.</span><span class="sxs-lookup"><span data-stu-id="91dbf-165">File creation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-166">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91dbf-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dbf-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-169">Eine Beschreibung der-Objekte.</span><span class="sxs-lookup"><span data-stu-id="91dbf-169">A description of the objects.</span></span>

<span data-ttu-id="91dbf-170">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-170">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-171">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="91dbf-171">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-172">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91dbf-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-174">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte")</span><span class="sxs-lookup"><span data-stu-id="91dbf-174">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-175">Größe der Datei in Bytes.</span><span class="sxs-lookup"><span data-stu-id="91dbf-175">Size of the file, in bytes.</span></span>

<span data-ttu-id="91dbf-176">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="91dbf-176">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-177">**MD5Checksum**</span><span class="sxs-lookup"><span data-stu-id="91dbf-177">**MD5Checksum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dbf-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-180">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span><span class="sxs-lookup"><span data-stu-id="91dbf-180">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (16)</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-181">Algorithmus zum Berechnen einer 128-Bit-Prüfsumme für eine beliebige Datei oder ein beliebiges Objekt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-181">Algorithm for computing a 128-bit checksum for any file or object.</span></span> <span data-ttu-id="91dbf-182">Die Wahrscheinlichkeit, dass zwei verschiedene Dateien, die dieselbe MD5-Prüfsumme erzeugen, sehr klein ist (ungefähr 1 in 2 ^ 64), und die MD5-Prüfsumme einer Datei kann verwendet werden, um einen zuverlässigen Inhalts Bezeichner zu erstellen, der die Datei wahrscheinlich eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="91dbf-182">The likelihood of two different files producing the same MD5 checksum is very small (about 1 in 2^64), and the MD5 checksum of a file can be used to construct a reliable content identifier that is likely to uniquely identify the file.</span></span> <span data-ttu-id="91dbf-183">Das Gegenteil trifft ebenfalls zu.</span><span class="sxs-lookup"><span data-stu-id="91dbf-183">The reverse is also true.</span></span> <span data-ttu-id="91dbf-184">Wenn zwei Dateien dieselbe MD5-Prüfsumme aufweisen, ist es sehr wahrscheinlich, dass die Dateien identisch sind.</span><span class="sxs-lookup"><span data-stu-id="91dbf-184">If two files have the same MD5 checksum, it is very likely that the files are identical.</span></span> <span data-ttu-id="91dbf-185">Zum Zwecke der MOF-Spezifikation der MD5-Eigenschaft generiert der MD5-Algorithmus immer eine Zeichenfolge mit 32 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="91dbf-185">For purposes of MOF specification of the MD5 property, the MD5 algorithm always generates a 32-character string.</span></span> <span data-ttu-id="91dbf-186">Die Zeichenfolge "abcdefghijklmnopqrstuvwxyz" generiert beispielsweise die Zeichenfolge "c3fcd3d76192e4007dfb496cca67e13b".</span><span class="sxs-lookup"><span data-stu-id="91dbf-186">For example, the string "abcdefghijklmnopqrstuvwxyz" generates the string "c3fcd3d76192e4007dfb496cca67e13b".</span></span> <span data-ttu-id="91dbf-187">Weitere Informationen zum Implementieren des MD5-Algorithmus finden Sie unter [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span><span class="sxs-lookup"><span data-stu-id="91dbf-187">For more information about implementing the MD5 algorithm, see [RFC 1321](https://www.ietf.org/rfc/rfc1321.txt).</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-188">**Name**</span><span class="sxs-lookup"><span data-stu-id="91dbf-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dbf-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-191">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung (Name), [**korrigiert**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="91dbf-191">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Name), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-192">Entweder der Name der Datei oder der Name der Datei mit einem Verzeichnis Präfix.</span><span class="sxs-lookup"><span data-stu-id="91dbf-192">Either the name of the file or the name of the file with a directory prefix.</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-193">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="91dbf-193">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dbf-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-196">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="91dbf-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-197">Dies ist ein Bezeichner für dieses Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="91dbf-197">This is an identifier for this software element.</span></span>

<span data-ttu-id="91dbf-198">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-198">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="91dbf-199">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="91dbf-199">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-200">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91dbf-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-201">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-202">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91dbf-202">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-203">Der Softwareelement Zustand eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="91dbf-203">The software element state of a software element.</span></span>

<span data-ttu-id="91dbf-204">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-204">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="91dbf-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="91dbf-205"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-206">Beschreibt die für die erfolgreiche Verteilung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im installierbaren Zustand (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="91dbf-206">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="91dbf-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="91dbf-207"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-208">Beschreibt die für die erfolgreiche Installation erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "ausführbare Datei" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="91dbf-208">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="91dbf-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="91dbf-209"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-210">Beschreibt die für die erfolgreiche Ausführung erforderlichen Details und die Details (Bedingungen und Aktionen), die erforderlich sind, um ein Softwareelement im Zustand "wird ausgeführt" (d. h. im nächsten Zustand) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="91dbf-210">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="91dbf-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="91dbf-211"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-212">Beschreibt die Details, die für die Überwachung und den Betrieb eines Start Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="91dbf-212">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91dbf-213">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="91dbf-213">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-214">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91dbf-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-215">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-216">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="91dbf-216">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-217">Ziel Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="91dbf-217">Target operating system of the software element.</span></span>

<span data-ttu-id="91dbf-218">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-218">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91dbf-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="91dbf-219"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91dbf-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="91dbf-220"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="91dbf-221"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="91dbf-221"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-222">Mac OS</span><span class="sxs-lookup"><span data-stu-id="91dbf-222">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="91dbf-223"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="91dbf-223"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-224">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="91dbf-224">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="91dbf-225"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="91dbf-225"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="91dbf-226"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="91dbf-226"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="91dbf-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="91dbf-227"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="91dbf-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="91dbf-228"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-229">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="91dbf-229">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="91dbf-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="91dbf-230"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-231">HP-UX</span><span class="sxs-lookup"><span data-stu-id="91dbf-231">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="91dbf-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="91dbf-232"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="91dbf-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="91dbf-233"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="91dbf-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="91dbf-234"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="91dbf-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="91dbf-235"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="91dbf-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="91dbf-236"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-237">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="91dbf-237">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="91dbf-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="91dbf-238"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="91dbf-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="91dbf-239"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-240">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="91dbf-240">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="91dbf-241"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="91dbf-241"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-242">Windows 95</span><span class="sxs-lookup"><span data-stu-id="91dbf-242">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="91dbf-243"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="91dbf-243"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-244">Windows 98</span><span class="sxs-lookup"><span data-stu-id="91dbf-244">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="91dbf-245"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="91dbf-245"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-246">Windows NT</span><span class="sxs-lookup"><span data-stu-id="91dbf-246">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="91dbf-247"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="91dbf-247"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-248">Windows CE</span><span class="sxs-lookup"><span data-stu-id="91dbf-248">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="91dbf-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="91dbf-249"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-250">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="91dbf-250">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="91dbf-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="91dbf-251"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="91dbf-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="91dbf-252"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="91dbf-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="91dbf-253"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="91dbf-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="91dbf-254"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="91dbf-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="91dbf-255"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="91dbf-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="91dbf-256"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="91dbf-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="91dbf-257"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="91dbf-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="91dbf-258"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="91dbf-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="91dbf-259"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="91dbf-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="91dbf-260"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="91dbf-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="91dbf-261"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="91dbf-262"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="91dbf-262"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-263">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="91dbf-263">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="91dbf-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="91dbf-264"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-265">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="91dbf-265">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="91dbf-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="91dbf-266"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-267">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="91dbf-267">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="91dbf-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="91dbf-268"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-269">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="91dbf-269">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="91dbf-270"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="91dbf-270"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="91dbf-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="91dbf-271"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="91dbf-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="91dbf-272"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="91dbf-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="91dbf-273"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="91dbf-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="91dbf-274"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="91dbf-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="91dbf-275"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-276">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="91dbf-276">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="91dbf-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="91dbf-277"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="91dbf-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="91dbf-278"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="91dbf-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="91dbf-279"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="91dbf-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="91dbf-280"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-281">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="91dbf-281">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="91dbf-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="91dbf-282"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="91dbf-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="91dbf-283"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="91dbf-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="91dbf-284"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="91dbf-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="91dbf-285"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="91dbf-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="91dbf-286"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="91dbf-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="91dbf-287"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="91dbf-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="91dbf-288"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="91dbf-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="91dbf-289"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="91dbf-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="91dbf-290"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="91dbf-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="91dbf-291"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="91dbf-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="91dbf-292"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="91dbf-293">Palm OS</span><span class="sxs-lookup"><span data-stu-id="91dbf-293">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="91dbf-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="91dbf-294"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="91dbf-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="91dbf-295"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="91dbf-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="91dbf-296"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="91dbf-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="91dbf-297"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="91dbf-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="91dbf-298"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91dbf-299">**Version**</span><span class="sxs-lookup"><span data-stu-id="91dbf-299">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91dbf-300">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="91dbf-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-301">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="91dbf-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91dbf-302">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="91dbf-302">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="91dbf-303">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="91dbf-303">Version of the operation.</span></span>

<span data-ttu-id="91dbf-304">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="91dbf-304">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="91dbf-305"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="91dbf-305"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="91dbf-306"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="91dbf-306"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="91dbf-307">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="91dbf-307">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91dbf-308">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91dbf-308">Remarks</span></span>

<span data-ttu-id="91dbf-309">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="91dbf-309">WMI does not implement this class.</span></span> <span data-ttu-id="91dbf-310">Informationen zu Klassen, die von **CIM \_ File Specification** abgeleitet sind, finden Sie unter [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="91dbf-310">For classes derived from **CIM\_FileSpecification**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="91dbf-311">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="91dbf-311">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="91dbf-312">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="91dbf-312">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="91dbf-313">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91dbf-313">Requirements</span></span>



| <span data-ttu-id="91dbf-314">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91dbf-314">Requirement</span></span> | <span data-ttu-id="91dbf-315">Wert</span><span class="sxs-lookup"><span data-stu-id="91dbf-315">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91dbf-316">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91dbf-316">Minimum supported client</span></span><br/> | <span data-ttu-id="91dbf-317">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91dbf-317">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91dbf-318">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91dbf-318">Minimum supported server</span></span><br/> | <span data-ttu-id="91dbf-319">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91dbf-319">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91dbf-320">Namespace</span><span class="sxs-lookup"><span data-stu-id="91dbf-320">Namespace</span></span><br/>                | <span data-ttu-id="91dbf-321">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="91dbf-321">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91dbf-322">MOF</span><span class="sxs-lookup"><span data-stu-id="91dbf-322">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91dbf-323"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="91dbf-323"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91dbf-324">DLL</span><span class="sxs-lookup"><span data-stu-id="91dbf-324">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91dbf-325"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91dbf-325"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91dbf-326">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91dbf-326">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91dbf-327">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="91dbf-327">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

