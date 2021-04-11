---
description: Fungiert als übergeordnete Klasse für Registrierungs Klassen für verschiedene Typen von Anbietern.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: __ProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131772"
---
# <a name="__providerregistration-class"></a><span data-ttu-id="2df41-103">\_\_Providerregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="2df41-103">\_\_ProviderRegistration class</span></span>

<span data-ttu-id="2df41-104">Die abstrakte System Klasse **\_ \_ providerregistration** fungiert als übergeordnete Klasse für Registrierungs Klassen für verschiedene Typen von Anbietern.</span><span class="sxs-lookup"><span data-stu-id="2df41-104">The **\_\_ProviderRegistration** abstract system class serves as the parent class for registration classes for various types of providers.</span></span>

<span data-ttu-id="2df41-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2df41-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2df41-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2df41-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2df41-107">Syntax</span></span>

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="2df41-108">Member</span><span class="sxs-lookup"><span data-stu-id="2df41-108">Members</span></span>

<span data-ttu-id="2df41-109">Die **\_ \_ providerregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2df41-109">The **\_\_ProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="2df41-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2df41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2df41-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2df41-111">Properties</span></span>

<span data-ttu-id="2df41-112">Die **\_ \_ providerregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2df41-112">The **\_\_ProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2df41-113">**ab**</span><span class="sxs-lookup"><span data-stu-id="2df41-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2df41-114">Datentyp: **\_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="2df41-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="2df41-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2df41-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2df41-116">Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die den Objekt Pfad zum Anbieter darstellt.</span><span class="sxs-lookup"><span data-stu-id="2df41-116">Reference to an instance of [**\_\_Provider**](--provider.md) representing the object path to the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2df41-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2df41-117">Remarks</span></span>

<span data-ttu-id="2df41-118">Die **\_ \_ providerregistration** -Klasse wird von [**\_ \_ systemclass**](--systemclass.md)abgeleitet, die keine Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="2df41-118">The **\_\_ProviderRegistration** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="2df41-119">Instanzen der **\_ \_ providerregistration** -System Klasse werden nie erstellt.</span><span class="sxs-lookup"><span data-stu-id="2df41-119">Instances of the **\_\_ProviderRegistration** system class are never created.</span></span> <span data-ttu-id="2df41-120">Die Klassen, die Anbieter zum Erstellen von Instanzen für die Registrierung verwenden, werden entweder direkt oder indirekt von dieser Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="2df41-120">The classes that providers use to create instances for registration derive either directly or indirectly from this class.</span></span> <span data-ttu-id="2df41-121">Diese Klassen sind:</span><span class="sxs-lookup"><span data-stu-id="2df41-121">These classes are:</span></span>

[<span data-ttu-id="2df41-122">**\_\_Classproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="2df41-122">**\_\_ClassProviderRegistration**</span></span>](--classproviderregistration.md)

[<span data-ttu-id="2df41-123">**\_\_Eventconsumerproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="2df41-123">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md)

[<span data-ttu-id="2df41-124">**\_\_Eventproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="2df41-124">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

[<span data-ttu-id="2df41-125">**\_\_Instanceproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="2df41-125">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

[<span data-ttu-id="2df41-126">**\_\_Methodproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="2df41-126">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

[<span data-ttu-id="2df41-127">**\_\_Objectproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="2df41-127">**\_\_ObjectProviderRegistration**</span></span>](--objectproviderregistration.md)

[<span data-ttu-id="2df41-128">**\_\_Propertyproviderregistration**</span><span class="sxs-lookup"><span data-stu-id="2df41-128">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

<span data-ttu-id="2df41-129">Nur Administratoren können einen Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) erstellen und registrieren.</span><span class="sxs-lookup"><span data-stu-id="2df41-129">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2df41-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2df41-130">Requirements</span></span>



| <span data-ttu-id="2df41-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2df41-131">Requirement</span></span> | <span data-ttu-id="2df41-132">Wert</span><span class="sxs-lookup"><span data-stu-id="2df41-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2df41-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2df41-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2df41-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2df41-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2df41-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2df41-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2df41-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2df41-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2df41-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="2df41-137">Namespace</span></span><br/>                | <span data-ttu-id="2df41-138">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="2df41-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2df41-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2df41-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df41-140">**\_\_System Class**</span><span class="sxs-lookup"><span data-stu-id="2df41-140">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="2df41-141">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="2df41-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2df41-142">Registrieren eines Anbieters</span><span class="sxs-lookup"><span data-stu-id="2df41-142">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

