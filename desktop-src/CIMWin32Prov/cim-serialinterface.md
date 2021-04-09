---
description: Die CIM \_ serialinterface-Klasse stellt eine CIM \_ controlledby-Beziehung dar, die angibt, auf welche Geräte über den seriellen Controller und die Eigenschaften des Zugriffs zugegriffen werden.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: CIM_SerialInterface-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861024"
---
# <a name="cim_serialinterface-class"></a><span data-ttu-id="fd970-103">CIM \_ serialinterface-Klasse</span><span class="sxs-lookup"><span data-stu-id="fd970-103">CIM\_SerialInterface class</span></span>

<span data-ttu-id="fd970-104">Die **CIM \_ serialinterface** -Klasse stellt eine [**CIM \_ controlledby**](cim-controlledby.md) -Beziehung dar, die angibt, auf welche Geräte über den seriellen Controller und die Eigenschaften des Zugriffs zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="fd970-104">The **CIM\_SerialInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd970-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fd970-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fd970-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fd970-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fd970-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd970-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fd970-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fd970-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd970-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd970-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a><span data-ttu-id="fd970-110">Member</span><span class="sxs-lookup"><span data-stu-id="fd970-110">Members</span></span>

<span data-ttu-id="fd970-111">Die **CIM \_ serialinterface** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fd970-111">The **CIM\_SerialInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="fd970-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd970-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd970-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd970-113">Properties</span></span>

