---
description: Ordnet einen virtuellen Computer und seine Geräte Instanzen von CIM \_ SettingData zu, die die aktuellen Einstellungen darstellen, die für diese Objekte gelten.
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216764"
---
# <a name="msvm_settingsdefinestate-class"></a><span data-ttu-id="1762b-103">MSVM \_ settingsdefinestate-Klasse</span><span class="sxs-lookup"><span data-stu-id="1762b-103">Msvm\_SettingsDefineState class</span></span>

<span data-ttu-id="1762b-104">Ordnet einen virtuellen Computer und seine Geräte Instanzen von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) zu, die die aktuellen Einstellungen darstellen, die für diese Objekte gelten.</span><span class="sxs-lookup"><span data-stu-id="1762b-104">Associates a virtual machine and its devices with instances of [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) that represent the current settings that apply to these objects.</span></span> <span data-ttu-id="1762b-105">Genauer gesagt, ordnet Sie [**MSVM \_ Computersystem**](msvm-computersystem.md) Instanzen von [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)zu und ordnet \**MSVM \_ \** _-Ableitungen von [_ *CIM \_ LogicalDevice* \*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) mit \**MSVM \_ \** _-Ableitungen von [_ *CIM \_ resourcezuordcationsettingdata* \*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)zu.</span><span class="sxs-lookup"><span data-stu-id="1762b-105">More specifically, it associates [**Msvm\_ComputerSystem**](msvm-computersystem.md) with instances of [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md), and it associates \**Msvm\_\** _ derivatives of [_ *CIM\_LogicalDevice*\*](/windows/desktop/CIMWin32Prov/cim-logicaldevice) with \**Msvm\_\** _ derivatives of [_ *CIM\_ResourceAllocationSettingData*\*](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="1762b-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1762b-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1762b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1762b-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="1762b-108">Member</span><span class="sxs-lookup"><span data-stu-id="1762b-108">Members</span></span>

<span data-ttu-id="1762b-109">Die **MSVM \_ settingsdefinestate** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1762b-109">The **Msvm\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="1762b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1762b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1762b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1762b-111">Properties</span></span>

<span data-ttu-id="1762b-112">Die **MSVM \_ settingsdefinestate** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1762b-112">The **Msvm\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1762b-113">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="1762b-113">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1762b-114">Datentyp: **[ **MSVM \_ Computersystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="1762b-114">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1762b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1762b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1762b-116">Ein Verweis auf den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1762b-116">A reference to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="1762b-117">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="1762b-117">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1762b-118">Datentyp: **[ **MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="1762b-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1762b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1762b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1762b-120">Ein Verweis auf die derzeit aktiven Einstellungen für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1762b-120">A reference to the currently active settings for the virtual machine.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1762b-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1762b-121">Remarks</span></span>

<span data-ttu-id="1762b-122">Der Zugriff auf die **MSVM \_ settingsdefinestate** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="1762b-122">Access to the **Msvm\_SettingsDefineState** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1762b-123">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1762b-123">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1762b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1762b-124">Requirements</span></span>



| <span data-ttu-id="1762b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1762b-125">Requirement</span></span> | <span data-ttu-id="1762b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="1762b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1762b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1762b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1762b-128">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="1762b-128">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1762b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1762b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1762b-130">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1762b-130">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1762b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="1762b-131">Namespace</span></span><br/>                | <span data-ttu-id="1762b-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="1762b-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1762b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1762b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1762b-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1762b-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1762b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1762b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1762b-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1762b-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1762b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1762b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1762b-138">**CIM \_ settingsdefinestate**</span><span class="sxs-lookup"><span data-stu-id="1762b-138">**CIM\_SettingsDefineState**</span></span>](cim-settingsdefinestate.md)
</dt> <dt>

[<span data-ttu-id="1762b-139">**CIM \_ settingsdefinestate**</span><span class="sxs-lookup"><span data-stu-id="1762b-139">**CIM\_SettingsDefineState**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[<span data-ttu-id="1762b-140">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="1762b-140">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

