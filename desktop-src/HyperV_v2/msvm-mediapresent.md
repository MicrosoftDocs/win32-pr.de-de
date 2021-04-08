---
description: Ordnet ein Speicher Laufwerk den Medien zu, die in das Laufwerk eingefügt werden.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Msvm_MediaPresent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869592"
---
# <a name="msvm_mediapresent-class"></a><span data-ttu-id="2654a-103">MSVM \_ mediapresent-Klasse</span><span class="sxs-lookup"><span data-stu-id="2654a-103">Msvm\_MediaPresent class</span></span>

<span data-ttu-id="2654a-104">Ordnet ein Speicher Laufwerk den Medien zu, die in das Laufwerk eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="2654a-104">Associates a storage drive with the media inserted into the drive.</span></span> <span data-ttu-id="2654a-105">Diese Zuordnung wird für alle Speicher Laufwerk Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="2654a-105">This association is used for all storage drive objects.</span></span>

<span data-ttu-id="2654a-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2654a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2654a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2654a-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="2654a-108">Member</span><span class="sxs-lookup"><span data-stu-id="2654a-108">Members</span></span>

<span data-ttu-id="2654a-109">Die **MSVM \_ mediapresent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2654a-109">The **Msvm\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="2654a-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2654a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2654a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2654a-111">Properties</span></span>

<span data-ttu-id="2654a-112">Die **MSVM \_ mediapresent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2654a-112">The **Msvm\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2654a-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="2654a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2654a-114">Datentyp: **[ **CIM \_ mediaaccessdevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span><span class="sxs-lookup"><span data-stu-id="2654a-114">Data type: **[**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span></span>
</dt> <dt>

<span data-ttu-id="2654a-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2654a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2654a-116">Der Verweis auf das Medien Zugriffsgerät.</span><span class="sxs-lookup"><span data-stu-id="2654a-116">The reference to the media access device.</span></span> <span data-ttu-id="2654a-117">Diese Eigenschaft wird von [**CIM \_ mediapresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2654a-117">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="2654a-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="2654a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2654a-119">Datentyp: **[ **CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="2654a-119">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="2654a-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2654a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2654a-121">Der Verweis auf den Speicherblock, auf den mit dem Medien Zugriffsgerät zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="2654a-121">The reference to the storage extent accessed with the media access device.</span></span> <span data-ttu-id="2654a-122">Diese Eigenschaft wird von [**CIM \_ mediapresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2654a-122">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="2654a-123">**Fixedmedia**</span><span class="sxs-lookup"><span data-stu-id="2654a-123">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2654a-124">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="2654a-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2654a-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2654a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2654a-126">Gibt an, ob der Speicherplatz, auf den zugegriffen wird, fest ist und nicht aussteht.</span><span class="sxs-lookup"><span data-stu-id="2654a-126">Indicates whether the accessed storage extent is fixed and cannot be ejected.</span></span> <span data-ttu-id="2654a-127">Der Wert ist für Festplatten **true** und andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="2654a-127">The value is **True** for hard disks and **False** otherwise.</span></span> <span data-ttu-id="2654a-128">Diese Eigenschaft wird von [**CIM \_ mediapresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2654a-128">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2654a-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2654a-129">Remarks</span></span>

<span data-ttu-id="2654a-130">Der Zugriff auf die **MSVM \_ mediapresent** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="2654a-130">Access to the **Msvm\_MediaPresent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2654a-131">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2654a-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2654a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2654a-132">Requirements</span></span>



| <span data-ttu-id="2654a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2654a-133">Requirement</span></span> | <span data-ttu-id="2654a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2654a-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2654a-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2654a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2654a-136">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2654a-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2654a-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2654a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2654a-138">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2654a-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2654a-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="2654a-139">Namespace</span></span><br/>                | <span data-ttu-id="2654a-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2654a-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2654a-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2654a-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2654a-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2654a-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2654a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2654a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2654a-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2654a-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2654a-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2654a-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2654a-146">**CIM- \_ mediapresent**</span><span class="sxs-lookup"><span data-stu-id="2654a-146">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

[<span data-ttu-id="2654a-147">**CIM- \_ mediapresent**</span><span class="sxs-lookup"><span data-stu-id="2654a-147">**CIM\_MediaPresent**</span></span>](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[<span data-ttu-id="2654a-148">Speicher Klassen</span><span class="sxs-lookup"><span data-stu-id="2654a-148">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

