---
description: Eine Zuordnung zwischen einer Instanz von MSVM \_ vsscomponent und einer Instanz von MSVM \_ VssService, die einen Dienst zum Ausführen von Vorgängen für die VSS-Komponente darstellt.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Msvm_ServiceOfVssComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5787dcdd4d8ce1aeefdc1fbafb2c156aec4d467a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349506"
---
# <a name="msvm_serviceofvsscomponent-class"></a><span data-ttu-id="5fd16-103">MSVM \_ serviceofvsscomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="5fd16-103">Msvm\_ServiceOfVssComponent class</span></span>

<span data-ttu-id="5fd16-104">Eine Zuordnung zwischen einer Instanz von [**MSVM \_ vsscomponent**](msvm-vsscomponent.md) und einer Instanz von [**MSVM \_ VssService**](msvm-vssservice.md) , die einen Dienst zum Ausführen von Vorgängen für die VSS-Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="5fd16-104">An association between an instance of [**Msvm\_VssComponent**](msvm-vsscomponent.md) and an instance of [**Msvm\_VssService**](msvm-vssservice.md) that represents a service for performing operations on the VSS component.</span></span>

<span data-ttu-id="5fd16-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5fd16-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd16-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fd16-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5fd16-107">Member</span><span class="sxs-lookup"><span data-stu-id="5fd16-107">Members</span></span>

<span data-ttu-id="5fd16-108">Die **MSVM \_ serviceofvsscomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5fd16-108">The **Msvm\_ServiceOfVssComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="5fd16-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fd16-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fd16-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5fd16-110">Properties</span></span>

<span data-ttu-id="5fd16-111">Die **MSVM \_ serviceofvsscomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5fd16-111">The **Msvm\_ServiceOfVssComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fd16-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="5fd16-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fd16-113">Datentyp: **MSVM \_ vsscomponent**</span><span class="sxs-lookup"><span data-stu-id="5fd16-113">Data type: **Msvm\_VssComponent**</span></span>
</dt> <dt>

<span data-ttu-id="5fd16-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fd16-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fd16-115">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="5fd16-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5fd16-116">Ein, [**MSVM \_ vsscomponent**](msvm-vsscomponent.md) , das die VSS-Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="5fd16-116">A, [**Msvm\_VssComponent**](msvm-vsscomponent.md) that represents the VSS component.</span></span>

</dd> <dt>

<span data-ttu-id="5fd16-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="5fd16-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fd16-118">Datentyp: **MSVM \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="5fd16-118">Data type: **Msvm\_VssService**</span></span>
</dt> <dt>

<span data-ttu-id="5fd16-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5fd16-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fd16-120">Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM- \_ Abhängigkeit. abhängig")</span><span class="sxs-lookup"><span data-stu-id="5fd16-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_Dependency.Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5fd16-121">Ein [**MSVM- \_ VssService**](msvm-vssservice.md) , der den VSS-IC-Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="5fd16-121">An [**Msvm\_VssService**](msvm-vssservice.md) that represents the VSS IC service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fd16-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5fd16-122">Requirements</span></span>



| <span data-ttu-id="5fd16-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5fd16-123">Requirement</span></span> | <span data-ttu-id="5fd16-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5fd16-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd16-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5fd16-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd16-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5fd16-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5fd16-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5fd16-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd16-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5fd16-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5fd16-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fd16-129">Namespace</span></span><br/>                | <span data-ttu-id="5fd16-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5fd16-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5fd16-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5fd16-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fd16-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5fd16-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fd16-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5fd16-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fd16-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fd16-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5fd16-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fd16-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd16-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="5fd16-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

