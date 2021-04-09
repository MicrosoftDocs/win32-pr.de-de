---
description: Eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und seiner Implementierung.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Msvm_WiFiDeviceSAPImplementation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debec96efb93e60ec18d75b62ffa0d13b0e0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862463"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="85930-103">MSVM- \_ wifidevicesapimplementation-Klasse</span><span class="sxs-lookup"><span data-stu-id="85930-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="85930-104">Eine Zuordnung zwischen einem Dienst Zugriffspunkt (SAP) und seiner Implementierung.</span><span class="sxs-lookup"><span data-stu-id="85930-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="85930-105">Die Kardinalität dieser Zuordnung ist m:n.</span><span class="sxs-lookup"><span data-stu-id="85930-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="85930-106">Ein SAP kann von mehreren logischen Geräten bereitgestellt werden, die zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="85930-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="85930-107">Jedes Gerät kann mehr als ein SAP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="85930-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="85930-108">Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammenarbeiten, um den Zugriffspunkt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="85930-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="85930-109">Wenn verschiedene Implementierungen eines SAP vorhanden sind, führt jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts.</span><span class="sxs-lookup"><span data-stu-id="85930-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="85930-110">Diese einzelnen Instanziierungen haben dann Zuordnungen zu den eindeutigen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="85930-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="85930-111">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85930-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="85930-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="85930-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="85930-113">Member</span><span class="sxs-lookup"><span data-stu-id="85930-113">Members</span></span>

<span data-ttu-id="85930-114">Die **MSVM \_ wifidevicesapimplementation** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="85930-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="85930-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85930-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85930-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85930-116">Properties</span></span>

<span data-ttu-id="85930-117">Die **MSVM \_ wifidevicesapimplementation** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85930-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85930-118">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="85930-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85930-119">Datentyp: **[ **MSVM- \_ wifiport**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="85930-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="85930-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85930-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85930-121">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="85930-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="85930-122">Eine Instanz der [**MSVM- \_ wifiport**](msvm-wifiport.md) -Klasse, die das logische Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="85930-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="85930-123">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="85930-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85930-124">Datentyp: **[ **MSVM \_ wifiendpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="85930-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="85930-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="85930-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85930-126">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="85930-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="85930-127">Eine Instanz der [**MSVM \_ wifiendpoint**](msvm-wifiendpoint.md) -Klasse, die den mithilfe des logischen Geräts implementierten Dienst Zugriffspunkt darstellt.</span><span class="sxs-lookup"><span data-stu-id="85930-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85930-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85930-128">Requirements</span></span>



| <span data-ttu-id="85930-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85930-129">Requirement</span></span> | <span data-ttu-id="85930-130">Wert</span><span class="sxs-lookup"><span data-stu-id="85930-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85930-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85930-131">Minimum supported client</span></span><br/> | <span data-ttu-id="85930-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85930-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="85930-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85930-133">Minimum supported server</span></span><br/> | <span data-ttu-id="85930-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85930-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="85930-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="85930-135">Namespace</span></span><br/>                | <span data-ttu-id="85930-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="85930-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="85930-137">MOF</span><span class="sxs-lookup"><span data-stu-id="85930-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85930-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="85930-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85930-139">DLL</span><span class="sxs-lookup"><span data-stu-id="85930-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85930-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85930-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

