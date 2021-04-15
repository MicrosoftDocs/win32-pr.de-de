---
description: Stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: CIM_Memory-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529504"
---
# <a name="cim_memory-class-hyper-v-management"></a><span data-ttu-id="6e97b-103">CIM_Memory-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="6e97b-103">CIM_Memory class (Hyper-V management)</span></span>

<span data-ttu-id="6e97b-104">Stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.</span><span class="sxs-lookup"><span data-stu-id="6e97b-104">Represents the capabilities and management of memory-related logical devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e97b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e97b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="6e97b-106">Member</span><span class="sxs-lookup"><span data-stu-id="6e97b-106">Members</span></span>

<span data-ttu-id="6e97b-107">Die **CIM- \_ Speicher** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6e97b-107">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="6e97b-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e97b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6e97b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6e97b-109">Properties</span></span>

<span data-ttu-id="6e97b-110">Die **CIM- \_ Speicher** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6e97b-110">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6e97b-111">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="6e97b-111">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-112">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="6e97b-112">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-114">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **octetstring**, [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 005,18 "," MIF. Physisches DMTF- \| Speicher Array \| 001,13 ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-114">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.AdditionalErrorData"), **OctetString**, [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.18", "MIF.DMTF\|Physical Memory Array\|001.13")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-115">Ein Array von Oktetten, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="6e97b-115">An array of octets that contains additional error information.</span></span> <span data-ttu-id="6e97b-116">Ein Beispiel hierfür ist ECC-Syndrom oder die Rückgabe der Kontroll Bits, wenn eine CRC-basierte Fehler Methodik verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e97b-116">An example is ECC syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="6e97b-117">Wenn in letzterem Fall ein Single-Bit-Fehler erkannt wird und der CRC-Algorithmus bekannt ist, können Sie das genaue Bit ermitteln, bei dem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6e97b-117">In the latter case, if a single bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span>

<span data-ttu-id="6e97b-118">Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-118">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-119">**Korrektur Fehler**</span><span class="sxs-lookup"><span data-stu-id="6e97b-119">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6e97b-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-122">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. correctableerror"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.CorrectableError"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-123">**true** , wenn der letzte Fehler korrigiert werden kann. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="6e97b-123">**true** if the most recent error is correctable; otherwise, **false**.</span></span> <span data-ttu-id="6e97b-124">Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-124">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-125">**"Endadresse"**</span><span class="sxs-lookup"><span data-stu-id="6e97b-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-126">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e97b-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-128">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,4 "," MIF "zugeordnet. DMTF- \| Speichergerät, zugeordnete Adressen \| 001,5 "), **Punit** (" Byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-128">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-129">Die Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für das Speicher Objekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="6e97b-129">The ending address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="6e97b-130">Die Endadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="6e97b-130">The ending address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-131">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="6e97b-131">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-132">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e97b-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-134">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-134">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorAccess"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-135">Der Speicherzugriffs Vorgang, der den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="6e97b-135">The memory access operation that caused the last error.</span></span> <span data-ttu-id="6e97b-136">Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-136">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6e97b-137">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6e97b-137">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e97b-138">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6e97b-138">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="6e97b-139">**Lesen** (3)</span><span class="sxs-lookup"><span data-stu-id="6e97b-139">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="6e97b-140">**Schreiben** (4)</span><span class="sxs-lookup"><span data-stu-id="6e97b-140">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="6e97b-141">**Partieller Schreibvorgang** (5)</span><span class="sxs-lookup"><span data-stu-id="6e97b-141">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e97b-142">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="6e97b-142">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-143">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e97b-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-145">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. StartingAddress"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 005,19 "," MIF. Physisches DMTF- \| Speicher Array \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-145">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.StartingAddress"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.19", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-146">Die Adresse des letzten Speicher Fehlers.</span><span class="sxs-lookup"><span data-stu-id="6e97b-146">The address of the last memory error.</span></span> <span data-ttu-id="6e97b-147">Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6e97b-147">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="6e97b-148">Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-148">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-149">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="6e97b-149">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-150">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="6e97b-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-152">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorData"), **octetstring**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,12 ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-152">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorData"), **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.12")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-153">Ein Array, das Daten enthält, die während des letzten fehlerhaften Speicherzugriffs aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="6e97b-153">An array that contains data captured during the last erroneous memory access.</span></span> <span data-ttu-id="6e97b-154">Die Daten belegen die ersten n Oktette des Arrays, die die Anzahl der Bits enthalten muss, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e97b-154">The data occupies the first n octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span>

