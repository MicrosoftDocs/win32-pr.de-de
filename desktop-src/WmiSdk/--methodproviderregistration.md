---
description: Registriert Methoden Anbieter bei WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: __MethodProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363709"
---
# <a name="__methodproviderregistration-class"></a><span data-ttu-id="7b6ed-103">\_\_Methodproviderregistration-Klasse</span><span class="sxs-lookup"><span data-stu-id="7b6ed-103">\_\_MethodProviderRegistration class</span></span>

<span data-ttu-id="7b6ed-104">Die **\_ \_ methodproviderregistration** -System Klasse registriert Methoden Anbieter bei WMI.</span><span class="sxs-lookup"><span data-stu-id="7b6ed-104">The **\_\_MethodProviderRegistration** system class registers method providers with WMI.</span></span>

<span data-ttu-id="7b6ed-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7b6ed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7b6ed-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7b6ed-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6ed-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b6ed-107">Syntax</span></span>

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="7b6ed-108">Member</span><span class="sxs-lookup"><span data-stu-id="7b6ed-108">Members</span></span>

<span data-ttu-id="7b6ed-109">Die **\_ \_ methodproviderregistration** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7b6ed-109">The **\_\_MethodProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="7b6ed-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b6ed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b6ed-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b6ed-111">Properties</span></span>

<span data-ttu-id="7b6ed-112">Die **\_ \_ methodproviderregistration** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7b6ed-112">The **\_\_MethodProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b6ed-113">**ab**</span><span class="sxs-lookup"><span data-stu-id="7b6ed-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6ed-114">Datentyp: **\_ \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="7b6ed-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="7b6ed-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7b6ed-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6ed-116">Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die den Objekt Pfad des Methoden Anbieters darstellt.</span><span class="sxs-lookup"><span data-stu-id="7b6ed-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the method provider.</span></span> <span data-ttu-id="7b6ed-117">Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="7b6ed-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b6ed-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b6ed-118">Remarks</span></span>

<span data-ttu-id="7b6ed-119">Die **\_ \_ methodproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7b6ed-119">The **\_\_MethodProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="7b6ed-120">Nur Administratoren können einen Methoden Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und **\_ \_ methodproviderregistration** erstellen.</span><span class="sxs-lookup"><span data-stu-id="7b6ed-120">Only administrators can register or delete a method provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_MethodProviderRegistration**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b6ed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b6ed-121">Requirements</span></span>



| <span data-ttu-id="7b6ed-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b6ed-122">Requirement</span></span> | <span data-ttu-id="7b6ed-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7b6ed-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7b6ed-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b6ed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7b6ed-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b6ed-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7b6ed-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b6ed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7b6ed-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b6ed-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="7b6ed-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b6ed-128">Namespace</span></span><br/>                | <span data-ttu-id="7b6ed-129">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="7b6ed-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="7b6ed-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b6ed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6ed-131">**\_\_Providerregistration**</span><span class="sxs-lookup"><span data-stu-id="7b6ed-131">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="7b6ed-132">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="7b6ed-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="7b6ed-133">Registrieren eines Methoden Anbieters</span><span class="sxs-lookup"><span data-stu-id="7b6ed-133">Registering a Method Provider</span></span>](registering-a-method-provider.md)
</dt> </dl>

 

