---
description: Die CIM- \_ DMA-Klasse stellt die Computerarchitektur für den direkten Speicherzugriff (DMA) dar.
ms.assetid: 101fa9f3-a403-487d-8482-b1e8e9f957d6
ms.tgt_platform: multiple
title: CIM_DMA-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DMA
- CIM_DMA.AddressSize
- CIM_DMA.Availability
- CIM_DMA.BurstMode
- CIM_DMA.ByteMode
- CIM_DMA.Caption
- CIM_DMA.ChannelTiming
- CIM_DMA.CreationClassName
- CIM_DMA.CSCreationClassName
- CIM_DMA.CSName
- CIM_DMA.Description
- CIM_DMA.DMAChannel
- CIM_DMA.InstallDate
- CIM_DMA.MaxTransferSize
- CIM_DMA.Name
- CIM_DMA.Status
- CIM_DMA.TransferWidths
- CIM_DMA.TypeCTiming
- CIM_DMA.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71fe9c0ad29afa7be20df6fbf05c5d1183d23d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958414"
---
# <a name="cim_dma-class"></a><span data-ttu-id="74474-103">CIM- \_ DMA-Klasse</span><span class="sxs-lookup"><span data-stu-id="74474-103">CIM\_DMA class</span></span>

<span data-ttu-id="74474-104">Die **CIM- \_ DMA** -Klasse stellt die Computerarchitektur für den direkten Speicherzugriff (DMA) dar.</span><span class="sxs-lookup"><span data-stu-id="74474-104">The **CIM\_DMA** class represents computer architecture direct memory access (DMA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74474-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="74474-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="74474-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="74474-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="74474-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="74474-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="74474-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="74474-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="74474-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="74474-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C523-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DMA : CIM_SystemResource
{
  uint16   AddressSize;
  uint16   Availability;
  boolean  BurstMode;
  uint16   ByteMode;
  string   Caption;
  uint16   ChannelTiming;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint32   DMAChannel;
  datetime InstallDate;
  uint32   MaxTransferSize;
  string   Name;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="74474-110">Member</span><span class="sxs-lookup"><span data-stu-id="74474-110">Members</span></span>

<span data-ttu-id="74474-111">Die **CIM- \_ DMA** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="74474-111">The **CIM\_DMA** class has these types of members:</span></span>

-   [<span data-ttu-id="74474-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74474-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74474-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="74474-113">Properties</span></span>

<span data-ttu-id="74474-114">Die **CIM- \_ DMA** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="74474-114">The **CIM\_DMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74474-115">**Addresssize**</span><span class="sxs-lookup"><span data-stu-id="74474-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74474-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74474-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-118">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="74474-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="74474-119">DMA-channeladressgröße in Bits.</span><span class="sxs-lookup"><span data-stu-id="74474-119">DMA channel address size, in bits.</span></span> <span data-ttu-id="74474-120">Zulässige Werte sind 8, 16, 32 und 64.</span><span class="sxs-lookup"><span data-stu-id="74474-120">Permissible values are 8, 16, 32, and 64.</span></span> <span data-ttu-id="74474-121">Wenn unbekannt, geben Sie 0 ein.</span><span class="sxs-lookup"><span data-stu-id="74474-121">If unknown, enter 0.</span></span>

<dt>



 <span data-ttu-id="74474-122"> (0)</span><span class="sxs-lookup"><span data-stu-id="74474-122">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-123">(8)</span><span class="sxs-lookup"><span data-stu-id="74474-123">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-124">(16)</span><span class="sxs-lookup"><span data-stu-id="74474-124">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-125">(32)</span><span class="sxs-lookup"><span data-stu-id="74474-125">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-126">(64)</span><span class="sxs-lookup"><span data-stu-id="74474-126">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74474-127">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="74474-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74474-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74474-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-130">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="74474-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="74474-131">Die Verfügbarkeit des DMA.</span><span class="sxs-lookup"><span data-stu-id="74474-131">Availability of the DMA.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74474-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74474-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74474-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74474-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74474-134">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="74474-134">Unknown.</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="74474-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Verfügbar** (3)</span><span class="sxs-lookup"><span data-stu-id="74474-135"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74474-136">Verfügbar.</span><span class="sxs-lookup"><span data-stu-id="74474-136">Available.</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="74474-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Gebrauch/nicht verfügbar** (4)</span><span class="sxs-lookup"><span data-stu-id="74474-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74474-138">Wird verwendet (nicht verfügbar).</span><span class="sxs-lookup"><span data-stu-id="74474-138">In use (not available).</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="74474-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Verwendung und verfügbar/frei stellbar** (5)</span><span class="sxs-lookup"><span data-stu-id="74474-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74474-140">Wird verwendet, ist jedoch verfügbar (Sharable).</span><span class="sxs-lookup"><span data-stu-id="74474-140">In use, but available (sharable).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74474-141">**Burstmode**</span><span class="sxs-lookup"><span data-stu-id="74474-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="74474-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="74474-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="74474-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="74474-145">**True** gibt an, dass der DMA-Kanal den Burst Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74474-145">If **TRUE**, the DMA channel supports burst mode.</span></span>

</dd> <dt>

<span data-ttu-id="74474-146">**Bytemode**</span><span class="sxs-lookup"><span data-stu-id="74474-146">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-147">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74474-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74474-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-149">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="74474-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="74474-150">Gibt an, ob DMA im Count-by-Byte-Modus ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="74474-150">Indicates whether DMA can execute in count-by-byte mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74474-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74474-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74474-152">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="74474-152">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74474-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74474-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74474-154">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="74474-154">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="74474-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Nicht im "Anzahl nach Byte"-Modus ausführen** (3)</span><span class="sxs-lookup"><span data-stu-id="74474-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74474-156">Kann nicht im Count-by-Byte-Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="74474-156">Cannot execute in count-by-byte mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="74474-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Ausführung im Modus "Anzahl nach Byte"** (4)</span><span class="sxs-lookup"><span data-stu-id="74474-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74474-158">Die Ausführung im Count-by-Byte-Modus ist möglich.</span><span class="sxs-lookup"><span data-stu-id="74474-158">Able to execute in count-by-byte mode.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74474-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="74474-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74474-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74474-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-162">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="74474-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="74474-163">Kurze Textbeschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="74474-163">Short textual description of the object.</span></span>

<span data-ttu-id="74474-164">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74474-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74474-165">**Channelzeitlichen Steuerung**</span><span class="sxs-lookup"><span data-stu-id="74474-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-166">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74474-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74474-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-168">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="74474-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="74474-169">DMA-Kanal zeitliche Steuerung.</span><span class="sxs-lookup"><span data-stu-id="74474-169">DMA channel timing.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74474-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74474-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74474-171">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="74474-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74474-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74474-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74474-173">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="74474-173">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="74474-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA-kompatibel** (3)</span><span class="sxs-lookup"><span data-stu-id="74474-174"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74474-175">ISA-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="74474-175">ISA-compatible.</span></span>

</dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="74474-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Typ A** (4)</span><span class="sxs-lookup"><span data-stu-id="74474-176"><span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Type A** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74474-177">Geben Sie ein ein.</span><span class="sxs-lookup"><span data-stu-id="74474-177">Type A.</span></span>

</dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="74474-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Typ B** (5)</span><span class="sxs-lookup"><span data-stu-id="74474-178"><span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Type B** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74474-179">Geben Sie B ein.</span><span class="sxs-lookup"><span data-stu-id="74474-179">Type B.</span></span>

</dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="74474-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Typ F** (6)</span><span class="sxs-lookup"><span data-stu-id="74474-180"><span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Type F** (6)</span></span>


</dt> <dd>

<span data-ttu-id="74474-181">Geben Sie F ein.</span><span class="sxs-lookup"><span data-stu-id="74474-181">Type F.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74474-182">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="74474-182">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74474-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74474-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-185">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74474-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74474-186">Der Name der Klasse oder Unterklasse, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74474-186">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="74474-187">Wenn diese Eigenschaft mit anderen Schlüsseleigenschaften der-Klasse verwendet wird, können alle Instanzen der-Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="74474-187">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="74474-188">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="74474-188">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-189">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74474-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74474-190">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-191">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74474-191">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74474-192">Der Name der Erstellungs Klasse des Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="74474-192">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="74474-193">**CSName**</span><span class="sxs-lookup"><span data-stu-id="74474-193">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-194">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74474-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74474-195">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-196">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="74474-196">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="74474-197">Der Name des Computer Systems wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74474-197">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="74474-198">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="74474-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-199">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74474-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74474-200">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-201">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="74474-201">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="74474-202">Die Textbeschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="74474-202">Textual description of the object.</span></span>

<span data-ttu-id="74474-203">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74474-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74474-204">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="74474-204">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-205">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74474-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74474-206">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-207">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="74474-207">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="74474-208">DMA-Kanalnummer.</span><span class="sxs-lookup"><span data-stu-id="74474-208">DMA channel number.</span></span> <span data-ttu-id="74474-209">Diese Zahl ist Teil des Schlüssel Werts des Objekts.</span><span class="sxs-lookup"><span data-stu-id="74474-209">This number is part of the object's key value.</span></span>

</dd> <dt>

<span data-ttu-id="74474-210">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="74474-210">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-211">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="74474-211">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="74474-212">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-213">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="74474-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="74474-214">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="74474-214">Date and time the object was installed.</span></span> <span data-ttu-id="74474-215">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="74474-215">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="74474-216">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74474-216">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74474-217">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="74474-217">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-218">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74474-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74474-219">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-220">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="74474-220">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="74474-221">Maximale Anzahl von Bytes, die von diesem DMA-Kanal übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="74474-221">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="74474-222">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="74474-222">If unknown, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="74474-223">**Name**</span><span class="sxs-lookup"><span data-stu-id="74474-223">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-224">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74474-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74474-225">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-226">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="74474-226">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="74474-227">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="74474-227">Label by which the object is known.</span></span> <span data-ttu-id="74474-228">Bei einer Unterklasse kann diese Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="74474-228">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="74474-229">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74474-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="74474-230">**Status**</span><span class="sxs-lookup"><span data-stu-id="74474-230">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-231">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="74474-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74474-232">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-233">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="74474-233">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="74474-234">Gibt den aktuellen Status des Objekts an.</span><span class="sxs-lookup"><span data-stu-id="74474-234">Indicates the current status of the object.</span></span>

<span data-ttu-id="74474-235">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="74474-235">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="74474-236">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="74474-236">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="74474-237">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="74474-237">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="74474-238">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="74474-238">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="74474-239">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="74474-239">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74474-240">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="74474-240">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="74474-241">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="74474-241">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="74474-242">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="74474-242">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="74474-243">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="74474-243">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="74474-244">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="74474-244">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="74474-245">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="74474-245">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="74474-246">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="74474-246">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="74474-247">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="74474-247">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="74474-248">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="74474-248">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74474-249">**Übertragungs breiten**</span><span class="sxs-lookup"><span data-stu-id="74474-249">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-250">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="74474-250">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74474-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-252">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="74474-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="74474-253">Ein Array, das alle Übertragungs breiten in Bits angibt, die von diesem DMA-Kanal unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="74474-253">Array that indicates all of the transfer widths, in bits, supported by this DMA channel.</span></span> <span data-ttu-id="74474-254">Zulässige Werte sind 8, 16, 32, 64 und 128 Bits.</span><span class="sxs-lookup"><span data-stu-id="74474-254">Permissible values are 8, 16, 32, 64, and 128 bits.</span></span> <span data-ttu-id="74474-255">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="74474-255">If unknown, enter 0 (zero).</span></span>

<dt>



 <span data-ttu-id="74474-256"> (0)</span><span class="sxs-lookup"><span data-stu-id="74474-256">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-257">(8)</span><span class="sxs-lookup"><span data-stu-id="74474-257">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-258">(16)</span><span class="sxs-lookup"><span data-stu-id="74474-258">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-259">(32)</span><span class="sxs-lookup"><span data-stu-id="74474-259">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-260">(64)</span><span class="sxs-lookup"><span data-stu-id="74474-260">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="74474-261">(128)</span><span class="sxs-lookup"><span data-stu-id="74474-261">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74474-262">**Typectiming**</span><span class="sxs-lookup"><span data-stu-id="74474-262">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-263">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74474-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74474-264">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-265">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="74474-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="74474-266">Gibt an, ob die zeitliche Steuerung von Typ C (Burst) unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="74474-266">Indicates whether Type C (burst) timing is supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74474-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74474-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74474-268">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="74474-268">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74474-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74474-269"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74474-270">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="74474-270">Unknown.</span></span>

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="74474-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA-kompatibel** (3)</span><span class="sxs-lookup"><span data-stu-id="74474-271"><span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**ISA Compatible** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74474-272">ISA-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="74474-272">ISA-compatible.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="74474-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (4)</span><span class="sxs-lookup"><span data-stu-id="74474-273"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74474-274">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74474-274">Not supported.</span></span>

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="74474-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Unterstützt** (5)</span><span class="sxs-lookup"><span data-stu-id="74474-275"><span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Supported** (5)</span></span>


</dt> <dd>

<span data-ttu-id="74474-276">Unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74474-276">Supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="74474-277">**Wordmode**</span><span class="sxs-lookup"><span data-stu-id="74474-277">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74474-278">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74474-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74474-279">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="74474-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74474-280">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="74474-280">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="74474-281">Gibt an, ob DMA im Count-by-Word-Modus ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="74474-281">Indicates whether DMA can execute in count-by-word mode.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="74474-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="74474-282"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="74474-283">Sonstiges</span><span class="sxs-lookup"><span data-stu-id="74474-283">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74474-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="74474-284"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="74474-285">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="74474-285">Unknown.</span></span>

</dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="74474-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Nicht im ' Anzahl nach Wort '-Modus ausführen** (3)</span><span class="sxs-lookup"><span data-stu-id="74474-286"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="74474-287">Die Ausführung im Count-by-Word-Modus ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="74474-287">Cannot execute in count-by-word mode.</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="74474-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Ausführung im "count by Word"-Modus** (4)</span><span class="sxs-lookup"><span data-stu-id="74474-288"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="74474-289">Kann im Count-by-Word-Modus ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="74474-289">Able to execute in count-by-word mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74474-290">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74474-290">Remarks</span></span>

<span data-ttu-id="74474-291">Die **CIM- \_ DMA** -Klasse wird von [**CIM \_ Systemresource**](cim-systemresource.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="74474-291">The **CIM\_DMA** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="74474-292">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="74474-292">WMI does not implement this class.</span></span> <span data-ttu-id="74474-293">Informationen zu von **CIM \_ DMA** abgeleiteten Klassen finden Sie unter [Win32-Klassen](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="74474-293">For classes derived from **CIM\_DMA**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="74474-294">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="74474-294">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="74474-295">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="74474-295">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="74474-296">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74474-296">Requirements</span></span>



| <span data-ttu-id="74474-297">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74474-297">Requirement</span></span> | <span data-ttu-id="74474-298">Wert</span><span class="sxs-lookup"><span data-stu-id="74474-298">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74474-299">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74474-299">Minimum supported client</span></span><br/> | <span data-ttu-id="74474-300">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74474-300">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74474-301">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74474-301">Minimum supported server</span></span><br/> | <span data-ttu-id="74474-302">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74474-302">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74474-303">Namespace</span><span class="sxs-lookup"><span data-stu-id="74474-303">Namespace</span></span><br/>                | <span data-ttu-id="74474-304">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74474-304">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74474-305">MOF</span><span class="sxs-lookup"><span data-stu-id="74474-305">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74474-306"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="74474-306"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74474-307">DLL</span><span class="sxs-lookup"><span data-stu-id="74474-307">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74474-308"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74474-308"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74474-309">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74474-309">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74474-310">**CIM- \_ Systemresource**</span><span class="sxs-lookup"><span data-stu-id="74474-310">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

