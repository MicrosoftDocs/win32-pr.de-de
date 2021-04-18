---
description: Diese Klasse ist veraltet. Stattdessen wird die Ableitung von der CIM- \_ Dienstklasse empfohlen.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: CIM_NetworkService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352513"
---
# <a name="cim_networkservice-class"></a><span data-ttu-id="14f9b-104">CIM- \_ NetworkService-Klasse</span><span class="sxs-lookup"><span data-stu-id="14f9b-104">CIM\_NetworkService class</span></span>

<span data-ttu-id="14f9b-105">Diese Klasse ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="14f9b-105">This class is deprecated.</span></span> <span data-ttu-id="14f9b-106">Stattdessen wird die Ableitung von der [**CIM- \_ Dienst**](cim-service.md) Klasse empfohlen.</span><span class="sxs-lookup"><span data-stu-id="14f9b-106">Instead, we recommend deriving from the [**CIM\_Service**](cim-service.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f9b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="14f9b-107">Syntax</span></span>

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a><span data-ttu-id="14f9b-108">Member</span><span class="sxs-lookup"><span data-stu-id="14f9b-108">Members</span></span>

<span data-ttu-id="14f9b-109">Die **CIM- \_ NetworkService** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="14f9b-109">The **CIM\_NetworkService** class has these types of members:</span></span>

-   [<span data-ttu-id="14f9b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14f9b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14f9b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="14f9b-111">Properties</span></span>

<span data-ttu-id="14f9b-112">Die **CIM- \_ NetworkService** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="14f9b-112">The **CIM\_NetworkService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14f9b-113">**Schlüsselwörter**</span><span class="sxs-lookup"><span data-stu-id="14f9b-113">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f9b-114">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="14f9b-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="14f9b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14f9b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f9b-116">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")</span><span class="sxs-lookup"><span data-stu-id="14f9b-116">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="14f9b-117">Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14f9b-117">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="14f9b-118">Veraltete Beschreibung: ein Array von Schlüsselwörtern, die in Abfragen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="14f9b-118">Deprecated description: An array of keywords that can be used in queries.</span></span>

 

</dd> <dt>

<span data-ttu-id="14f9b-119">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="14f9b-119">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f9b-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="14f9b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14f9b-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14f9b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f9b-122">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ serviceaccessuri")</span><span class="sxs-lookup"><span data-stu-id="14f9b-122">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_ServiceAccessURI")</span></span>
</dt> </dl>

<span data-ttu-id="14f9b-123">Diese Eigenschaft ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="14f9b-123">This property is deprecated.</span></span> <span data-ttu-id="14f9b-124">Stattdessen wird die **CIM \_ serviceaccessuri** -Klasse empfohlen.</span><span class="sxs-lookup"><span data-stu-id="14f9b-124">Instead, we recommend the **CIM\_ServiceAccessURI** class.</span></span>

> [!Note]  
> <span data-ttu-id="14f9b-125">Veraltete Beschreibung: eine URL, die das Protokoll, den Netzwerk Speicherort und andere Dienst spezifische Informationen bereitstellt, die erforderlich sind, um auf den Dienst zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="14f9b-125">Deprecated description: A URL that provides the protocol, network location, and other service-specific information required in order to access the service.</span></span>

 

</dd> <dt>

<span data-ttu-id="14f9b-126">**Startupconditions**</span><span class="sxs-lookup"><span data-stu-id="14f9b-126">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f9b-127">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="14f9b-127">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="14f9b-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14f9b-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f9b-129">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")</span><span class="sxs-lookup"><span data-stu-id="14f9b-129">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="14f9b-130">Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14f9b-130">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="14f9b-131">Veraltete Beschreibung: die Voraussetzungen, die erfüllt sein müssen, damit dieser Dienst ordnungsgemäß gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="14f9b-131">Deprecated description: The pre-conditions that must be met in order for this service to start correctly.</span></span>

 

</dd> <dt>

<span data-ttu-id="14f9b-132">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="14f9b-132">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14f9b-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="14f9b-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="14f9b-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="14f9b-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14f9b-135">Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")</span><span class="sxs-lookup"><span data-stu-id="14f9b-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="14f9b-136">Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14f9b-136">This property is deprecated and should not be used.</span></span>

> [!Note]  
> <span data-ttu-id="14f9b-137">Deprecated Description: die Parameter, die für die **Start Service** -Methode bereitgestellt werden müssen, damit dieser Dienst ordnungsgemäß gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="14f9b-137">Deprecated description: The parameters that must be supplied to the **StartService** method in order for this service to start correctly.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14f9b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14f9b-138">Requirements</span></span>



| <span data-ttu-id="14f9b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14f9b-139">Requirement</span></span> | <span data-ttu-id="14f9b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="14f9b-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14f9b-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14f9b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="14f9b-142">Windows 8</span><span class="sxs-lookup"><span data-stu-id="14f9b-142">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="14f9b-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14f9b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="14f9b-144">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14f9b-144">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="14f9b-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="14f9b-145">Namespace</span></span><br/>                | <span data-ttu-id="14f9b-146">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="14f9b-146">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14f9b-147">MOF</span><span class="sxs-lookup"><span data-stu-id="14f9b-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14f9b-148"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="14f9b-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14f9b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="14f9b-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14f9b-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14f9b-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14f9b-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14f9b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f9b-152">**CIM- \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="14f9b-152">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

