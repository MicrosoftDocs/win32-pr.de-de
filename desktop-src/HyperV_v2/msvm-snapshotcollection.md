---
description: Stellt eine Auflistung von Momentaufnahmen des virtuellen Systems dar.
ms.assetid: c9b64421-232c-4f32-a088-6b98602ca3f4
title: Msvm_SnapshotCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotCollection
- Msvm_SnapshotCollection.CollectionID
- Msvm_SnapshotCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e24566f1f5c5500258f14f88cbe2b7c4fa29e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130693"
---
# <a name="msvm_snapshotcollection-class"></a><span data-ttu-id="31a50-103">MSVM \_ snapshotcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="31a50-103">Msvm\_SnapshotCollection class</span></span>

<span data-ttu-id="31a50-104">Stellt eine Auflistung von Momentaufnahmen des virtuellen Systems dar.</span><span class="sxs-lookup"><span data-stu-id="31a50-104">Represents a collection of virtual system snapshots.</span></span>

<span data-ttu-id="31a50-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="31a50-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a50-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="31a50-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotCollection : CIM_Collection
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="31a50-107">Member</span><span class="sxs-lookup"><span data-stu-id="31a50-107">Members</span></span>

<span data-ttu-id="31a50-108">Die **MSVM \_ snapshotcollection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="31a50-108">The **Msvm\_SnapshotCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="31a50-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31a50-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31a50-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31a50-110">Properties</span></span>

<span data-ttu-id="31a50-111">Die **MSVM \_ snapshotcollection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="31a50-111">The **Msvm\_SnapshotCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31a50-112">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="31a50-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a50-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31a50-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31a50-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31a50-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31a50-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="31a50-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="31a50-116">Die eindeutige Identifikation des Auflistungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="31a50-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="31a50-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="31a50-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31a50-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="31a50-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31a50-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31a50-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31a50-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Elementname")</span><span class="sxs-lookup"><span data-stu-id="31a50-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="31a50-121">Ein benutzerdefinierter Name für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="31a50-121">An user-defined name for the collection.</span></span> <span data-ttu-id="31a50-122">Beachten Sie, dass dies nicht unbedingt eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="31a50-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31a50-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a50-123">Requirements</span></span>



| <span data-ttu-id="31a50-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31a50-124">Requirement</span></span> | <span data-ttu-id="31a50-125">Wert</span><span class="sxs-lookup"><span data-stu-id="31a50-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31a50-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31a50-126">Minimum supported client</span></span><br/> | <span data-ttu-id="31a50-127">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31a50-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="31a50-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31a50-128">Minimum supported server</span></span><br/> | <span data-ttu-id="31a50-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="31a50-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="31a50-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="31a50-130">Namespace</span></span><br/>                | <span data-ttu-id="31a50-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="31a50-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="31a50-132">MOF</span><span class="sxs-lookup"><span data-stu-id="31a50-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31a50-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="31a50-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31a50-134">DLL</span><span class="sxs-lookup"><span data-stu-id="31a50-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31a50-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31a50-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="31a50-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31a50-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a50-137">**CIM \_ -Auflistung**</span><span class="sxs-lookup"><span data-stu-id="31a50-137">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

