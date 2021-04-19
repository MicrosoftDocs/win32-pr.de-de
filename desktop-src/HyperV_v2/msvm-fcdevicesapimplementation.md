---
description: Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt und dem logischen Gerät dar, von dem es implementiert wird.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Msvm_FcDeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc40f25e3b288155e713415aa512d629b538d1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355504"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="5078f-103">MSVM \_ fcdevicesapimplementation-Klasse</span><span class="sxs-lookup"><span data-stu-id="5078f-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="5078f-104">Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt und dem logischen Gerät dar, von dem es implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="5078f-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="5078f-105">Die Kardinalität dieser Zuordnung ist m:n.</span><span class="sxs-lookup"><span data-stu-id="5078f-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="5078f-106">Ein Dienst Zugriffspunkt (SAP) kann von mehreren logischen Geräten bereitgestellt werden, die zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5078f-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="5078f-107">Jedes Gerät kann mehr als ein SAP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5078f-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="5078f-108">Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammenarbeiten, um den Zugriffspunkt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5078f-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="5078f-109">Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts.</span><span class="sxs-lookup"><span data-stu-id="5078f-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="5078f-110">Diese einzelnen Instanziierungen haben dann Zuordnungen zu den eindeutigen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="5078f-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="5078f-111">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5078f-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5078f-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="5078f-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="5078f-113">Member</span><span class="sxs-lookup"><span data-stu-id="5078f-113">Members</span></span>

<span data-ttu-id="5078f-114">Die **MSVM \_ fcdevicesapimplementation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5078f-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="5078f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5078f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5078f-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5078f-116">Properties</span></span>

<span data-ttu-id="5078f-117">Die **MSVM \_ fcdevicesapimplementation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5078f-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5078f-118">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="5078f-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5078f-119">Datentyp: **CIM \_ fcport**</span><span class="sxs-lookup"><span data-stu-id="5078f-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="5078f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5078f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5078f-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="5078f-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5078f-122">Ein Verweis auf eine von **CIM \_ fcport** abgeleitete Klasse, die das logische Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="5078f-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="5078f-123">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="5078f-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5078f-124">Datentyp: **MSVM \_ fcendpoint**</span><span class="sxs-lookup"><span data-stu-id="5078f-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="5078f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5078f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5078f-126">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="5078f-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5078f-127">Ein Verweis auf eine Instanz der [**MSVM \_ fcendpoint**](msvm-fcendpoint.md) -Klasse, die den SAP darstellt, der den **Vorgänger** verwendet.</span><span class="sxs-lookup"><span data-stu-id="5078f-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5078f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5078f-128">Requirements</span></span>



| <span data-ttu-id="5078f-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5078f-129">Requirement</span></span> | <span data-ttu-id="5078f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5078f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5078f-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5078f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5078f-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5078f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5078f-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5078f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5078f-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5078f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5078f-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="5078f-135">Namespace</span></span><br/>                | <span data-ttu-id="5078f-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5078f-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5078f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="5078f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5078f-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5078f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5078f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5078f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5078f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5078f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