<span data-ttu-id="6e97b-155">Wenn die **ErrorTransferSize** -Eigenschaft den Wert "0" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-155">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-156">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="6e97b-156">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-157">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e97b-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-159">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")</span><span class="sxs-lookup"><span data-stu-id="6e97b-159">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorDataOrder")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-160">Die Reihenfolge der in der **ErrorData** -Eigenschaft gespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="6e97b-160">The ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="6e97b-161">Es kann "least signifikanter Byte First" (Value = 1) oder "Most signifikanter Byte First" (2) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e97b-161">"Least Significant Byte First" (value=1) or "Most Significant Byte First" (2) can be specified.</span></span> <span data-ttu-id="6e97b-162">Wenn die **ErrorTransferSize** -Eigenschaft den Wert "0" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-162">If the **ErrorTransferSize** property contains "0" (OK), this property is not used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e97b-163">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="6e97b-163">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="6e97b-164">**Am wenigsten signifikantes Byte zuerst** (1)</span><span class="sxs-lookup"><span data-stu-id="6e97b-164">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="6e97b-165">**Signifikanteste Byte First** (2)</span><span class="sxs-lookup"><span data-stu-id="6e97b-165">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e97b-166">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6e97b-166">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-167">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6e97b-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-169">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorInfo"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 005,12 "," MIF. DMTF \| physikalisches Speicher Array \| 001,8 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM-Arbeits **\_ Speicher**".**Othererrordescription**")</span><span class="sxs-lookup"><span data-stu-id="6e97b-169">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorInfo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-170">Der Typ des letzten Fehlers, der auftreten soll.</span><span class="sxs-lookup"><span data-stu-id="6e97b-170">The type of the last error to occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6e97b-171">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="6e97b-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6e97b-172">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="6e97b-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6e97b-173">**OK** (3)</span><span class="sxs-lookup"><span data-stu-id="6e97b-173">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="6e97b-174">Ungültiger **Lese** Vorgang (4)</span><span class="sxs-lookup"><span data-stu-id="6e97b-174">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="6e97b-175">**Paritätsfehler** (5)</span><span class="sxs-lookup"><span data-stu-id="6e97b-175">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="6e97b-176">**Einzelbit-Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="6e97b-176">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="6e97b-177">**Doppelbit-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="6e97b-177">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="6e97b-178">**Multi-Bit-Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="6e97b-178">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="6e97b-179">**Nibble-Fehler** (9)</span><span class="sxs-lookup"><span data-stu-id="6e97b-179">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="6e97b-180">**Prüfsummen Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="6e97b-180">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="6e97b-181">**CRC-Fehler** (11)</span><span class="sxs-lookup"><span data-stu-id="6e97b-181">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6e97b-182">Nicht **definiert** (12)</span><span class="sxs-lookup"><span data-stu-id="6e97b-182">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6e97b-183">Nicht **definiert** (13)</span><span class="sxs-lookup"><span data-stu-id="6e97b-183">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="6e97b-184">Nicht **definiert** (14)</span><span class="sxs-lookup"><span data-stu-id="6e97b-184">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6e97b-185">**Errormethodmethodologie**</span><span class="sxs-lookup"><span data-stu-id="6e97b-185">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-186">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e97b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-187">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-188">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("errormethod"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-188">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-189">Gibt an, ob Paritäts Algorithmen, CRC-Algorithmen, ECC oder andere Mechanismen vom Speicher Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e97b-189">Indicates whether parity algorithms, CRC algorithms, ECC, or other mechanisms are used by the memory object.</span></span> <span data-ttu-id="6e97b-190">Details zum Algorithmus können auch bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e97b-190">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-191">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="6e97b-191">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-192">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e97b-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-193">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-194">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 005,21 "," MIF. DMTF \| physikalisches Speicher Array \| 001,15 "), **Punit** (" Byte ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-194">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|005.21", "MIF.DMTF\|Physical Memory Array\|001.15"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-195">Der Bereich in Bytes, in dem der letzte Fehler aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="6e97b-195">The range, in bytes, in which the last error can be resolved.</span></span> <span data-ttu-id="6e97b-196">Wenn z. b. Fehler Adressen in Bit 11 aufgelöst werden, z. b. auf einer typischen Seite, Anschließend können die Fehler in 4K-Begrenzungen aufgelöst werden, und diese Eigenschaft wird auf "4000" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6e97b-196">For example, if error addresses are resolved to bit 11, such as on a typical page basis; then the errors can be resolved to 4K boundaries, and this property is set to "4000".</span></span> <span data-ttu-id="6e97b-197">Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-197">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-198">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="6e97b-198">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-199">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="6e97b-199">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-201">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. errortime")</span><span class="sxs-lookup"><span data-stu-id="6e97b-201">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTime")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-202">Der Zeitpunkt, zu dem der letzte Speicherfehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="6e97b-202">The time when the last memory error occurred.</span></span> <span data-ttu-id="6e97b-203">Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-203">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-204">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="6e97b-204">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-205">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6e97b-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-207">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| physikalisches Speicher Array \| 001,11 "), **Punit** (" Bit ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-207">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.ErrorTransferSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.11"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-208">Die Größe der Datenübertragung in Bits, die den letzten Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="6e97b-208">The size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="6e97b-209">"0" gibt keinen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="6e97b-209">"0" indicates no error.</span></span> <span data-ttu-id="6e97b-210">Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e97b-210">If the **ErrorInfo** property contains "3" (OK), this property is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-211">**Othererrordescription**</span><span class="sxs-lookup"><span data-stu-id="6e97b-211">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-212">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6e97b-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-213">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-214">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. othererrordescription"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Speicher**.**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="6e97b-214">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.OtherErrorDescription"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-215">Eine Beschreibung des Fehler Typs, wenn die **ErrorType** -Eigenschaft auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6e97b-215">A description of the error type, when the **ErrorType** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-216">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="6e97b-216">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-217">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6e97b-217">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-218">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-219">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,3 "," MIF "zugeordnet. DMTF- \| Speichergerät, zugeordnete Adressen \| 001,4 "), **Punit** (" Byte \* 10 ^ 3 ")</span><span class="sxs-lookup"><span data-stu-id="6e97b-219">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), **PUnit** ("byte \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-220">Die Startadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für das Speicher Objekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="6e97b-220">The starting address that is referenced by an application or operating system, and mapped by a memory controller for the memory object.</span></span> <span data-ttu-id="6e97b-221">Die Startadresse wird in Kilobyte angegeben.</span><span class="sxs-lookup"><span data-stu-id="6e97b-221">The starting address is specified in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-222">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="6e97b-222">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-223">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6e97b-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-225">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.Systemleveladdress")</span><span class="sxs-lookup"><span data-stu-id="6e97b-225">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_MemoryError.SystemLevelAddress")</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-226">**true** , wenn die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene sind, **false** , wenn es sich um eine physische Adresse handelt.</span><span class="sxs-lookup"><span data-stu-id="6e97b-226">**true** if the address information in the **ErrorAddress** property is a system-level address, **false** if it is a physical address.</span></span>

