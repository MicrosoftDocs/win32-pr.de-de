---
description: Registriert Eigenschafts Anbieter in WMI.
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: __PropertyProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529306"
---
# <a name="__propertyproviderregistration-class"></a><span data-ttu-id="746b8-103">\_\_Propertyproviderregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="746b8-103">\_\_PropertyProviderRegistration class</span></span>

<span data-ttu-id="746b8-104">Die **\_ \_ propertyproviderregistration** -System Klasse registriert Eigenschafts Anbieter in WMI.</span><span class="sxs-lookup"><span data-stu-id="746b8-104">The **\_\_PropertyProviderRegistration** system class registers property providers in WMI.</span></span>

<span data-ttu-id="746b8-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="746b8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="746b8-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="746b8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="746b8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="746b8-107">Syntax</span></span>

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a><span data-ttu-id="746b8-108">Member</span><span class="sxs-lookup"><span data-stu-id="746b8-108">Members</span></span>

<span data-ttu-id="746b8-109">Die **\_ \_ propertyproviderregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="746b8-109">The **\_\_PropertyProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="746b8-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="746b8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="746b8-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="746b8-111">Properties</span></span>

<span data-ttu-id="746b8-112">Die **\_ \_ propertyproviderregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="746b8-112">The **\_\_PropertyProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="746b8-113">**ab**</span><span class="sxs-lookup"><span data-stu-id="746b8-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="746b8-114">Datentyp: **\_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="746b8-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="746b8-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="746b8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="746b8-116">Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die den Objekt Pfad des Eigenschaften Anbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="746b8-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the property provider.</span></span> <span data-ttu-id="746b8-117">Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="746b8-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="746b8-118">**Supportsget**</span><span class="sxs-lookup"><span data-stu-id="746b8-118">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="746b8-119">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="746b8-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="746b8-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="746b8-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="746b8-121">Beschreibt, ob der Klassen-oder Instanzanbieter den Datenabruf unterstützt.</span><span class="sxs-lookup"><span data-stu-id="746b8-121">Describes whether the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="746b8-122">Richtig</span><span class="sxs-lookup"><span data-stu-id="746b8-122">True</span></span>
</dt> <dd>

<span data-ttu-id="746b8-123">Der Anbieter unterstützt den Datenabruf durch Implementieren von [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="746b8-123">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="746b8-124">False</span><span class="sxs-lookup"><span data-stu-id="746b8-124">False</span></span>
</dt> <dd>

<span data-ttu-id="746b8-125">Der Anbieter unterstützt nicht das Abrufen von Daten und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="746b8-125">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="746b8-126">**Supportsput**</span><span class="sxs-lookup"><span data-stu-id="746b8-126">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="746b8-127">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="746b8-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="746b8-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="746b8-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="746b8-129">Beschreibt, ob der Klassen-oder Instanzanbieter die Datenänderung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="746b8-129">Describes whether the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="746b8-130">Richtig</span><span class="sxs-lookup"><span data-stu-id="746b8-130">True</span></span>
</dt> <dd>

<span data-ttu-id="746b8-131">Der Anbieter unterstützt die Änderung von Klassen oder Instanzen durch Implementieren einer der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="746b8-131">The provider supports class or instance modification by implementing one of the following methods:</span></span>

-   <span data-ttu-id="746b8-132">[**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (Klassen Anbieter)</span><span class="sxs-lookup"><span data-stu-id="746b8-132">[**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers)</span></span>
-   <span data-ttu-id="746b8-133">[**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (Klassen Anbieter)</span><span class="sxs-lookup"><span data-stu-id="746b8-133">[**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers)</span></span>

</dd> <dt>

<span data-ttu-id="746b8-134">False</span><span class="sxs-lookup"><span data-stu-id="746b8-134">False</span></span>
</dt> <dd>

<span data-ttu-id="746b8-135">Der Anbieter unterstützt keine Datenänderungen und gibt den **WBEM E-Anbieter zurück, der \_ nicht \_ \_ \_** von [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) oder [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="746b8-135">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="746b8-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="746b8-136">Remarks</span></span>

<span data-ttu-id="746b8-137">Die **\_ \_ propertyproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="746b8-137">The **\_\_PropertyProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="746b8-138">Nur Administratoren können einen Eigenschaften Anbieter registrieren, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und **\_ \_ propertyproviderregistration** erstellen.</span><span class="sxs-lookup"><span data-stu-id="746b8-138">Only administrators can register a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_PropertyProviderRegistration**.</span></span> <span data-ttu-id="746b8-139">Nur Administratoren können einen Eigenschaften Anbieter löschen.</span><span class="sxs-lookup"><span data-stu-id="746b8-139">Only administrators can delete a property provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="746b8-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="746b8-140">Requirements</span></span>



| <span data-ttu-id="746b8-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="746b8-141">Requirement</span></span> | <span data-ttu-id="746b8-142">Wert</span><span class="sxs-lookup"><span data-stu-id="746b8-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="746b8-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="746b8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="746b8-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="746b8-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="746b8-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="746b8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="746b8-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="746b8-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="746b8-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="746b8-147">Namespace</span></span><br/>                | <span data-ttu-id="746b8-148">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="746b8-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="746b8-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="746b8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="746b8-150">**\_\_Providerregistration**</span><span class="sxs-lookup"><span data-stu-id="746b8-150">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="746b8-151">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="746b8-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="746b8-152">Registrieren eines Eigenschaften Anbieters</span><span class="sxs-lookup"><span data-stu-id="746b8-152">Registering a Property Provider</span></span>](registering-a-property-provider.md)
</dt> </dl>

 

