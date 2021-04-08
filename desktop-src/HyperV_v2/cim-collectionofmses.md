---
description: Eine abstrakte Klasse für Unterklassen, die eine Auflistung von CIM \_ ManagedSystemElement-Objekten darstellen. Mithilfe dieser Sammlungen können verwaltete Systemelemente zu Identifikationszwecken gruppiert und die Zuordnung von Einstellungen und Konfigurationen vereinfacht werden.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: CIM_CollectionOfMSEs-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864123"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a><span data-ttu-id="c3f83-104">CIM_CollectionOfMSEs-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="c3f83-104">CIM_CollectionOfMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="c3f83-105">Eine abstrakte Klasse für Unterklassen, die eine Auflistung von [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekten darstellen.</span><span class="sxs-lookup"><span data-stu-id="c3f83-105">An abstract class for subclasses that represent a collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span> <span data-ttu-id="c3f83-106">Mithilfe dieser Sammlungen können verwaltete Systemelemente zu Identifikationszwecken gruppiert und die Zuordnung von Einstellungen und Konfigurationen vereinfacht werden.</span><span class="sxs-lookup"><span data-stu-id="c3f83-106">These collections allow managed system elements to be grouped for identification purposes and to simplify the association of settings and configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f83-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3f83-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a><span data-ttu-id="c3f83-108">Member</span><span class="sxs-lookup"><span data-stu-id="c3f83-108">Members</span></span>

<span data-ttu-id="c3f83-109">Die **CIM \_ CollectionOfMSEs** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c3f83-109">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="c3f83-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3f83-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3f83-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3f83-111">Properties</span></span>

<span data-ttu-id="c3f83-112">Die **CIM \_ CollectionOfMSEs** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c3f83-112">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3f83-113">**Sammlungs**</span><span class="sxs-lookup"><span data-stu-id="c3f83-113">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f83-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c3f83-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f83-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c3f83-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f83-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c3f83-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c3f83-117">Die Identifizierung des Auflistungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="c3f83-117">The identification of the collection object.</span></span> <span data-ttu-id="c3f83-118">Bei einer Unterklasse kann die **CollectionId** -Eigenschaft als Schlüsseleigenschaft überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c3f83-118">When subclassed, the **CollectionID** property can be overridden as a key property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3f83-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3f83-119">Requirements</span></span>



| <span data-ttu-id="c3f83-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3f83-120">Requirement</span></span> | <span data-ttu-id="c3f83-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c3f83-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f83-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3f83-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f83-123">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3f83-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c3f83-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3f83-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f83-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c3f83-125">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c3f83-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3f83-126">Namespace</span></span><br/>                | <span data-ttu-id="c3f83-127">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c3f83-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c3f83-128">MOF</span><span class="sxs-lookup"><span data-stu-id="c3f83-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3f83-129"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c3f83-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3f83-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c3f83-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3f83-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3f83-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c3f83-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3f83-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f83-133">**CIM \_ -Auflistung**</span><span class="sxs-lookup"><span data-stu-id="c3f83-133">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

