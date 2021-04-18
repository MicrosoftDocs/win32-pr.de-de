---
description: Wird zum Registrieren von Ereignis Anbietern bei Windows-Verwaltungsinstrumentation (WMI) verwendet.
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: __EventProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347682"
---
# <a name="__eventproviderregistration-class"></a><span data-ttu-id="f5883-103">\_\_Eventproviderregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="f5883-103">\_\_EventProviderRegistration class</span></span>

<span data-ttu-id="f5883-104">Die **\_ \_ eventproviderregistration** -System Klasse wird zum Registrieren von Ereignis Anbietern bei Windows-Verwaltungsinstrumentation (WMI) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5883-104">The **\_\_EventProviderRegistration** system class is used to register event providers with Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="f5883-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f5883-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f5883-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f5883-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5883-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5883-107">Syntax</span></span>

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="f5883-108">Member</span><span class="sxs-lookup"><span data-stu-id="f5883-108">Members</span></span>

<span data-ttu-id="f5883-109">Die **\_ \_ eventproviderregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f5883-109">The **\_\_EventProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="f5883-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5883-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5883-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5883-111">Properties</span></span>

<span data-ttu-id="f5883-112">Die **\_ \_ eventproviderregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f5883-112">The **\_\_EventProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5883-113">**EventQueryList**</span><span class="sxs-lookup"><span data-stu-id="f5883-113">**EventQueryList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5883-114">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f5883-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f5883-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f5883-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f5883-116">Eine oder mehrere WQL-Abfragen (Windows-Verwaltungsinstrumentation Query Language), die die Ereignisse beschreiben, die vom Ereignis Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f5883-116">One or more Windows Management Instrumentation Query Language (WQL) queries that describe the events that the event provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="f5883-117">**ab**</span><span class="sxs-lookup"><span data-stu-id="f5883-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5883-118">Datentyp: **\_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="f5883-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="f5883-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f5883-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5883-120">Objekt Pfad zum Ereignis Anbieter.</span><span class="sxs-lookup"><span data-stu-id="f5883-120">Object path to the event provider.</span></span> <span data-ttu-id="f5883-121">Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="f5883-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5883-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5883-122">Remarks</span></span>

<span data-ttu-id="f5883-123">Nur Administratoren können einen Ereignis Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und [**\_ \_ eventproviderregistration**](--eventconsumerproviderregistration.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="f5883-123">Only administrators can register or delete an event provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="f5883-124">Die **\_ \_ eventproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="f5883-124">The **\_\_EventProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5883-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5883-125">Requirements</span></span>



| <span data-ttu-id="f5883-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5883-126">Requirement</span></span> | <span data-ttu-id="f5883-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f5883-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f5883-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5883-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f5883-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5883-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f5883-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5883-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f5883-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5883-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f5883-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5883-132">Namespace</span></span><br/>                | <span data-ttu-id="f5883-133">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="f5883-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f5883-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5883-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5883-135">**\_\_Providerregistration**</span><span class="sxs-lookup"><span data-stu-id="f5883-135">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="f5883-136">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="f5883-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f5883-137">Registrieren eines Ereignis Anbieters</span><span class="sxs-lookup"><span data-stu-id="f5883-137">Registering an Event Provider</span></span>](registering-an-event-provider.md)
</dt> <dt>

[<span data-ttu-id="f5883-138">Schreiben eines Ereignis Anbieters</span><span class="sxs-lookup"><span data-stu-id="f5883-138">Writing an Event Provider</span></span>](writing-an-event-provider.md)
</dt> </dl>

 

