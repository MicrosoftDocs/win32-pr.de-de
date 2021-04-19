---
description: Stellt den Konfigurations Status der Datenträger zusammenlaufseinstellungen für einen virtuellen Computer dar.
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Msvm_DiskMergeSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362657"
---
# <a name="msvm_diskmergesettingdata-class"></a><span data-ttu-id="9b497-103">MSVM \_ diskmergesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="9b497-103">Msvm\_DiskMergeSettingData class</span></span>

<span data-ttu-id="9b497-104">Stellt den Konfigurations Status der Datenträger zusammenlaufseinstellungen für einen virtuellen Computer dar.</span><span class="sxs-lookup"><span data-stu-id="9b497-104">Represents the configuration state of the disk merge settings for a virtual machine.</span></span>

<span data-ttu-id="9b497-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b497-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b497-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b497-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a><span data-ttu-id="9b497-107">Member</span><span class="sxs-lookup"><span data-stu-id="9b497-107">Members</span></span>

<span data-ttu-id="9b497-108">Die **MSVM \_ diskmergesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9b497-108">The **Msvm\_DiskMergeSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9b497-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b497-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b497-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b497-110">Properties</span></span>

<span data-ttu-id="9b497-111">Die **MSVM \_ diskmergesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b497-111">The **Msvm\_DiskMergeSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b497-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9b497-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b497-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b497-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b497-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b497-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b497-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9b497-115">A short description of the object.</span></span> <span data-ttu-id="9b497-116">Diese Eigenschaft wird von der [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) -Klasse geerbt und ist immer auf "Datenträger-Merge-Einstellungsdaten" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b497-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="9b497-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9b497-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b497-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b497-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b497-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b497-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b497-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9b497-120">A description of the object.</span></span> <span data-ttu-id="9b497-121">Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Microsoft Disk Merge Setting Data" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b497-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="9b497-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9b497-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b497-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b497-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b497-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b497-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b497-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9b497-125">A display name for the object.</span></span> <span data-ttu-id="9b497-126">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und ist immer auf "Datenträger-Merge-Einstellungsdaten" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b497-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Disk Merge Setting Data".</span></span> <span data-ttu-id="9b497-127">Durch Ändern dieser Eigenschaft wird die **ElementName** -Eigenschaft der zugeordneten [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) -Ableitung geändert.</span><span class="sxs-lookup"><span data-stu-id="9b497-127">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="9b497-128">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9b497-128">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="9b497-129">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9b497-129">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b497-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b497-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b497-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b497-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b497-132">Gibt den aktivierten Zustand der Datenträger-Merge-Funktionalität an.</span><span class="sxs-lookup"><span data-stu-id="9b497-132">Specifies the enabled state of the disk merge functionality.</span></span>

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

<span data-ttu-id="9b497-133">**Temporär deaktiviert** (0)</span><span class="sxs-lookup"><span data-stu-id="9b497-133">**Temporarily disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9b497-134">**Aktiviert** (1)</span><span class="sxs-lookup"><span data-stu-id="9b497-134">**Enabled** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b497-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9b497-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b497-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b497-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b497-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b497-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b497-138">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="9b497-138">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9b497-139">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="9b497-139">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9b497-140">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) geerbt und ist immer auf "Microsoft:*GUID* Geräte-ID- \\ *Daten*" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9b497-140">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b497-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b497-141">Requirements</span></span>



| <span data-ttu-id="9b497-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b497-142">Requirement</span></span> | <span data-ttu-id="9b497-143">Wert</span><span class="sxs-lookup"><span data-stu-id="9b497-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b497-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b497-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9b497-145">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b497-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9b497-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b497-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9b497-147">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9b497-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9b497-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b497-148">Namespace</span></span><br/>                | <span data-ttu-id="9b497-149">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9b497-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9b497-150">MOF</span><span class="sxs-lookup"><span data-stu-id="9b497-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b497-151"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9b497-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b497-152">DLL</span><span class="sxs-lookup"><span data-stu-id="9b497-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b497-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9b497-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

