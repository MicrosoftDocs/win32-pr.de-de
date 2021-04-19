---
description: Stellt Informationen zu einer VHD-Datei bereit.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Msvm_VHDSetInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 51f1371baea902627160c2c7a1fb31d156be8951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349071"
---
# <a name="msvm_vhdsetinformation-class"></a><span data-ttu-id="3cf30-103">MSVM \_ vhdsetinformation-Klasse</span><span class="sxs-lookup"><span data-stu-id="3cf30-103">Msvm\_VHDSetInformation class</span></span>

<span data-ttu-id="3cf30-104">Stellt Informationen zu einer VHD-Datei bereit.</span><span class="sxs-lookup"><span data-stu-id="3cf30-104">Provides information about a VHD Set file.</span></span>

<span data-ttu-id="3cf30-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3cf30-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cf30-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cf30-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a><span data-ttu-id="3cf30-107">Member</span><span class="sxs-lookup"><span data-stu-id="3cf30-107">Members</span></span>

<span data-ttu-id="3cf30-108">Die **MSVM \_ vhdsetinformation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3cf30-108">The **Msvm\_VHDSetInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="3cf30-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cf30-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cf30-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cf30-110">Properties</span></span>

<span data-ttu-id="3cf30-111">Die **MSVM \_ vhdsetinformation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3cf30-111">The **Msvm\_VHDSetInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cf30-112">**Allpath**</span><span class="sxs-lookup"><span data-stu-id="3cf30-112">**AllPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf30-113">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3cf30-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3cf30-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cf30-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cf30-115">Eine Liste aller Dateien, die von der VHD-Set-Datei eingeschlossen werden, einschließlich aller Dateien, auf die nicht verwiesen wird, und aller übergeordneten Elemente der virtuellen Stamm Festplatte.</span><span class="sxs-lookup"><span data-stu-id="3cf30-115">A list of all files encompassed by the VHD Set file, including any unreferenced files and any parents of the root virtual hard disk.</span></span> <span data-ttu-id="3cf30-116">Alle Dateien, die nach der virtuellen Stamm Festplatte aufgeführt sind, werden von dieser VHD-Datei nicht mehr verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3cf30-116">All files listed after the root virtual hard disk are unmanaged by this VHD Set file.</span></span> <span data-ttu-id="3cf30-117">Dieses Feld ist möglicherweise leer, wenn diese Informationen nicht ausdrücklich angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="3cf30-117">This field may be empty if this information was not specifically requested.</span></span>

</dd> <dt>

<span data-ttu-id="3cf30-118">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="3cf30-118">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf30-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3cf30-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cf30-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cf30-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cf30-121">Der Pfad der VHD-Satz Datei.</span><span class="sxs-lookup"><span data-stu-id="3cf30-121">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="3cf30-122">**Snapshotidlist**</span><span class="sxs-lookup"><span data-stu-id="3cf30-122">**SnapshotIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cf30-123">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="3cf30-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3cf30-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3cf30-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3cf30-125">Eine Liste von GUIDs, die alle in dieser VHD-Satz Datei enthaltenen Momentaufnahmen darstellen.</span><span class="sxs-lookup"><span data-stu-id="3cf30-125">A list of GUIDs representing all of the snapshots contained by this VHD Set file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cf30-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cf30-126">Requirements</span></span>



| <span data-ttu-id="3cf30-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cf30-127">Requirement</span></span> | <span data-ttu-id="3cf30-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3cf30-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf30-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cf30-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf30-130">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cf30-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3cf30-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cf30-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf30-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3cf30-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3cf30-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cf30-133">Namespace</span></span><br/>                | <span data-ttu-id="3cf30-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3cf30-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3cf30-135">MOF</span><span class="sxs-lookup"><span data-stu-id="3cf30-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cf30-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3cf30-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cf30-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3cf30-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cf30-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3cf30-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




