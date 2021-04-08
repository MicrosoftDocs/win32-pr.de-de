---
description: Eine abstrakte Klasse, die von einer Ethernet-Switcherweiterung erfasste Port Laufzeitdaten darstellt.
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Msvm_EthernetPortData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36167d4acad3c0da6b96efb9f9cc1fe58bd41a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865536"
---
# <a name="msvm_ethernetportdata-class"></a><span data-ttu-id="341b3-103">MSVM \_ ethernetportdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="341b3-103">Msvm\_EthernetPortData class</span></span>

<span data-ttu-id="341b3-104">Eine abstrakte Klasse, die von einer Ethernet-Switcherweiterung erfasste Port Laufzeitdaten darstellt.</span><span class="sxs-lookup"><span data-stu-id="341b3-104">An abstract class that represents port runtime data collected by an Ethernet switch extension.</span></span> <span data-ttu-id="341b3-105">Alle Ethernet-Port Daten Klassen müssen von dieser abstrakten Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="341b3-105">All Ethernet port data classes must derive from this abstract class.</span></span>

<span data-ttu-id="341b3-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="341b3-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="341b3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="341b3-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="341b3-108">Member</span><span class="sxs-lookup"><span data-stu-id="341b3-108">Members</span></span>

<span data-ttu-id="341b3-109">Die **MSVM-Klasse " \_ ethernetportdata** " enthält diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="341b3-109">The **Msvm\_EthernetPortData** class has these types of members:</span></span>

-   [<span data-ttu-id="341b3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="341b3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="341b3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="341b3-111">Properties</span></span>

<span data-ttu-id="341b3-112">Die **MSVM-Klasse " \_ ethernetportdata** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="341b3-112">The **Msvm\_EthernetPortData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="341b3-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="341b3-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="341b3-116">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="341b3-116">A short description of the object.</span></span> <span data-ttu-id="341b3-117">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="341b3-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="341b3-118">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="341b3-118">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="341b3-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="341b3-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="341b3-122">Der Name der Unterklasse, die bei der Erstellung dieser Port Daten Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="341b3-122">The name of the subclass used in the creation of this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="341b3-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="341b3-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="341b3-126">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="341b3-126">A description of the object.</span></span> <span data-ttu-id="341b3-127">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="341b3-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="341b3-128">**Geräteklassen Name**</span><span class="sxs-lookup"><span data-stu-id="341b3-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="341b3-131">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**"Kreationclassname**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="341b3-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="341b3-132">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="341b3-132">The scoping system's creation class name.</span></span> <span data-ttu-id="341b3-133">Diese Eigenschaft ist immer auf "MSVM \_ ethernetzwitchport" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="341b3-133">This property is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="341b3-134">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="341b3-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="341b3-137">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**De viceid**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="341b3-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="341b3-138">Die Geräte-ID des Ports, der diese Port Daten Instanz eingibt.</span><span class="sxs-lookup"><span data-stu-id="341b3-138">The Device ID of the port that scopes this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="341b3-139">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="341b3-139">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="341b3-142">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="341b3-142">A display name for the object.</span></span> <span data-ttu-id="341b3-143">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="341b3-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="341b3-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="341b3-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="341b3-147">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="341b3-147">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="341b3-148">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="341b3-148">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="341b3-149">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="341b3-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="341b3-150">**Name**</span><span class="sxs-lookup"><span data-stu-id="341b3-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="341b3-153">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="341b3-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="341b3-154">Eine Zeichenfolge, die diese Port Daten Instanz innerhalb des Bereichs des Schalters und des Ports eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="341b3-154">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span>

</dd> <dt>

<span data-ttu-id="341b3-155">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="341b3-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-156">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-157">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="341b3-158">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="341b3-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="341b3-159">Der Name der Erstellungs Klasse des Bereichs Systems.</span><span class="sxs-lookup"><span data-stu-id="341b3-159">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="341b3-160">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="341b3-160">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="341b3-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="341b3-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="341b3-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="341b3-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="341b3-163">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="341b3-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="341b3-164">Der Name des virtuellen Switches, der diese Port Daten Instanz eingibt.</span><span class="sxs-lookup"><span data-stu-id="341b3-164">The name of the virtual switch that scopes this port data instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="341b3-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="341b3-165">Requirements</span></span>



| <span data-ttu-id="341b3-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="341b3-166">Requirement</span></span> | <span data-ttu-id="341b3-167">Wert</span><span class="sxs-lookup"><span data-stu-id="341b3-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="341b3-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="341b3-168">Minimum supported client</span></span><br/> | <span data-ttu-id="341b3-169">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="341b3-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="341b3-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="341b3-170">Minimum supported server</span></span><br/> | <span data-ttu-id="341b3-171">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="341b3-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="341b3-172">Namespace</span><span class="sxs-lookup"><span data-stu-id="341b3-172">Namespace</span></span><br/>                | <span data-ttu-id="341b3-173">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="341b3-173">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="341b3-174">MOF</span><span class="sxs-lookup"><span data-stu-id="341b3-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="341b3-175"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="341b3-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="341b3-176">DLL</span><span class="sxs-lookup"><span data-stu-id="341b3-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="341b3-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="341b3-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

