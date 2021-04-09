---
description: Registriert Ereignisconsumeranbieter bei WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: __EventConsumerProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867356"
---
# <a name="__eventconsumerproviderregistration-class"></a><span data-ttu-id="e3777-103">\_\_Eventconsumerproviderregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="e3777-103">\_\_EventConsumerProviderRegistration class</span></span>

<span data-ttu-id="e3777-104">Die **\_ \_ eventconsumerproviderregistration-System Klasse registriert Ereignisconsumeranbieter** bei WMI.</span><span class="sxs-lookup"><span data-stu-id="e3777-104">The **\_\_EventConsumerProviderRegistration** system class registers event consumer providers with WMI.</span></span>

<span data-ttu-id="e3777-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e3777-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e3777-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e3777-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3777-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3777-107">Syntax</span></span>

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="e3777-108">Member</span><span class="sxs-lookup"><span data-stu-id="e3777-108">Members</span></span>

<span data-ttu-id="e3777-109">Die **\_ \_ eventconsumerproviderregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e3777-109">The **\_\_EventConsumerProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="e3777-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3777-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3777-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e3777-111">Properties</span></span>

<span data-ttu-id="e3777-112">Die **\_ \_ eventconsumerproviderregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e3777-112">The **\_\_EventConsumerProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3777-113">**Consumerclassnames**</span><span class="sxs-lookup"><span data-stu-id="e3777-113">**ConsumerClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3777-114">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="e3777-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e3777-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="e3777-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e3777-116">Array von Namen der logischen Consumerklassen, die vom Ereignisconsumeranbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e3777-116">Array of names of the logical consumer classes that the event consumer provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="e3777-117">**ab**</span><span class="sxs-lookup"><span data-stu-id="e3777-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3777-118">Datentyp: **\_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="e3777-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="e3777-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e3777-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3777-120">Objekt Pfad zum Anbieter.</span><span class="sxs-lookup"><span data-stu-id="e3777-120">Object path to the provider.</span></span> <span data-ttu-id="e3777-121">Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="e3777-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3777-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3777-122">Remarks</span></span>

<span data-ttu-id="e3777-123">Die **\_ \_ eventconsumerproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e3777-123">The **\_\_EventConsumerProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3777-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3777-124">Requirements</span></span>



| <span data-ttu-id="e3777-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3777-125">Requirement</span></span> | <span data-ttu-id="e3777-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e3777-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e3777-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3777-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e3777-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3777-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e3777-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3777-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e3777-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3777-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="e3777-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3777-131">Namespace</span></span><br/>                | <span data-ttu-id="e3777-132">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="e3777-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="e3777-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3777-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3777-134">**\_\_Providerregistration**</span><span class="sxs-lookup"><span data-stu-id="e3777-134">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="e3777-135">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="e3777-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="e3777-136">Registrieren eines Ereignisconsumeranbieters</span><span class="sxs-lookup"><span data-stu-id="e3777-136">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
</dt> <dt>

[<span data-ttu-id="e3777-137">Schreiben eines Ereignisconsumeranbieters</span><span class="sxs-lookup"><span data-stu-id="e3777-137">Writing an Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)
</dt> </dl>

 

