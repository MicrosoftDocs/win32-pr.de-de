---
description: Die \_ WMI-Klasse Win32 dmachannel stellt einen DMA-Kanal (Direct Memory Access) auf einem Computersystem dar, auf dem Windows ausgeführt wird.
ms.assetid: cc517aac-7bd4-4937-8b07-2597076fca2c
ms.tgt_platform: multiple
title: Win32_DMAChannel-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DMAChannel
- Win32_DMAChannel.AddressSize
- Win32_DMAChannel.Availability
- Win32_DMAChannel.BurstMode
- Win32_DMAChannel.ByteMode
- Win32_DMAChannel.Caption
- Win32_DMAChannel.ChannelTiming
- Win32_DMAChannel.CreationClassName
- Win32_DMAChannel.CSCreationClassName
- Win32_DMAChannel.CSName
- Win32_DMAChannel.Description
- Win32_DMAChannel.DMAChannel
- Win32_DMAChannel.InstallDate
- Win32_DMAChannel.MaxTransferSize
- Win32_DMAChannel.Name
- Win32_DMAChannel.Port
- Win32_DMAChannel.Status
- Win32_DMAChannel.TransferWidths
- Win32_DMAChannel.TypeCTiming
- Win32_DMAChannel.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c2b36ff17931133d0dc4529e34f31ac24e00653
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861507"
---
# <a name="win32_dmachannel-class"></a><span data-ttu-id="9d37c-103">Win32- \_ dmachannel-Klasse</span><span class="sxs-lookup"><span data-stu-id="9d37c-103">Win32\_DMAChannel class</span></span>

<span data-ttu-id="9d37c-104">Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ dmachannel** stellt einen DMA-Kanal (Direct Memory Access) auf einem Computersystem dar, auf dem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d37c-104">The **Win32\_DMAChannel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a direct memory access (DMA) channel on a computer system running Windows.</span></span> <span data-ttu-id="9d37c-105">DMA ist eine Methode zum Verschieben von Daten von einem Gerät in den Arbeitsspeicher (oder umgekehrt), ohne dass der Mikroprozessor unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9d37c-105">DMA is a method of moving data from a device to memory (or vice versa) without the help of the microprocessor.</span></span> <span data-ttu-id="9d37c-106">Das System Board verwendet einen DMA-Controller, um eine festgelegte Anzahl von Kanälen zu verarbeiten, von denen jede jeweils von einem (und nur einem) Gerät gleichzeitig verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9d37c-106">The system board uses a DMA controller to handle a fixed number of channels, each of which can be used by one (and only one) device at a time.</span></span>

<span data-ttu-id="9d37c-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d37c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9d37c-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9d37c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d37c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d37c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DMAChannel : CIM_DMA
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
  uint32   Port;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a><span data-ttu-id="9d37c-110">Member</span><span class="sxs-lookup"><span data-stu-id="9d37c-110">Members</span></span>

<span data-ttu-id="9d37c-111">Die **Win32- \_ dmachannel** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9d37c-111">The **Win32\_DMAChannel** class has these types of members:</span></span>

