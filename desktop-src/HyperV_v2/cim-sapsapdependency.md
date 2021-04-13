---
description: Stellt eine Zuordnung zwischen zwei Dienst Zugriffs Punkten (SAP) dar, bei der ein SAP vom anderen abhängig ist, um einen Dienst zu verwenden oder mit diesem zu verbinden.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: CIM_SAPSAPDependency-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6888cbb74ea03b85bc9abfcea24e65660fd65953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526780"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a><span data-ttu-id="9e2b6-103">CIM_SAPSAPDependency-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="9e2b6-103">CIM_SAPSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="9e2b6-104">Stellt eine Zuordnung zwischen zwei Dienst Zugriffs Punkten (SAP) dar, bei der ein SAP vom anderen abhängig ist, um einen Dienst zu verwenden oder mit diesem zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="9e2b6-104">Represents an association between two service access points (SAP), in which one SAP is dependant on the other to utilize or connect with a service.</span></span> <span data-ttu-id="9e2b6-105">Um z. b. auf einem Netzwerkdrucker zu drucken, müssen lokale Druck Zugriffspunkte zugrunde liegende netzwerkbezogene SAPS verwenden, um die Druck Anforderung zu senden.</span><span class="sxs-lookup"><span data-stu-id="9e2b6-105">For example, to print on a network printer, local print access points must utilize underlying network-related SAPs to send the print request.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e2b6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e2b6-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9e2b6-107">Member</span><span class="sxs-lookup"><span data-stu-id="9e2b6-107">Members</span></span>

<span data-ttu-id="9e2b6-108">Die **CIM \_ sapsapdepenpklasse** verfügt über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9e2b6-108">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="9e2b6-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e2b6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e2b6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e2b6-110">Properties</span></span>

<span data-ttu-id="9e2b6-111">Die **CIM \_ sapsapdepenpklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9e2b6-111">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e2b6-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="9e2b6-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e2b6-113">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="9e2b6-113">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="9e2b6-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e2b6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e2b6-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="9e2b6-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9e2b6-116">Ein Verweis auf das erforderliche SAP.</span><span class="sxs-lookup"><span data-stu-id="9e2b6-116">A reference to the required SAP.</span></span>

</dd> <dt>

<span data-ttu-id="9e2b6-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="9e2b6-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e2b6-118">Datentyp: **CIM \_ serviceaccesspoint**</span><span class="sxs-lookup"><span data-stu-id="9e2b6-118">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="9e2b6-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e2b6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e2b6-120">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="9e2b6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9e2b6-121">Ein Verweis auf den abhängigen SAP.</span><span class="sxs-lookup"><span data-stu-id="9e2b6-121">A reference to the dependant SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e2b6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e2b6-122">Requirements</span></span>



| <span data-ttu-id="9e2b6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e2b6-123">Requirement</span></span> | <span data-ttu-id="9e2b6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9e2b6-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2b6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e2b6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9e2b6-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9e2b6-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="9e2b6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e2b6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9e2b6-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e2b6-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="9e2b6-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e2b6-129">Namespace</span></span><br/>                | <span data-ttu-id="9e2b6-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9e2b6-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9e2b6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9e2b6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e2b6-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9e2b6-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e2b6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9e2b6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e2b6-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e2b6-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9e2b6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e2b6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e2b6-136">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="9e2b6-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

