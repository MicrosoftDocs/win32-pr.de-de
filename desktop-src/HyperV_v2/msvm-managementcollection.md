---
description: Stellt eine Auflistung anderer Auflistungen dar.
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Msvm_ManagementCollection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360838"
---
# <a name="msvm_managementcollection-class"></a><span data-ttu-id="3c550-103">MSVM \_ managementcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="3c550-103">Msvm\_ManagementCollection class</span></span>

<span data-ttu-id="3c550-104">Stellt eine Auflistung anderer Auflistungen dar.</span><span class="sxs-lookup"><span data-stu-id="3c550-104">Represents a collection of other collections.</span></span>

<span data-ttu-id="3c550-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c550-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c550-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c550-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="3c550-107">Member</span><span class="sxs-lookup"><span data-stu-id="3c550-107">Members</span></span>

<span data-ttu-id="3c550-108">Die **MSVM \_ managementcollection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3c550-108">The **Msvm\_ManagementCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="3c550-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c550-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c550-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3c550-110">Properties</span></span>

<span data-ttu-id="3c550-111">Die **MSVM \_ managementcollection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3c550-111">The **Msvm\_ManagementCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c550-112">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="3c550-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c550-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c550-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c550-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c550-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c550-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="3c550-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="3c550-116">Die eindeutige Identifikation des Auflistungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="3c550-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="3c550-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3c550-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c550-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3c550-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c550-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3c550-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c550-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Elementname")</span><span class="sxs-lookup"><span data-stu-id="3c550-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="3c550-121">Ein benutzerdefinierter Name für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3c550-121">An user-defined name for the collection.</span></span> <span data-ttu-id="3c550-122">Beachten Sie, dass dies nicht unbedingt eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="3c550-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c550-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c550-123">Requirements</span></span>



| <span data-ttu-id="3c550-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c550-124">Requirement</span></span> | <span data-ttu-id="3c550-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3c550-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c550-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c550-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3c550-127">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c550-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3c550-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c550-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3c550-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3c550-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3c550-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c550-130">Namespace</span></span><br/>                | <span data-ttu-id="3c550-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3c550-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3c550-132">MOF</span><span class="sxs-lookup"><span data-stu-id="3c550-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c550-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3c550-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c550-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3c550-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c550-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c550-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3c550-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c550-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c550-137">**CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="3c550-137">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

