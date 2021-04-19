---
description: Eine abstrakte Klasse, die eine Ressource für eine bestimmte Instanz eines Ethernet-Schalters darstellt.
ms.assetid: 5ae1be2a-8d59-4efe-a4ae-7cac1727cfa2
title: Msvm_EthernetSwitchData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchData
- Msvm_EthernetSwitchData.InstanceID
- Msvm_EthernetSwitchData.Caption
- Msvm_EthernetSwitchData.Description
- Msvm_EthernetSwitchData.ElementName
- Msvm_EthernetSwitchData.SystemCreationClassName
- Msvm_EthernetSwitchData.SystemName
- Msvm_EthernetSwitchData.CreationClassName
- Msvm_EthernetSwitchData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca2e4e01266a0a7da0f3ec85a86615406625f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368786"
---
# <a name="msvm_ethernetswitchdata-class"></a><span data-ttu-id="ae5b8-103">MSVM \_ ethernetzwitchdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="ae5b8-103">Msvm\_EthernetSwitchData class</span></span>

<span data-ttu-id="ae5b8-104">Eine abstrakte Klasse, die eine Ressource für eine bestimmte Instanz eines Ethernet-Schalters darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-104">Abstract class that represents a resource for a given instance of an Ethernet switch.</span></span>

<span data-ttu-id="ae5b8-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae5b8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae5b8-106">Syntax</span></span>

``` syntax
[Abstract, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchData : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchBandwidthData";
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="ae5b8-107">Member</span><span class="sxs-lookup"><span data-stu-id="ae5b8-107">Members</span></span>

<span data-ttu-id="ae5b8-108">Die **MSVM \_ ethernetzwitchdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ae5b8-108">The **Msvm\_EthernetSwitchData** class has these types of members:</span></span>

-   [<span data-ttu-id="ae5b8-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae5b8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae5b8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ae5b8-110">Properties</span></span>

<span data-ttu-id="ae5b8-111">Die **MSVM \_ ethernetzwitchdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-111">The **Msvm\_EthernetSwitchData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae5b8-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae5b8-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae5b8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae5b8-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-115">A short description of the object.</span></span> <span data-ttu-id="ae5b8-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae5b8-117">**"Name der Klassenname"**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae5b8-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae5b8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ae5b8-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae5b8-121">Der Name der Klasse oder Unterklasse, die bei der Erstellung dieser Instanz verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-121">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b8-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae5b8-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae5b8-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae5b8-125">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-125">A description of the object.</span></span> <span data-ttu-id="ae5b8-126">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae5b8-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae5b8-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae5b8-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae5b8-130">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-130">A display name for the object.</span></span> <span data-ttu-id="ae5b8-131">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae5b8-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae5b8-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae5b8-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-135">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ae5b8-136">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ae5b8-137">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae5b8-138">**Name**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae5b8-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae5b8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-141">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ae5b8-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae5b8-142">Der eindeutige Name der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-142">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b8-143">**Systemkreationclassname**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae5b8-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae5b8-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-146">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ae5b8-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae5b8-147">Der Name der Erstellungs Klasse des hostingsystems.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-147">The hosting system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="ae5b8-148">**Systemname**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae5b8-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ae5b8-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ae5b8-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae5b8-151">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ae5b8-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ae5b8-152">Der Name des virtuellen Switchs, an den die zugeordnete Ressourcen Instanz gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="ae5b8-152">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae5b8-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae5b8-153">Requirements</span></span>



| <span data-ttu-id="ae5b8-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae5b8-154">Requirement</span></span> | <span data-ttu-id="ae5b8-155">Wert</span><span class="sxs-lookup"><span data-stu-id="ae5b8-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5b8-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae5b8-156">Minimum supported client</span></span><br/> | <span data-ttu-id="ae5b8-157">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae5b8-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ae5b8-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae5b8-158">Minimum supported server</span></span><br/> | <span data-ttu-id="ae5b8-159">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae5b8-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae5b8-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae5b8-160">Namespace</span></span><br/>                | <span data-ttu-id="ae5b8-161">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ae5b8-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ae5b8-162">MOF</span><span class="sxs-lookup"><span data-stu-id="ae5b8-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae5b8-163"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b8-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae5b8-164">DLL</span><span class="sxs-lookup"><span data-stu-id="ae5b8-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae5b8-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae5b8-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

