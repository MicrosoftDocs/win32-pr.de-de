---
description: Festlegen von Daten, die als Array an die MSVM \_ collectionreferencepointexportsettingdata-Klasse übermittelt werden sollen.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Msvm_VirtualMachineToDisks-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862067"
---
# <a name="msvm_virtualmachinetodisks-class"></a><span data-ttu-id="dc04d-103">MSVM \_ virtualmachinetodisks-Klasse</span><span class="sxs-lookup"><span data-stu-id="dc04d-103">Msvm\_VirtualMachineToDisks class</span></span>

<span data-ttu-id="dc04d-104">Festlegen von Daten, die als Array an die [**MSVM \_ collectionreferencepointexportsettingdata**](msvm-collectionreferencepointexportsettingdata.md) -Klasse übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dc04d-104">Setting data to be passed as an array to the [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) class.</span></span>

<span data-ttu-id="dc04d-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc04d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc04d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc04d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="dc04d-107">Member</span><span class="sxs-lookup"><span data-stu-id="dc04d-107">Members</span></span>

<span data-ttu-id="dc04d-108">Die **MSVM-Klasse " \_ virtualmachinetodisks** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc04d-108">The **Msvm\_VirtualMachineToDisks** class has these types of members:</span></span>

-   [<span data-ttu-id="dc04d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc04d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc04d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc04d-110">Properties</span></span>

<span data-ttu-id="dc04d-111">Die **MSVM \_ virtualmachinetodisks** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc04d-111">The **Msvm\_VirtualMachineToDisks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc04d-112">**Diskstoexport**</span><span class="sxs-lookup"><span data-stu-id="dc04d-112">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc04d-113">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="dc04d-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc04d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc04d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc04d-115">Die WMI-Instanz-IDs der Datenträger, die zu der ID der virtuellen Maschine gehören, für die Daten exportiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="dc04d-115">The WMI instance IDs of the disks those belong to given Virtual Machine ID for which data needs to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="dc04d-116">**Virtualmachineid**</span><span class="sxs-lookup"><span data-stu-id="dc04d-116">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc04d-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc04d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc04d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dc04d-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dc04d-119">Eine ID des virtuellen Computers, der virtuelle Datenträger zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dc04d-119">A Virtual Machine ID that virtual disks are associated with.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc04d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc04d-120">Requirements</span></span>



| <span data-ttu-id="dc04d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc04d-121">Requirement</span></span> | <span data-ttu-id="dc04d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="dc04d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc04d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc04d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc04d-124">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc04d-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="dc04d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc04d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc04d-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dc04d-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dc04d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc04d-127">Namespace</span></span><br/>                | <span data-ttu-id="dc04d-128">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="dc04d-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dc04d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="dc04d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc04d-130"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dc04d-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc04d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dc04d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc04d-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc04d-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




