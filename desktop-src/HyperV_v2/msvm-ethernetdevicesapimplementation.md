---
description: Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt und dem logischen Gerät dar, von dem es implementiert wird.
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Msvm_EthernetDeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 96290eb0d572f4848fbf3805a44ce0ae173892c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345788"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a><span data-ttu-id="237f1-103">MSVM- \_ Klasse "ethernetdevicesapimplementation"</span><span class="sxs-lookup"><span data-stu-id="237f1-103">Msvm\_EthernetDeviceSAPImplementation class</span></span>

<span data-ttu-id="237f1-104">Stellt eine Zuordnung zwischen einem Dienst Zugriffspunkt und dem logischen Gerät dar, von dem es implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="237f1-104">Represents an association between a service access point and the logical device that implements it.</span></span> <span data-ttu-id="237f1-105">Die Kardinalität dieser Zuordnung ist m:n.</span><span class="sxs-lookup"><span data-stu-id="237f1-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="237f1-106">Ein Dienst Zugriffspunkt (SAP) kann von mehreren logischen Geräten bereitgestellt werden, die zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="237f1-106">A service access point (SAP) can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="237f1-107">Jedes Gerät kann mehr als ein SAP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="237f1-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="237f1-108">Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammenarbeiten, um den Zugriffspunkt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="237f1-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="237f1-109">Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts.</span><span class="sxs-lookup"><span data-stu-id="237f1-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="237f1-110">Diese einzelnen Instanziierungen haben dann Zuordnungen zu den eindeutigen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="237f1-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="237f1-111">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="237f1-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="237f1-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="237f1-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="237f1-113">Member</span><span class="sxs-lookup"><span data-stu-id="237f1-113">Members</span></span>

<span data-ttu-id="237f1-114">Die **MSVM-Klasse " \_ ethernetdevicesapimplementation** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="237f1-114">The **Msvm\_EthernetDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="237f1-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="237f1-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="237f1-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="237f1-116">Properties</span></span>

<span data-ttu-id="237f1-117">Die **MSVM-Klasse " \_ ethernetdevicesapimplementation** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="237f1-117">The **Msvm\_EthernetDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="237f1-118">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="237f1-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237f1-119">Datentyp: **[ **CIM \_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span><span class="sxs-lookup"><span data-stu-id="237f1-119">Data type: **[**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**</span></span>
</dt> <dt>

<span data-ttu-id="237f1-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="237f1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237f1-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="237f1-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="237f1-122">Ein Verweis auf eine vom CIM- [**\_ Ethernetport**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) abgeleitete Klasse, die das logische Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="237f1-122">A reference to a class derived from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="237f1-123">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="237f1-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237f1-124">Datentyp: **[ **MSVM \_ lanendpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="237f1-124">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="237f1-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="237f1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237f1-126">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="237f1-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="237f1-127">Ein Verweis auf eine Instanz der [**MSVM \_ lanendpoint**](msvm-lanendpoint.md) -Klasse, die den SAP darstellt, der den **Vorgänger** verwendet.</span><span class="sxs-lookup"><span data-stu-id="237f1-127">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the SAP that is using the **Antecedent**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="237f1-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="237f1-128">Requirements</span></span>



| <span data-ttu-id="237f1-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="237f1-129">Requirement</span></span> | <span data-ttu-id="237f1-130">Wert</span><span class="sxs-lookup"><span data-stu-id="237f1-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="237f1-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="237f1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="237f1-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="237f1-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="237f1-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="237f1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="237f1-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="237f1-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="237f1-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="237f1-135">Namespace</span></span><br/>                | <span data-ttu-id="237f1-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="237f1-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="237f1-137">MOF</span><span class="sxs-lookup"><span data-stu-id="237f1-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="237f1-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="237f1-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="237f1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="237f1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="237f1-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="237f1-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