</dd> <dt>

<span data-ttu-id="6e97b-227">**Ständigem**</span><span class="sxs-lookup"><span data-stu-id="6e97b-227">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e97b-228">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6e97b-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6e97b-229">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6e97b-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6e97b-230">**true** , wenn der Arbeitsspeicher flüchtig ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="6e97b-230">**true** if the memory is volatile; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e97b-231">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e97b-231">Requirements</span></span>



| <span data-ttu-id="6e97b-232">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e97b-232">Requirement</span></span> | <span data-ttu-id="6e97b-233">Wert</span><span class="sxs-lookup"><span data-stu-id="6e97b-233">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e97b-234">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e97b-234">Minimum supported client</span></span><br/> | <span data-ttu-id="6e97b-235">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e97b-235">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6e97b-236">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e97b-236">Minimum supported server</span></span><br/> | <span data-ttu-id="6e97b-237">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e97b-237">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6e97b-238">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e97b-238">Namespace</span></span><br/>                | <span data-ttu-id="6e97b-239">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6e97b-239">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6e97b-240">MOF</span><span class="sxs-lookup"><span data-stu-id="6e97b-240">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e97b-241"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6e97b-241"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e97b-242">DLL</span><span class="sxs-lookup"><span data-stu-id="6e97b-242">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e97b-243"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e97b-243"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e97b-244">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e97b-244">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e97b-245">**CIM- \_ storageblock**</span><span class="sxs-lookup"><span data-stu-id="6e97b-245">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

