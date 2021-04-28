---
description: 'Msvm_FcDeviceSAPImplementation-Klasse: Stellt eine Zuordnung zwischen einem Dienstzugriffspunkt und dem logischen Gerät dar, das ihn implementiert.'
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
ms.openlocfilehash: b0df7a198b3ee52d131800073f8be30d51d93181
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119028"
---
# <a name="msvm_fcdevicesapimplementation-class"></a><span data-ttu-id="f154f-103">Msvm \_ FcDeviceSAPImplementation-Klasse</span><span class="sxs-lookup"><span data-stu-id="f154f-103">Msvm\_FcDeviceSAPImplementation class</span></span>

<span data-ttu-id="f154f-104">Stellt eine Zuordnung zwischen einem Dienstzugriffspunkt und dem logischen Gerät dar, das ihn implementiert.</span><span class="sxs-lookup"><span data-stu-id="f154f-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="f154f-105">Die Kardinalität dieser Zuordnung ist m:n.</span><span class="sxs-lookup"><span data-stu-id="f154f-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="f154f-106">Ein Dienstzugriffspunkt (SAP) kann von mehreren logischen Geräten bereitgestellt werden, die in Verbindung stehen.</span><span class="sxs-lookup"><span data-stu-id="f154f-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="f154f-107">Jedes Gerät kann mehrere SAP-Geräte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f154f-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="f154f-108">Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammen ausgeführt werden, um den Zugriffspunkt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f154f-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="f154f-109">Wenn unterschiedliche Implementierungen eines SAP vorhanden sind, würde jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts führen.</span><span class="sxs-lookup"><span data-stu-id="f154f-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="f154f-110">Diese einzelnen Instanziierungen verfügen dann über Zuordnungen zu den eindeutigen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="f154f-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="f154f-111">Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f154f-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f154f-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="f154f-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f154f-113">Member</span><span class="sxs-lookup"><span data-stu-id="f154f-113">Members</span></span>

<span data-ttu-id="f154f-114">Die **Msvm \_ FcDeviceSAPImplementation-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f154f-114">The **Msvm\_FcDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="f154f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f154f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f154f-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f154f-116">Properties</span></span>

<span data-ttu-id="f154f-117">Die **Msvm \_ FcDeviceSAPImplementation-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f154f-117">The **Msvm\_FcDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f154f-118">**Vorläufer**</span><span class="sxs-lookup"><span data-stu-id="f154f-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f154f-119">Datentyp: **CIM \_ FCPort**</span><span class="sxs-lookup"><span data-stu-id="f154f-119">Data type: **CIM\_FCPort**</span></span>
</dt> <dt>

<span data-ttu-id="f154f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f154f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f154f-121">Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="f154f-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f154f-122">Ein Verweis auf eine von **CIM \_ FCPort** abgeleitete Klasse, die das logische Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="f154f-122">A reference to a class derived from **CIM\_FCPort** that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="f154f-123">**Abhängigen**</span><span class="sxs-lookup"><span data-stu-id="f154f-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f154f-124">Datentyp: **Msvm \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="f154f-124">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="f154f-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f154f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f154f-126">Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")</span><span class="sxs-lookup"><span data-stu-id="f154f-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f154f-127">Ein Verweis auf eine Instanz der [**Msvm \_ FcEndpoint-Klasse,**](msvm-fcendpoint.md) die den SAP darstellt, der die **-Instanz verwendet.**</span><span class="sxs-lookup"><span data-stu-id="f154f-127">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f154f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f154f-128">Requirements</span></span>



| <span data-ttu-id="f154f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f154f-129">Requirement</span></span> | <span data-ttu-id="f154f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="f154f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f154f-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f154f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f154f-132">Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f154f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f154f-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f154f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f154f-134">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f154f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f154f-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="f154f-135">Namespace</span></span><br/>                | <span data-ttu-id="f154f-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="f154f-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f154f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f154f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f154f-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f154f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f154f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f154f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f154f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f154f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

