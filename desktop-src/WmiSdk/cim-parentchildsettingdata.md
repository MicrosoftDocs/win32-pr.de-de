---
description: Eine Zuordnung zwischen einer Instanz von CIM \_ virtualsystemsettingdata und der CIM \_ virtualsystemsettingdata-Instanz, die die aktuelle Momentaufnahme darstellt, auf der dieses Objekt basiert.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: CIM_ParentChildSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 9b2b866c3d5ae15d3f5a97c971e8efec75e9164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359628"
---
# <a name="cim_parentchildsettingdata-class"></a><span data-ttu-id="b9837-103">CIM- \_ parametrientchildsettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="b9837-103">CIM\_ParentChildSettingData class</span></span>

<span data-ttu-id="b9837-104">Eine Zuordnung zwischen einer Instanz von [**CIM \_ virtualsystemsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) und der **CIM \_ virtualsystemsettingdata** -Instanz, die die aktuelle Momentaufnahme darstellt, auf der dieses Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="b9837-104">An association between an instance of [**CIM\_VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) and the **CIM\_VirtualSystemSettingData** instance which represents the most recent snapshot upon which this object is based.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9837-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b9837-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b9837-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b9837-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b9837-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9837-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9837-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9837-108">Syntax</span></span>

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a><span data-ttu-id="b9837-109">Member</span><span class="sxs-lookup"><span data-stu-id="b9837-109">Members</span></span>

<span data-ttu-id="b9837-110">Die CIM-Klasse " **\_ Parser-childsettingdata** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b9837-110">The **CIM\_ParentChildSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b9837-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9837-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9837-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9837-112">Properties</span></span>

<span data-ttu-id="b9837-113">Die CIM-Klasse " **\_ Parser-childsettingdata** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9837-113">The **CIM\_ParentChildSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9837-114">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="b9837-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9837-115">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="b9837-115">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b9837-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9837-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9837-117">Verweis auf das unabhängige Objekt in dieser Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="b9837-117">Reference to the independent object in this association.</span></span>

<span data-ttu-id="b9837-118">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9837-118">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="b9837-119">**Untergeordnet**</span><span class="sxs-lookup"><span data-stu-id="b9837-119">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9837-120">Datentyp: **CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="b9837-120">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="b9837-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9837-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9837-122">Die Einstellungsdaten für das virtuelle System, das das untergeordnete Element des übergeordneten Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9837-122">The setting data for the virtual system which represents the child of the Parent.</span></span>

</dd> <dt>

<span data-ttu-id="b9837-123">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="b9837-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9837-124">Datentyp: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="b9837-124">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b9837-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9837-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9837-126">Verweis auf das Objekt, das von der **Vorgänger** Eigenschaft abhängt.</span><span class="sxs-lookup"><span data-stu-id="b9837-126">Reference to the object that is dependent on the **Antecedent** property.</span></span>

<span data-ttu-id="b9837-127">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9837-127">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="b9837-128">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b9837-128">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9837-129">Datentyp: **CIM \_ virtualsystemsettingdata**</span><span class="sxs-lookup"><span data-stu-id="b9837-129">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="b9837-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9837-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9837-131">Die Momentaufnahme Einstellungsdaten, auf denen die Daten der untergeordneten Einstellung basieren.</span><span class="sxs-lookup"><span data-stu-id="b9837-131">The snapshot setting data upon which the Child setting data is based.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9837-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9837-132">Requirements</span></span>



| <span data-ttu-id="b9837-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9837-133">Requirement</span></span> | <span data-ttu-id="b9837-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b9837-134">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="b9837-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9837-135">Namespace</span></span><br/> | <span data-ttu-id="b9837-136">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b9837-136">Root\\CIMV2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9837-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9837-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9837-138">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="b9837-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

