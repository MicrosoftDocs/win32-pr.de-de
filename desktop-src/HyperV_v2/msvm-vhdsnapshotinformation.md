---
description: Stellt Informationen zu einer Momentaufnahme in einer VHD-Datei bereit.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Msvm_VHDSnapshotInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863287"
---
# <a name="msvm_vhdsnapshotinformation-class"></a><span data-ttu-id="836ba-103">MSVM \_ vhdsnapshotinformation-Klasse</span><span class="sxs-lookup"><span data-stu-id="836ba-103">Msvm\_VHDSnapshotInformation class</span></span>

<span data-ttu-id="836ba-104">Stellt Informationen zu einer Momentaufnahme in einer VHD-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="836ba-104">Provides information about a snapshot within a VHD Set file</span></span>

<span data-ttu-id="836ba-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="836ba-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="836ba-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="836ba-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a><span data-ttu-id="836ba-107">Member</span><span class="sxs-lookup"><span data-stu-id="836ba-107">Members</span></span>

<span data-ttu-id="836ba-108">Die **MSVM \_ vhdsnapshotinformation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="836ba-108">The **Msvm\_VHDSnapshotInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="836ba-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="836ba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="836ba-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="836ba-110">Properties</span></span>

<span data-ttu-id="836ba-111">Die **MSVM \_ vhdsnapshotinformation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="836ba-111">The **Msvm\_VHDSnapshotInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="836ba-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="836ba-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="836ba-113">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="836ba-113">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="836ba-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="836ba-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="836ba-115">Das Datum und die Uhrzeit der Erstellung der Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="836ba-115">The date and time of this snapshot's creation.</span></span>

</dd> <dt>

<span data-ttu-id="836ba-116">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="836ba-116">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="836ba-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="836ba-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="836ba-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="836ba-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="836ba-119">Der Pfad der VHD-Satz Datei.</span><span class="sxs-lookup"><span data-stu-id="836ba-119">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="836ba-120">**"Parametripathslist"**</span><span class="sxs-lookup"><span data-stu-id="836ba-120">**ParentPathsList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="836ba-121">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="836ba-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="836ba-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="836ba-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="836ba-123">Eine Liste der Dateipfade, die alle Dateien darstellen, von denen diese Momentaufnahme abhängt.</span><span class="sxs-lookup"><span data-stu-id="836ba-123">A list of file paths representing all of the files on which this snapshot depends.</span></span> <span data-ttu-id="836ba-124">Dieses Feld ist leer, es sei denn, es wird ausdrücklich angefordert.</span><span class="sxs-lookup"><span data-stu-id="836ba-124">This field will be empty unless specifically requested.</span></span> <span data-ttu-id="836ba-125">Der erste Eintrag ist das unmittelbar übergeordnete Element der Datei, wobei der letzte Eintrag der Stamm ist.</span><span class="sxs-lookup"><span data-stu-id="836ba-125">The first entry is the file's immediate parent, with the last entry being the root.</span></span>

</dd> <dt>

<span data-ttu-id="836ba-126">**Resilientchangetrackingid**</span><span class="sxs-lookup"><span data-stu-id="836ba-126">**ResilientChangeTrackingId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="836ba-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="836ba-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="836ba-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="836ba-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="836ba-129">Die robuste Änderungsnachverfolgungs-ID, die dieser Momentaufnahme zugeordnet ist, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="836ba-129">The resilient change tracking ID, if any, associated with this snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="836ba-130">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="836ba-130">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="836ba-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="836ba-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="836ba-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="836ba-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="836ba-133">Eine GUID, die diese Momentaufnahme innerhalb der VHD-Satz Datei eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="836ba-133">A GUID that uniquely identifies this snapshot within the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="836ba-134">**SnapshotPath**</span><span class="sxs-lookup"><span data-stu-id="836ba-134">**SnapshotPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="836ba-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="836ba-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="836ba-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="836ba-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="836ba-137">Der Pfad der Datei, die durch diese Momentaufnahme dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="836ba-137">The path of the file represented by this snapshot.</span></span> <span data-ttu-id="836ba-138">Dieses Feld ist möglicherweise leer, wenn dieser Momentaufnahme keine Datei zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="836ba-138">This field may be empty if there is no file associated with this snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="836ba-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="836ba-139">Requirements</span></span>



| <span data-ttu-id="836ba-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="836ba-140">Requirement</span></span> | <span data-ttu-id="836ba-141">Wert</span><span class="sxs-lookup"><span data-stu-id="836ba-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="836ba-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="836ba-142">Minimum supported client</span></span><br/> | <span data-ttu-id="836ba-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="836ba-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="836ba-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="836ba-144">Minimum supported server</span></span><br/> | <span data-ttu-id="836ba-145">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="836ba-145">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="836ba-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="836ba-146">Namespace</span></span><br/>                | <span data-ttu-id="836ba-147">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="836ba-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="836ba-148">MOF</span><span class="sxs-lookup"><span data-stu-id="836ba-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="836ba-149"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="836ba-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="836ba-150">DLL</span><span class="sxs-lookup"><span data-stu-id="836ba-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="836ba-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="836ba-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




