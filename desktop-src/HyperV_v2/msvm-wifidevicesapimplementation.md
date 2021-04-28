---
description: 'Msvm_WiFiDeviceSAPImplementation-Klasse: Eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung.'
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
ms.openlocfilehash: 99826ce3a37e19867cef1a6ddf276f5136b21a3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109248"
---
# <a name="msvm_wifidevicesapimplementation-class"></a><span data-ttu-id="3bbed-103">Msvm \_ WiFiDeviceSAPImplementation-Klasse</span><span class="sxs-lookup"><span data-stu-id="3bbed-103">Msvm\_WiFiDeviceSAPImplementation class</span></span>

<span data-ttu-id="3bbed-104">Eine Zuordnung zwischen einem Dienstzugriffspunkt (SAP) und seiner Implementierung.</span><span class="sxs-lookup"><span data-stu-id="3bbed-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="3bbed-105">Die Kardinalität dieser Zuordnung ist m:n.</span><span class="sxs-lookup"><span data-stu-id="3bbed-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="3bbed-106">Ein SAP kann von mehreren logischen Geräten bereitgestellt werden, die in Verbindung stehen.</span><span class="sxs-lookup"><span data-stu-id="3bbed-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="3bbed-107">Jedes Gerät kann mehrere SAP-Geräte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3bbed-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="3bbed-108">Wenn viele logische Geräte einem einzelnen SAP zugeordnet sind, wird davon ausgegangen, dass diese Elemente zusammen ausgeführt werden, um den Zugriffspunkt bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3bbed-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="3bbed-109">Wenn unterschiedliche Implementierungen eines SAP vorhanden sind, würde jede dieser Implementierungen zu einzelnen Instanziierungen des SAP-Objekts führen.</span><span class="sxs-lookup"><span data-stu-id="3bbed-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="3bbed-110">Diese einzelnen Instanziierungen verfügen dann über Zuordnungen zu den eindeutigen Implementierungen.</span><span class="sxs-lookup"><span data-stu-id="3bbed-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="3bbed-111">Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3bbed-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbed-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bbed-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3bbed-113">Member</span><span class="sxs-lookup"><span data-stu-id="3bbed-113">Members</span></span>

<span data-ttu-id="3bbed-114">Die **Msvm \_ WiFiDeviceSAPImplementation-Klasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3bbed-114">The **Msvm\_WiFiDeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="3bbed-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bbed-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3bbed-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3bbed-116">Properties</span></span>

<span data-ttu-id="3bbed-117">Die **Msvm \_ WiFiDeviceSAPImplementation-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3bbed-117">The **Msvm\_WiFiDeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3bbed-118">**Vorläufer**</span><span class="sxs-lookup"><span data-stu-id="3bbed-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bbed-119">Datentyp: **[ **Msvm \_ WiFiPort**](msvm-wifiport.md)**</span><span class="sxs-lookup"><span data-stu-id="3bbed-119">Data type: **[**Msvm\_WiFiPort**](msvm-wifiport.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3bbed-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3bbed-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bbed-121">Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="3bbed-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3bbed-122">Eine Instanz der [**Msvm \_ WiFiPort-Klasse,**](msvm-wifiport.md) die das logische Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="3bbed-122">An instance of the [**Msvm\_WiFiPort**](msvm-wifiport.md) class that represents the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="3bbed-123">**Abhängigen**</span><span class="sxs-lookup"><span data-stu-id="3bbed-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bbed-124">Datentyp: **[ **Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="3bbed-124">Data type: **[**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3bbed-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3bbed-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bbed-126">Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")</span><span class="sxs-lookup"><span data-stu-id="3bbed-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3bbed-127">Eine Instanz der [**Msvm \_ WiFiEndpoint-Klasse,**](msvm-wifiendpoint.md) die den dienstzugriffspunkt darstellt, der mit dem logischen Gerät implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3bbed-127">An instance of the [**Msvm\_WiFiEndpoint**](msvm-wifiendpoint.md) class that represents the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bbed-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bbed-128">Requirements</span></span>



| <span data-ttu-id="3bbed-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bbed-129">Requirement</span></span> | <span data-ttu-id="3bbed-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3bbed-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbed-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bbed-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3bbed-132">Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bbed-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3bbed-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bbed-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3bbed-134">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bbed-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3bbed-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="3bbed-135">Namespace</span></span><br/>                | <span data-ttu-id="3bbed-136">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="3bbed-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3bbed-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3bbed-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bbed-138"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bbed-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bbed-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3bbed-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bbed-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3bbed-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