-   [<span data-ttu-id="9d37c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d37c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d37c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d37c-113">Properties</span></span>

<span data-ttu-id="9d37c-114">Die **Win32- \_ dmachannel** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d37c-114">The **Win32\_DMAChannel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d37c-115">**Addresssize**</span><span class="sxs-lookup"><span data-stu-id="9d37c-115">**AddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d37c-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-118">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,3 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-119">DMA-channeladressgröße in Bits.</span><span class="sxs-lookup"><span data-stu-id="9d37c-119">DMA channel address size in bits.</span></span> <span data-ttu-id="9d37c-120">Zulässige Werte sind 8, 16, 32 oder 64 Bits.</span><span class="sxs-lookup"><span data-stu-id="9d37c-120">Permissible values are 8, 16, 32, or 64 bits.</span></span> <span data-ttu-id="9d37c-121">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="9d37c-121">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="9d37c-122">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-122">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="9d37c-123"> (0)</span><span class="sxs-lookup"><span data-stu-id="9d37c-123">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-124">(8)</span><span class="sxs-lookup"><span data-stu-id="9d37c-124">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-125">(16)</span><span class="sxs-lookup"><span data-stu-id="9d37c-125">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-126">(32)</span><span class="sxs-lookup"><span data-stu-id="9d37c-126">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-127">(64)</span><span class="sxs-lookup"><span data-stu-id="9d37c-127">(64)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9d37c-128">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="9d37c-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d37c-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-131">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| DMA \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-132">Die Verfügbarkeit des DMA.</span><span class="sxs-lookup"><span data-stu-id="9d37c-132">Availability of the DMA.</span></span> <span data-ttu-id="9d37c-133">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-133">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9d37c-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9d37c-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9d37c-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="9d37c-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="9d37c-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Verfügbar** (3)</span><span class="sxs-lookup"><span data-stu-id="9d37c-136"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="9d37c-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Gebrauch/nicht verfügbar** (4)</span><span class="sxs-lookup"><span data-stu-id="9d37c-137"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9d37c-138">In Verwendung oder nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="9d37c-138">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="9d37c-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Verwendung und verfügbar/frei stellbar** (5)</span><span class="sxs-lookup"><span data-stu-id="9d37c-139"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9d37c-140">In Verwendung und verfügbar oder Sharable</span><span class="sxs-lookup"><span data-stu-id="9d37c-140">In Use and Available or Sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9d37c-141">**Burstmode**</span><span class="sxs-lookup"><span data-stu-id="9d37c-141">**BurstMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9d37c-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-144">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| DMA \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-145">Gibt an, ob der DMA-Kanal den Burst Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-145">Indicates whether or not the DMA channel supports burst mode.</span></span>

<span data-ttu-id="9d37c-146">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-146">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-147">**Bytemode**</span><span class="sxs-lookup"><span data-stu-id="9d37c-147">**ByteMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-148">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d37c-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-150">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-151">DMA-Ausführungs Modus.</span><span class="sxs-lookup"><span data-stu-id="9d37c-151">DMA execution mode.</span></span>

<span data-ttu-id="9d37c-152">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-152">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9d37c-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9d37c-153"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9d37c-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="9d37c-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="9d37c-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Nicht im "Anzahl nach Byte"-Modus ausführen** (3)</span><span class="sxs-lookup"><span data-stu-id="9d37c-155"><span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Not execute in 'count by byte' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9d37c-156">Wird nicht im "count by Byte"-Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-156">Does not execute in "count by byte" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span data-ttu-id="9d37c-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Ausführung im Modus "Anzahl nach Byte"** (4)</span><span class="sxs-lookup"><span data-stu-id="9d37c-157"><span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Execute in 'count by byte' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9d37c-158">In "Anzahl nach Byte"-Modus ausführen</span><span class="sxs-lookup"><span data-stu-id="9d37c-158">Execute in "count by byte" mode</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9d37c-159">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9d37c-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d37c-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-162">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9d37c-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-163">Kurze Beschreibung des Objekts eine einzeilige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9d37c-163">Short description of the object a one-line string.</span></span>

<span data-ttu-id="9d37c-164">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-165">**Channelzeitlichen Steuerung**</span><span class="sxs-lookup"><span data-stu-id="9d37c-165">**ChannelTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-166">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d37c-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-168">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-169">DMA-Kanal zeitliche Steuerung.</span><span class="sxs-lookup"><span data-stu-id="9d37c-169">DMA channel timing.</span></span>

<span data-ttu-id="9d37c-170">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-170">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9d37c-171">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9d37c-171">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9d37c-172">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="9d37c-172">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="9d37c-173">**ISA-kompatibel** (3)</span><span class="sxs-lookup"><span data-stu-id="9d37c-173">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span data-ttu-id="9d37c-174">**Typ A** (4)</span><span class="sxs-lookup"><span data-stu-id="9d37c-174">**Type A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span data-ttu-id="9d37c-175">**Typ B** (5)</span><span class="sxs-lookup"><span data-stu-id="9d37c-175">**Type B** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span data-ttu-id="9d37c-176">**Typ F** (6)</span><span class="sxs-lookup"><span data-stu-id="9d37c-176">**Type F** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9d37c-177">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="9d37c-177">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d37c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-180">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9d37c-180">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-181">Der Name der ersten konkreten Klasse, die in der Vererbungs Kette angezeigt werden soll, die bei der Erstellung einer Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d37c-181">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="9d37c-182">Bei Verwendung mit den anderen Schlüsseleigenschaften der-Klasse ermöglicht die-Eigenschaft, dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9d37c-182">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9d37c-183">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-183">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-184">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9d37c-184">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d37c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-186">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-187">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**"Kreationclassname**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9d37c-187">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-188">Name der System Erstellungs Klasse des Bereichs bezogenen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d37c-188">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="9d37c-189">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-189">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-190">**CSName**</span><span class="sxs-lookup"><span data-stu-id="9d37c-190">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-191">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d37c-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-193">Qualifizierer: weiter [**gegeben ("**](/windows/desktop/WmiSdk/standard-qualifiers) [**CIM \_ Computersystem**](cim-computersystem.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9d37c-193">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-194">Name des Bereichs Computer Systems.</span><span class="sxs-lookup"><span data-stu-id="9d37c-194">Name of the scoping computer system.</span></span>

<span data-ttu-id="9d37c-195">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-195">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-196">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d37c-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-197">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d37c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-198">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-199">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="9d37c-199">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-200">Eine Beschreibung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9d37c-200">Description of the object.</span></span>

<span data-ttu-id="9d37c-201">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-202">**DMAChannel**</span><span class="sxs-lookup"><span data-stu-id="9d37c-202">**DMAChannel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-203">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d37c-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-205">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| DMA \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-205">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|DMA\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-206">DMA-Kanalnummer, Teil des Schlüssel Werts des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9d37c-206">DMA channel number, part of the object's key value.</span></span>

<span data-ttu-id="9d37c-207">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-207">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9d37c-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-209">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="9d37c-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-210">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-211">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| ComponentID \| 001,5 "), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) (" Install Date ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-211">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-212">Datum und Uhrzeit der Installation des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9d37c-212">Date and time the object was installed.</span></span> <span data-ttu-id="9d37c-213">Für diese Eigenschaft ist kein Wert erforderlich, um anzugeben, dass das Objekt installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9d37c-213">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9d37c-214">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-214">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-215">**MaxTransferSize**</span><span class="sxs-lookup"><span data-stu-id="9d37c-215">**MaxTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-216">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d37c-216">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-217">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-218">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,4 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bytes ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-219">Maximale Anzahl von Bytes, die von diesem DMA-Kanal übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="9d37c-219">Maximum number of bytes that can be transferred by this DMA channel.</span></span> <span data-ttu-id="9d37c-220">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="9d37c-220">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="9d37c-221">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-221">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-222">**Name**</span><span class="sxs-lookup"><span data-stu-id="9d37c-222">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-223">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d37c-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-224">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-225">Qualifizierer: [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="9d37c-225">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-226">Die Bezeichnung, nach der das-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="9d37c-226">Label by which the object is known.</span></span> <span data-ttu-id="9d37c-227">Bei einer Unterklasse kann die Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9d37c-227">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="9d37c-228">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-229">**Port**</span><span class="sxs-lookup"><span data-stu-id="9d37c-229">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-230">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d37c-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-231">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-232">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Structures \| [**cm \_ partielle \_ Ressourcen \_ Deskriptor**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| DMA- \| Port")</span><span class="sxs-lookup"><span data-stu-id="9d37c-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Dma\|Port")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-233">DMA-Port, der vom Hostbus Adapter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d37c-233">DMA port used by the host bus adapter.</span></span> <span data-ttu-id="9d37c-234">Dies ist für den MCA-Typ "Bus" sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="9d37c-234">This is meaningful for MCA-type buses.</span></span>

<span data-ttu-id="9d37c-235">Beispiel: 12</span><span class="sxs-lookup"><span data-stu-id="9d37c-235">Example: 12</span></span>

</dd> <dt>

<span data-ttu-id="9d37c-236">**Status**</span><span class="sxs-lookup"><span data-stu-id="9d37c-236">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9d37c-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-239">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**Display Name**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="9d37c-239">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-240">Aktueller Status des Objekts.</span><span class="sxs-lookup"><span data-stu-id="9d37c-240">Current status of the object.</span></span> <span data-ttu-id="9d37c-241">Es können verschiedene Betriebs-und nicht betriebliche Statuswerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9d37c-241">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9d37c-242">Betriebsstatus umfassen: "OK", "heruntergestuft" und "pred Fail" (ein Element, z. b. ein Smart-aktiviertes Festplattenlaufwerk, funktioniert möglicherweise ordnungsgemäß, aber in naher Zukunft einen Fehler vorherzusagen).</span><span class="sxs-lookup"><span data-stu-id="9d37c-242">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9d37c-243">Nicht betriebsbereite Status umfassen: "Error", "Starting", "Stop" und "Service".</span><span class="sxs-lookup"><span data-stu-id="9d37c-243">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9d37c-244">Der letztgenannte "Dienst" kann während der Spiegelung eines Datenträgers, dem erneuten Laden einer Benutzer Berechtigungs Liste oder anderer administrativer Aufgaben angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d37c-244">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9d37c-245">Nicht alle diese Arbeiten sind online, aber das verwaltete Element ist weder "OK" noch in einem der anderen Zustände.</span><span class="sxs-lookup"><span data-stu-id="9d37c-245">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9d37c-246">Diese Eigenschaft wird von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-246">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9d37c-247">Folgende Werte sind gültig:</span><span class="sxs-lookup"><span data-stu-id="9d37c-247">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9d37c-248">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9d37c-248">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9d37c-249">**Fehler** ("Fehler")</span><span class="sxs-lookup"><span data-stu-id="9d37c-249">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9d37c-250">Herunter **gestuft ("** heruntergestuft")</span><span class="sxs-lookup"><span data-stu-id="9d37c-250">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9d37c-251">**Unbekannt** ("unbekannt")</span><span class="sxs-lookup"><span data-stu-id="9d37c-251">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9d37c-252">**Pred-** Fehler ("pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9d37c-252">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9d37c-253">Wird **gestartet** ("wird gestartet")</span><span class="sxs-lookup"><span data-stu-id="9d37c-253">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9d37c-254">Wird **beendet ("wird angehalten** ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-254">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9d37c-255">**Dienst** ("Dienst")</span><span class="sxs-lookup"><span data-stu-id="9d37c-255">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9d37c-256">**Betont** ("gestresst")</span><span class="sxs-lookup"><span data-stu-id="9d37c-256">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9d37c-257">**Nicht wiederherstellen** ("nicht wiederherstellen")</span><span class="sxs-lookup"><span data-stu-id="9d37c-257">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9d37c-258">**Kein Kontakt** ("kein Kontakt")</span><span class="sxs-lookup"><span data-stu-id="9d37c-258">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9d37c-259">**Verlorene** Kommunikations ("verlorene Kommunikations-")</span><span class="sxs-lookup"><span data-stu-id="9d37c-259">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9d37c-260">**Übertragungs breiten**</span><span class="sxs-lookup"><span data-stu-id="9d37c-260">**TransferWidths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-261">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="9d37c-261">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-262">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-263">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,2 "), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) (" Bits ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-264">Array aller Übertragungs breiten (in Bits), die von diesem DMA-Kanal unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9d37c-264">Array of all the transfer widths (in bits) supported by this DMA channel.</span></span> <span data-ttu-id="9d37c-265">Wenn unbekannt, geben Sie 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="9d37c-265">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="9d37c-266">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-266">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>



 <span data-ttu-id="9d37c-267"> (0)</span><span class="sxs-lookup"><span data-stu-id="9d37c-267">(0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-268">(8)</span><span class="sxs-lookup"><span data-stu-id="9d37c-268">(8)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-269">(16)</span><span class="sxs-lookup"><span data-stu-id="9d37c-269">(16)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-270">(32)</span><span class="sxs-lookup"><span data-stu-id="9d37c-270">(32)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-271">(64)</span><span class="sxs-lookup"><span data-stu-id="9d37c-271">(64)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9d37c-272">(128)</span><span class="sxs-lookup"><span data-stu-id="9d37c-272">(128)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9d37c-273">**Typectiming**</span><span class="sxs-lookup"><span data-stu-id="9d37c-273">**TypeCTiming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-274">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d37c-274">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-275">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-276">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-277">Unterstützung für die C-Typen Zeit (Burst).</span><span class="sxs-lookup"><span data-stu-id="9d37c-277">Support for C type (burst) timing.</span></span>

<span data-ttu-id="9d37c-278">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-278">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9d37c-279">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9d37c-279">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9d37c-280">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="9d37c-280">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span data-ttu-id="9d37c-281">**ISA-kompatibel** (3)</span><span class="sxs-lookup"><span data-stu-id="9d37c-281">**ISA Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9d37c-282">**Nicht unterstützt** (4)</span><span class="sxs-lookup"><span data-stu-id="9d37c-282">**Not Supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="9d37c-283">**Unterstützt** (5)</span><span class="sxs-lookup"><span data-stu-id="9d37c-283">**Supported** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9d37c-284">**Wordmode**</span><span class="sxs-lookup"><span data-stu-id="9d37c-284">**WordMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d37c-285">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d37c-285">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-286">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d37c-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d37c-287">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Ressource DMA Info \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="9d37c-287">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource DMA Info\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="9d37c-288">DMA-Ausführungs Modus.</span><span class="sxs-lookup"><span data-stu-id="9d37c-288">DMA execution mode.</span></span>

<span data-ttu-id="9d37c-289">Diese Eigenschaft wird von [**CIM \_ DMA**](cim-dma.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-289">This property is inherited from [**CIM\_DMA**](cim-dma.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9d37c-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9d37c-290"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9d37c-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="9d37c-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="9d37c-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Nicht im ' Anzahl nach Wort '-Modus ausführen** (3)</span><span class="sxs-lookup"><span data-stu-id="9d37c-292"><span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Not execute in 'count by word' mode** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9d37c-293">Wird nicht im "count by Word"-Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d37c-293">Does not execute in "count by word" mode</span></span>

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span data-ttu-id="9d37c-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Ausführung im "count by Word"-Modus** (4)</span><span class="sxs-lookup"><span data-stu-id="9d37c-294"><span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Execute in 'count by word' mode** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9d37c-295">Im "count by Word"-Modus ausführen</span><span class="sxs-lookup"><span data-stu-id="9d37c-295">Execute in "count by word" mode</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d37c-296">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d37c-296">Remarks</span></span>

<span data-ttu-id="9d37c-297">Die **Win32- \_ dmachannel** -Klasse wird von [**CIM \_ DMA**](cim-dma.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="9d37c-297">The **Win32\_DMAChannel** class is derived from [**CIM\_DMA**](cim-dma.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d37c-298">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d37c-298">Requirements</span></span>



| <span data-ttu-id="9d37c-299">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d37c-299">Requirement</span></span> | <span data-ttu-id="9d37c-300">Wert</span><span class="sxs-lookup"><span data-stu-id="9d37c-300">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d37c-301">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d37c-301">Minimum supported client</span></span><br/> | <span data-ttu-id="9d37c-302">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d37c-302">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d37c-303">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d37c-303">Minimum supported server</span></span><br/> | <span data-ttu-id="9d37c-304">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d37c-304">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d37c-305">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d37c-305">Namespace</span></span><br/>                | <span data-ttu-id="9d37c-306">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9d37c-306">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9d37c-307">MOF</span><span class="sxs-lookup"><span data-stu-id="9d37c-307">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d37c-308"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9d37c-308"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d37c-309">DLL</span><span class="sxs-lookup"><span data-stu-id="9d37c-309">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d37c-310"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d37c-310"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d37c-311">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d37c-311">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d37c-312">**CIM \_ DMA**</span><span class="sxs-lookup"><span data-stu-id="9d37c-312">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dt>

[<span data-ttu-id="9d37c-313">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="9d37c-313">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

