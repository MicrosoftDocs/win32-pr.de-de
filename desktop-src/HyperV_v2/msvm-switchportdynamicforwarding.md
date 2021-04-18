---
description: Verbindet einen Switchport mit einem dynamischen Forward-Eintrag (erlernte Mac-Adresse).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Msvm_SwitchPortDynamicForwarding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e6dda46302e9e8c58710bad1f4221e14e2c3f4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357499"
---
# <a name="msvm_switchportdynamicforwarding-class"></a><span data-ttu-id="561da-103">MSVM \_ switchportdynamicforwarding-Klasse</span><span class="sxs-lookup"><span data-stu-id="561da-103">Msvm\_SwitchPortDynamicForwarding class</span></span>

<span data-ttu-id="561da-104">Verbindet einen Switchport mit einem dynamischen Forward-Eintrag (erlernte Mac-Adresse).</span><span class="sxs-lookup"><span data-stu-id="561da-104">Connects a switch port to a dynamic forward entry (learned MAC address).</span></span> <span data-ttu-id="561da-105">Dies ist nützlich, um alle gelernten Mac-Adressen für einen bestimmten Port zu suchen.</span><span class="sxs-lookup"><span data-stu-id="561da-105">This is useful in finding all of the learned MAC addresses for a specified port.</span></span>

<span data-ttu-id="561da-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="561da-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="561da-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="561da-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="561da-108">Member</span><span class="sxs-lookup"><span data-stu-id="561da-108">Members</span></span>

<span data-ttu-id="561da-109">Die **MSVM \_ switchportdynamicforwarding** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="561da-109">The **Msvm\_SwitchPortDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="561da-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="561da-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="561da-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="561da-111">Properties</span></span>

<span data-ttu-id="561da-112">Die **MSVM \_ switchportdynamicforwarding** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="561da-112">The **Msvm\_SwitchPortDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="561da-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="561da-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="561da-114">Datentyp: **[ **MSVM \_ ethernetzwitchport**](msvm-ethernetswitchport.md)**</span><span class="sxs-lookup"><span data-stu-id="561da-114">Data type: **[**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="561da-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="561da-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="561da-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="561da-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="561da-117">Ein Verweis auf eine Instanz der [**MSVM \_ ethernetzwitchport**](msvm-ethernetswitchport.md) -Klasse, die den Switchport darstellt.</span><span class="sxs-lookup"><span data-stu-id="561da-117">A reference to an instance of the [**Msvm\_EthernetSwitchPort**](msvm-ethernetswitchport.md) class that represents the switch port.</span></span>

</dd> <dt>

<span data-ttu-id="561da-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="561da-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="561da-119">Datentyp: **[ **MSVM \_ dynamicforwardingentry**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="561da-119">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="561da-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="561da-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="561da-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="561da-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="561da-122">Ein Verweis auf eine Instanz der [**MSVM \_ dynamicforwardingentry**](msvm-dynamicforwardingentry.md) -Klasse, die den dynamischen Weiterleitungs Eintrag der Weiterleitungs Datenbank darstellt.</span><span class="sxs-lookup"><span data-stu-id="561da-122">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="561da-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="561da-123">Remarks</span></span>

<span data-ttu-id="561da-124">Der Zugriff auf die **MSVM \_ switchportdynamicforwarding** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="561da-124">Access to the **Msvm\_SwitchPortDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="561da-125">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="561da-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="561da-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="561da-126">Examples</span></span>

<span data-ttu-id="561da-127">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="561da-127">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="561da-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="561da-128">Requirements</span></span>



| <span data-ttu-id="561da-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="561da-129">Requirement</span></span> | <span data-ttu-id="561da-130">Wert</span><span class="sxs-lookup"><span data-stu-id="561da-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="561da-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="561da-131">Minimum supported client</span></span><br/> | <span data-ttu-id="561da-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="561da-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="561da-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="561da-133">Minimum supported server</span></span><br/> | <span data-ttu-id="561da-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="561da-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="561da-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="561da-135">Namespace</span></span><br/>                | <span data-ttu-id="561da-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="561da-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="561da-137">MOF</span><span class="sxs-lookup"><span data-stu-id="561da-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="561da-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="561da-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="561da-139">DLL</span><span class="sxs-lookup"><span data-stu-id="561da-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="561da-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="561da-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="561da-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="561da-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="561da-142">**CIM \_ switchportdynamicforwarding**</span><span class="sxs-lookup"><span data-stu-id="561da-142">**CIM\_SwitchPortDynamicForwarding**</span></span>](cim-switchportdynamicforwarding.md)
</dt> <dt>

<span data-ttu-id="561da-143">[**CIM \_ switchportdynamicforwarding**](/previous-versions//cc136921(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="561da-143">[**CIM\_SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))</span></span>
</dt> </dl>

 

