---
description: Verschiebt eine virtuelle Festplatte von der Quell-in den Zielpfad.
ms.assetid: f51f7bf3-585a-442d-b84d-51d633c38dea
title: Msvm_MoveUnmanagedVhd-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MoveUnmanagedVhd
- Msvm_MoveUnmanagedVhd.VhdSourcePath
- Msvm_MoveUnmanagedVhd.VhdDestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e98139b747f4b32265e27bc84ca240f496dea715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868499"
---
# <a name="msvm_moveunmanagedvhd-class"></a><span data-ttu-id="2a6e9-103">MSVM- \_ Klasse "muveunmanagedvhd"</span><span class="sxs-lookup"><span data-stu-id="2a6e9-103">Msvm\_MoveUnmanagedVhd class</span></span>

<span data-ttu-id="2a6e9-104">Verschiebt eine virtuelle Festplatte von der Quell-in den Zielpfad.</span><span class="sxs-lookup"><span data-stu-id="2a6e9-104">Moves a virtual hard drive from the source to the destination path.</span></span>

<span data-ttu-id="2a6e9-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2a6e9-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a6e9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a6e9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_MoveUnmanagedVhd : CIM_ManagedElement
{
  string VhdSourcePath;
  string VhdDestinationPath;
};
```

## <a name="members"></a><span data-ttu-id="2a6e9-107">Member</span><span class="sxs-lookup"><span data-stu-id="2a6e9-107">Members</span></span>

<span data-ttu-id="2a6e9-108">Die **MSVM-Klasse " \_ muveunmanagedvhd** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2a6e9-108">The **Msvm\_MoveUnmanagedVhd** class has these types of members:</span></span>

-   [<span data-ttu-id="2a6e9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a6e9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a6e9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a6e9-110">Properties</span></span>

<span data-ttu-id="2a6e9-111">Die **MSVM-Klasse " \_ muveunmanagedvhd** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a6e9-111">The **Msvm\_MoveUnmanagedVhd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a6e9-112">**Vhddestinationpath**</span><span class="sxs-lookup"><span data-stu-id="2a6e9-112">**VhdDestinationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a6e9-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a6e9-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a6e9-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a6e9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a6e9-115">Der Zielpfad.</span><span class="sxs-lookup"><span data-stu-id="2a6e9-115">The destination path.</span></span>

</dd> <dt>

<span data-ttu-id="2a6e9-116">**Vhdsourcepath**</span><span class="sxs-lookup"><span data-stu-id="2a6e9-116">**VhdSourcePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a6e9-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a6e9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a6e9-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a6e9-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a6e9-119">Der Quellpfad der zu verschiebenden virtuellen Festplatte.</span><span class="sxs-lookup"><span data-stu-id="2a6e9-119">The source path of the virtual hard drive to move.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a6e9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a6e9-120">Requirements</span></span>



| <span data-ttu-id="2a6e9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a6e9-121">Requirement</span></span> | <span data-ttu-id="2a6e9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2a6e9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a6e9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a6e9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2a6e9-124">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a6e9-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2a6e9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a6e9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2a6e9-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2a6e9-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2a6e9-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a6e9-127">Namespace</span></span><br/>                | <span data-ttu-id="2a6e9-128">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a6e9-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2a6e9-129">MOF</span><span class="sxs-lookup"><span data-stu-id="2a6e9-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a6e9-130"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2a6e9-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a6e9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2a6e9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a6e9-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a6e9-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a6e9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a6e9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a6e9-134">**CIM- \_ managedelta**</span><span class="sxs-lookup"><span data-stu-id="2a6e9-134">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

 