<span data-ttu-id="fd970-114">Die **CIM \_ serialinterface** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fd970-114">The **CIM\_SerialInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd970-115">**Accessstate**</span><span class="sxs-lookup"><span data-stu-id="fd970-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-116">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd970-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd970-118">Gibt an, ob der Controller aktiv auf das Gerät zugreift oder darauf zugreift.</span><span class="sxs-lookup"><span data-stu-id="fd970-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="fd970-119">Diese Informationen sind erforderlich, wenn ein logisches Gerät durch mehrere Controller befohlen werden kann oder darauf zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd970-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="fd970-120">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd970-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd970-121">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="fd970-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="fd970-122">**Aktiv** (1)</span><span class="sxs-lookup"><span data-stu-id="fd970-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="fd970-123">**Inaktiv** (2)</span><span class="sxs-lookup"><span data-stu-id="fd970-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd970-124">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="fd970-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-125">Datentyp: **CIM \_ SerialController**</span><span class="sxs-lookup"><span data-stu-id="fd970-125">Data type: **CIM\_SerialController**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd970-127">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="fd970-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fd970-128">Ein [**CIM- \_ SerialController**](cim-serialcontroller.md) , der den seriellen Controller beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fd970-128">A [**CIM\_SerialController**](cim-serialcontroller.md) that describes the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="fd970-129">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="fd970-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-130">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="fd970-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd970-132">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="fd970-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fd970-133">Ein [**CIM \_ LogicalDevice**](cim-logicaldevice.md) , das das logische Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fd970-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="fd970-134">**Flowcontrolinfo**</span><span class="sxs-lookup"><span data-stu-id="fd970-134">**FlowControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-135">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd970-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd970-137">Gibt die Fluss Steuerung für übertragene Daten an.</span><span class="sxs-lookup"><span data-stu-id="fd970-137">Indicates the flow control for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd970-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="fd970-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="fd970-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="fd970-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="fd970-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Keine** (2)</span><span class="sxs-lookup"><span data-stu-id="fd970-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span data-ttu-id="fd970-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XOnXOff** (3)</span><span class="sxs-lookup"><span data-stu-id="fd970-141"><span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XonXoff** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span data-ttu-id="fd970-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span><span class="sxs-lookup"><span data-stu-id="fd970-142"><span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span data-ttu-id="fd970-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**XOnXOff und RTS/CTS** (5)</span><span class="sxs-lookup"><span data-stu-id="fd970-143"><span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Both XonXoff and RTS/CTS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="fd970-144">XOnXOff und RTS/CTS</span><span class="sxs-lookup"><span data-stu-id="fd970-144">XonXoff and RTS/CTS</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fd970-145">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="fd970-145">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-146">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd970-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd970-148">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="fd970-148">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fd970-149">Wenn mehrere Bus-oder Verbindungsdaten breiten möglich sind, definiert diese Eigenschaft die jeweils verwendete Eigenschaft zwischen den Geräten.</span><span class="sxs-lookup"><span data-stu-id="fd970-149">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="fd970-150">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd970-150">Data width is specified in bits.</span></span> <span data-ttu-id="fd970-151">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fd970-151">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="fd970-152">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd970-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd970-153">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="fd970-153">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-154">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fd970-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-155">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd970-156">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde")</span><span class="sxs-lookup"><span data-stu-id="fd970-156">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="fd970-157">Wenn mehrere Bus-oder Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die zwischen den Geräten verwendete.</span><span class="sxs-lookup"><span data-stu-id="fd970-157">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="fd970-158">Die Geschwindigkeit wird in Bits pro Sekunde angegeben.</span><span class="sxs-lookup"><span data-stu-id="fd970-158">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="fd970-159">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen für die Geräteverwaltung nicht verfügbar oder wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fd970-159">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="fd970-160">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fd970-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fd970-161">Diese Eigenschaft wird von CIM-Geräte [**\_ erviceconnetction**](cim-deviceconnection.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd970-161">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd970-162">**Anzahlersätze**</span><span class="sxs-lookup"><span data-stu-id="fd970-162">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-163">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd970-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd970-165">Anzahl von Festplatten, die vom Controller ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fd970-165">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="fd970-166">Bei einer festen zurück setzung wird das Gerät wieder in den Initialisierungs-oder Startzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="fd970-166">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="fd970-167">Alle internen Geräte Zustandsinformationen und Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="fd970-167">All internal device state information and data are lost.</span></span>

<span data-ttu-id="fd970-168">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd970-168">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd970-169">**Anzahlermengen**</span><span class="sxs-lookup"><span data-stu-id="fd970-169">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-170">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd970-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-171">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd970-172">Anzahl der vom Controller ausgestellten Soft-zurück Stellungen.</span><span class="sxs-lookup"><span data-stu-id="fd970-172">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="fd970-173">Eine weiche zurück Setzung löscht den aktuellen Gerätestatus und die Daten nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="fd970-173">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="fd970-174">Die genaue Semantik ist abhängig vom Gerät und den Protokollen und Mechanismen, die für die Kommunikation mit dem Gerät verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd970-174">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="fd970-175">Diese Eigenschaft wird von [**CIM \_ controlledby**](cim-controlledby.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="fd970-175">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd970-176">**"Nummeriofstopbits"**</span><span class="sxs-lookup"><span data-stu-id="fd970-176">**NumberOfStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-177">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd970-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd970-179">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits")</span><span class="sxs-lookup"><span data-stu-id="fd970-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="fd970-180">Anzahl der zu übermittelten Stoppbits.</span><span class="sxs-lookup"><span data-stu-id="fd970-180">Number of stop bits to transmit.</span></span>

</dd> <dt>

<span data-ttu-id="fd970-181">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="fd970-181">**ParityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd970-182">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd970-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd970-183">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fd970-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd970-184">Informationen über die Paritäts Einstellung für übertragene Daten.</span><span class="sxs-lookup"><span data-stu-id="fd970-184">Information about the parity setting for transmitted data.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fd970-185">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="fd970-185">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="fd970-186">**Keine** (1)</span><span class="sxs-lookup"><span data-stu-id="fd970-186">**None** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="fd970-187">**Sogar** (2)</span><span class="sxs-lookup"><span data-stu-id="fd970-187">**Even** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="fd970-188">**Ungerade** (3)</span><span class="sxs-lookup"><span data-stu-id="fd970-188">**Odd** (3)</span></span>


<span data-ttu-id="fd970-189"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fd970-189"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="fd970-190">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd970-190">Remarks</span></span>

<span data-ttu-id="fd970-191">Die **CIM- \_ serialinterface** -Klasse wird von [**CIM \_ controlledby**](cim-controlledby.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fd970-191">The **CIM\_SerialInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="fd970-192">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="fd970-192">WMI does not implement this class.</span></span>

<span data-ttu-id="fd970-193">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="fd970-193">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fd970-194">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fd970-194">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd970-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd970-195">Requirements</span></span>



| <span data-ttu-id="fd970-196">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd970-196">Requirement</span></span> | <span data-ttu-id="fd970-197">Wert</span><span class="sxs-lookup"><span data-stu-id="fd970-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd970-198">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd970-198">Minimum supported client</span></span><br/> | <span data-ttu-id="fd970-199">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd970-199">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd970-200">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd970-200">Minimum supported server</span></span><br/> | <span data-ttu-id="fd970-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd970-201">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd970-202">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd970-202">Namespace</span></span><br/>                | <span data-ttu-id="fd970-203">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fd970-203">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd970-204">MOF</span><span class="sxs-lookup"><span data-stu-id="fd970-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd970-205"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fd970-205"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd970-206">DLL</span><span class="sxs-lookup"><span data-stu-id="fd970-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd970-207"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd970-207"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd970-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd970-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd970-209">**CIM- \_ controlledby**</span><span class="sxs-lookup"><span data-stu-id="fd970-209">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

