---
description: Beschreibt die Funktionen und die Verwaltung eines seriellen Controllers.
ms.assetid: ce3e0424-4ab8-435d-a155-1164535b3b0d
title: CIM_SerialController-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a2e69bab38bb8b68c15ed93b2bee721c35a7600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372858"
---
# <a name="cim_serialcontroller-class-hyper-v-management"></a><span data-ttu-id="b661c-103">CIM_SerialController-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="b661c-103">CIM_SerialController class (Hyper-V management)</span></span>

<span data-ttu-id="b661c-104">Beschreibt die Funktionen und die Verwaltung eines seriellen Controllers.</span><span class="sxs-lookup"><span data-stu-id="b661c-104">Describes the capabilities and management of a serial controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b661c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b661c-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint32 MaxBaudRate;
  uint16 Security;
};
```

## <a name="members"></a><span data-ttu-id="b661c-106">Member</span><span class="sxs-lookup"><span data-stu-id="b661c-106">Members</span></span>

<span data-ttu-id="b661c-107">Die **CIM \_ SerialController** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b661c-107">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="b661c-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b661c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b661c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b661c-109">Properties</span></span>

<span data-ttu-id="b661c-110">Die **CIM \_ SerialController** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b661c-110">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b661c-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="b661c-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b661c-112">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="b661c-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b661c-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b661c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b661c-114">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| serielle Ports \| 004,7 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**".**Capabilitybeschreibungen**")</span><span class="sxs-lookup"><span data-stu-id="b661c-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="b661c-115">Die Kompatibilität der Chip Ebene für den seriellen Controller.</span><span class="sxs-lookup"><span data-stu-id="b661c-115">The chip level compatibility for the serial controller.</span></span> <span data-ttu-id="b661c-116">Diese Eigenschaft beschreibt die Pufferung und andere Funktionen des seriellen Controllers, die möglicherweise in der Chip Hardware enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b661c-116">This property describes the buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b661c-117">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b661c-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b661c-118">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b661c-118">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="b661c-119">**XT/kompatibel** (3)</span><span class="sxs-lookup"><span data-stu-id="b661c-119">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="b661c-120">**16450 kompatibel** (4)</span><span class="sxs-lookup"><span data-stu-id="b661c-120">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="b661c-121">**16550 kompatibel** (5)</span><span class="sxs-lookup"><span data-stu-id="b661c-121">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="b661c-122">**16550kompatibel** (6)</span><span class="sxs-lookup"><span data-stu-id="b661c-122">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="b661c-123">**8251 kompatibel** (160)</span><span class="sxs-lookup"><span data-stu-id="b661c-123">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="b661c-124">**8251FIFO-kompatibel** (161)</span><span class="sxs-lookup"><span data-stu-id="b661c-124">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b661c-125">**Capabilitybeschreibungen**</span><span class="sxs-lookup"><span data-stu-id="b661c-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b661c-126">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="b661c-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b661c-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b661c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b661c-128">Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SerialController**.**Funktionen**")</span><span class="sxs-lookup"><span data-stu-id="b661c-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="b661c-129">Ein Array, das Ausführlichere Erläuterungen zu seriellen Controller Features im Funktions **Array enthält** .</span><span class="sxs-lookup"><span data-stu-id="b661c-129">An array that contains more detailed explanations for serial controller features in the **Capabilities** array.</span></span> <span data-ttu-id="b661c-130">Die Elemente im **capabilitybeschreibungen** -Array korrelieren mit denen im Funktions **Array.**</span><span class="sxs-lookup"><span data-stu-id="b661c-130">The items in the **CapabilityDescriptions** array correlate to those in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="b661c-131">**Maxbaudrate**</span><span class="sxs-lookup"><span data-stu-id="b661c-131">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b661c-132">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b661c-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b661c-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b661c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b661c-134">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| serielle Ports \| 004,6 "), **Punit** (" Bit/Sekunde ")</span><span class="sxs-lookup"><span data-stu-id="b661c-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="b661c-135">Die maximale Baudrate in (Bits pro Sekunde), die vom seriellen Controller unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b661c-135">The maximum baud rate in, bits per second, that is supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="b661c-136">**Security**</span><span class="sxs-lookup"><span data-stu-id="b661c-136">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b661c-137">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b661c-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b661c-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b661c-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b661c-139">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| serielle Ports \| 004,9 ")</span><span class="sxs-lookup"><span data-stu-id="b661c-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="b661c-140">Die Betriebssicherheit für den Controller.</span><span class="sxs-lookup"><span data-stu-id="b661c-140">The operational security for the controller.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b661c-141">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b661c-141">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b661c-142">**Unbekannt** (2)</span><span class="sxs-lookup"><span data-stu-id="b661c-142">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b661c-143">**Keine** (3)</span><span class="sxs-lookup"><span data-stu-id="b661c-143">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Locked_Out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="b661c-144">**Externe Schnittstelle gesperrt** (4)</span><span class="sxs-lookup"><span data-stu-id="b661c-144">**External Interface Locked Out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_Interface_Enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="b661c-145">**Externe Schnittstelle aktiviert** (5)</span><span class="sxs-lookup"><span data-stu-id="b661c-145">**External Interface Enabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="b661c-146">**Start Umgehung** (6)</span><span class="sxs-lookup"><span data-stu-id="b661c-146">**Boot Bypass** (6)</span></span>


<span data-ttu-id="b661c-147"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b661c-147"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b661c-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b661c-148">Requirements</span></span>



| <span data-ttu-id="b661c-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b661c-149">Requirement</span></span> | <span data-ttu-id="b661c-150">Wert</span><span class="sxs-lookup"><span data-stu-id="b661c-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b661c-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b661c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b661c-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b661c-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b661c-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b661c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b661c-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b661c-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b661c-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="b661c-155">Namespace</span></span><br/>                | <span data-ttu-id="b661c-156">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b661c-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b661c-157">MOF</span><span class="sxs-lookup"><span data-stu-id="b661c-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b661c-158"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b661c-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b661c-159">DLL</span><span class="sxs-lookup"><span data-stu-id="b661c-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b661c-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b661c-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b661c-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b661c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b661c-162">**CIM- \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="b661c-162">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

