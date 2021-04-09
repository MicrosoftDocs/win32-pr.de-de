---
description: Enthält eine Zusammenfassung der Informationen zum angegebenen virtuellen Computersystem.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Msvm_ComputerSystemSummaryInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862652"
---
# <a name="msvm_computersystemsummaryinformation-class"></a><span data-ttu-id="101c4-103">MSVM \_ computersystemsummaryinformation-Klasse</span><span class="sxs-lookup"><span data-stu-id="101c4-103">Msvm\_ComputerSystemSummaryInformation class</span></span>

<span data-ttu-id="101c4-104">Enthält eine Zusammenfassung der Informationen zum angegebenen virtuellen Computersystem.</span><span class="sxs-lookup"><span data-stu-id="101c4-104">Contains an information summary about the specified virtual computer system.</span></span>

<span data-ttu-id="101c4-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="101c4-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="101c4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="101c4-106">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="101c4-107">Member</span><span class="sxs-lookup"><span data-stu-id="101c4-107">Members</span></span>

<span data-ttu-id="101c4-108">Die **MSVM \_ computersystemsummaryinformation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="101c4-108">The **Msvm\_ComputerSystemSummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="101c4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="101c4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="101c4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="101c4-110">Properties</span></span>

<span data-ttu-id="101c4-111">Die **MSVM \_ computersystemsummaryinformation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="101c4-111">The **Msvm\_ComputerSystemSummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="101c4-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="101c4-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="101c4-113">Datentyp: **CIM \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="101c4-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="101c4-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="101c4-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="101c4-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="101c4-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="101c4-116">Ein [**CIM \_ Computersystem**](cim-computersystem.md) -Objekt, bei dem es sich um eine Instanz in der normalisierten Darstellung der verwalteten Ressource handelt.</span><span class="sxs-lookup"><span data-stu-id="101c4-116">A [**CIM\_ComputerSystem**](cim-computersystem.md) object that is an instance in the normalized representation of the managed resource.</span></span>

> [!Note]
>
> <span data-ttu-id="101c4-117">DataType, aktualisiert von [**MSVM \_ Computersystem**](msvm-computersystem.md) in Windows 10, Version 1703.</span><span class="sxs-lookup"><span data-stu-id="101c4-117">Datatype upgraded from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="101c4-118">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="101c4-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="101c4-119">Datentyp: **MSVM \_ summaryinformationbase**</span><span class="sxs-lookup"><span data-stu-id="101c4-119">Data type: **Msvm\_SummaryInformationBase**</span></span>
</dt> <dt>

<span data-ttu-id="101c4-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="101c4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="101c4-121">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="101c4-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="101c4-122">Eine Instanz von [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , die eine entnormalisierte oder aggregierte Ansicht der verwalteten Ressource darstellt, die durch das [**MSVM \_ Computersystem**](msvm-computersystem.md) dargestellt wird, auf das von der Vorgänger Eigenschaft verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="101c4-122">An instance of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) that represents a de-normalized or aggregate view of the managed resource that is represented by the [**Msvm\_ComputerSystem**](msvm-computersystem.md) referenced by the Antecedent property.</span></span>

> [!Note]
>
> <span data-ttu-id="101c4-123">DataType wurde aus [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) in Windows 10, Version 1703, aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="101c4-123">Datatype updated from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) in Windows 10, version 1703.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="101c4-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="101c4-124">Requirements</span></span>



| <span data-ttu-id="101c4-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="101c4-125">Requirement</span></span> | <span data-ttu-id="101c4-126">Wert</span><span class="sxs-lookup"><span data-stu-id="101c4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="101c4-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="101c4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="101c4-128">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="101c4-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="101c4-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="101c4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="101c4-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="101c4-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="101c4-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="101c4-131">Namespace</span></span><br/>                | <span data-ttu-id="101c4-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="101c4-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="101c4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="101c4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="101c4-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="101c4-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="101c4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="101c4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="101c4-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="101c4-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="101c4-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="101c4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101c4-138">**CIM- \_ Element Ansicht**</span><span class="sxs-lookup"><span data-stu-id="101c4-138">**CIM\_ElementView**</span></span>](cim-elementview.md)
</dt> </dl>

 

