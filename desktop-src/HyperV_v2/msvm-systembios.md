---
description: Wird verwendet, um dem BIOS eine virtuelle Maschine zuzuordnen.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Msvm_SystemBIOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128421"
---
# <a name="msvm_systembios-class"></a><span data-ttu-id="dbd36-103">MSVM- \_ Systembios-Klasse</span><span class="sxs-lookup"><span data-stu-id="dbd36-103">Msvm\_SystemBIOS class</span></span>

<span data-ttu-id="dbd36-104">Wird verwendet, um dem BIOS eine virtuelle Maschine zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="dbd36-104">Used to associate a virtual machine with its BIOS.</span></span>

<span data-ttu-id="dbd36-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbd36-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbd36-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbd36-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="dbd36-107">Member</span><span class="sxs-lookup"><span data-stu-id="dbd36-107">Members</span></span>

<span data-ttu-id="dbd36-108">Die **MSVM- \_ Systembios** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dbd36-108">The **Msvm\_SystemBIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="dbd36-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbd36-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbd36-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbd36-110">Properties</span></span>

<span data-ttu-id="dbd36-111">Die **MSVM- \_ Systembios** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbd36-111">The **Msvm\_SystemBIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbd36-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="dbd36-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd36-113">Datentyp: **[ **CIM \_ Computersystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="dbd36-113">Data type: **[**CIM\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="dbd36-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbd36-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbd36-115">Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="dbd36-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dbd36-116">Der virtuelle Computer, der über das BIOS gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dbd36-116">The virtual machine that starts from the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="dbd36-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dbd36-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbd36-118">Datentyp: **[ **MSVM \_ bioselements**](msvm-bioselement.md)**</span><span class="sxs-lookup"><span data-stu-id="dbd36-118">Data type: **[**Msvm\_BIOSElement**](msvm-bioselement.md)**</span></span>
</dt> <dt>

<span data-ttu-id="dbd36-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbd36-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbd36-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="dbd36-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="dbd36-121">Das BIOS, das dem virtuellen Computer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dbd36-121">The BIOS associated with the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbd36-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbd36-122">Remarks</span></span>

<span data-ttu-id="dbd36-123">Der Zugriff auf die **MSVM- \_ Systembios** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="dbd36-123">Access to the **Msvm\_SystemBIOS** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dbd36-124">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dbd36-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbd36-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbd36-125">Requirements</span></span>



| <span data-ttu-id="dbd36-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbd36-126">Requirement</span></span> | <span data-ttu-id="dbd36-127">Wert</span><span class="sxs-lookup"><span data-stu-id="dbd36-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbd36-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbd36-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dbd36-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbd36-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dbd36-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbd36-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dbd36-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbd36-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dbd36-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbd36-132">Namespace</span></span><br/>                | <span data-ttu-id="dbd36-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="dbd36-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dbd36-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dbd36-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbd36-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dbd36-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbd36-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dbd36-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbd36-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dbd36-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dbd36-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbd36-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbd36-139">**CIM- \_ Systembios**</span><span class="sxs-lookup"><span data-stu-id="dbd36-139">**CIM\_SystemBIOS**</span></span>](cim-systembios.md)
</dt> <dt>

[<span data-ttu-id="dbd36-140">BIOS-Klassen</span><span class="sxs-lookup"><span data-stu-id="dbd36-140">BIOS Classes</span></span>](bios-classes.md)
</dt> </dl>

 

