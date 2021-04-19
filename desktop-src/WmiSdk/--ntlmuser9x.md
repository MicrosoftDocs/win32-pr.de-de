---
description: Steuert den Remote Zugriff auf nicht unterstützte Versionen von Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: __NTLMUser9X-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349650"
---
# <a name="__ntlmuser9x-class"></a><span data-ttu-id="b6ffc-103">\_\_NTLMUser9X-Klasse</span><span class="sxs-lookup"><span data-stu-id="b6ffc-103">\_\_NTLMUser9X class</span></span>

<span data-ttu-id="b6ffc-104">Die **\_ \_ NTLMUser9X** -System Klasse steuert den Remote Zugriff auf nicht unterstützte Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-104">The **\_\_NTLMUser9X** system class controls remote access to unsupported versions of Windows.</span></span> <span data-ttu-id="b6ffc-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b6ffc-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ffc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6ffc-107">Syntax</span></span>

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="b6ffc-108">Member</span><span class="sxs-lookup"><span data-stu-id="b6ffc-108">Members</span></span>

<span data-ttu-id="b6ffc-109">Die **\_ \_ NTLMUser9X** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b6ffc-109">The **\_\_NTLMUser9X** class has these types of members:</span></span>

-   [<span data-ttu-id="b6ffc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6ffc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6ffc-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b6ffc-111">Properties</span></span>

<span data-ttu-id="b6ffc-112">Die **\_ \_ NTLMUser9X** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-112">The **\_\_NTLMUser9X** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6ffc-113">**Autoritative Stelle**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-113">**Authority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6ffc-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6ffc-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6ffc-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b6ffc-116">Die Domäne, für die ein Benutzername gilt.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-116">Domain to which a user name applies.</span></span>

</dd> <dt>

<span data-ttu-id="b6ffc-117">**Flags**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-117">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6ffc-118">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6ffc-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6ffc-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b6ffc-120">Vererbungsflags.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-120">Inheritance flags.</span></span>

<dt>

<span data-ttu-id="b6ffc-121">0</span><span class="sxs-lookup"><span data-stu-id="b6ffc-121">0</span></span>
</dt> <dd>

<span data-ttu-id="b6ffc-122">Keine Vererbung.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-122">No inheritance.</span></span>

</dd> <dt>

<span data-ttu-id="b6ffc-123">2</span><span class="sxs-lookup"><span data-stu-id="b6ffc-123">2</span></span>
</dt> <dd>

<span data-ttu-id="b6ffc-124">Gilt für untergeordnete Namespaces, zusätzlich zur aktuellen.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-124">Apply to child namespaces, in addition to the current one.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b6ffc-125">**Mask**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-125">**Mask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6ffc-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6ffc-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6ffc-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b6ffc-128">Bitmaske, die Zugriffsrechte für den Namespace im WMI-Repository (Windows-Verwaltungsinstrumentation) angibt.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-128">Bitmask that specifies access rights to the namespace in the Windows Management Instrumentation (WMI) repository.</span></span> <span data-ttu-id="b6ffc-129">Informationen zu Bitwerten finden Sie unter [**Namespace-Zugriffsrechte Konstanten**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b6ffc-129">For bit values, see [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6ffc-130">**Name**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6ffc-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6ffc-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6ffc-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b6ffc-133">Benutzername.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-133">User name.</span></span>

</dd> <dt>

<span data-ttu-id="b6ffc-134">**Type**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-134">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6ffc-135">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6ffc-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="b6ffc-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b6ffc-137">Der Zugriff ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-137">Access allowed.</span></span>

<dt>

<span data-ttu-id="b6ffc-138">0</span><span class="sxs-lookup"><span data-stu-id="b6ffc-138">0</span></span>
</dt> <dd>

<span data-ttu-id="b6ffc-139">Der Zugriff ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-139">Access allowed.</span></span>

</dd> <dt>

<span data-ttu-id="b6ffc-140">2</span><span class="sxs-lookup"><span data-stu-id="b6ffc-140">2</span></span>
</dt> <dd>

<span data-ttu-id="b6ffc-141">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-141">Access denied.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6ffc-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6ffc-142">Remarks</span></span>

<span data-ttu-id="b6ffc-143">Die **\_ \_ NTLMUser9X** -Klasse wird als Eingabeparameter für die Methoden " [**\_ \_ SystemSecurity:: Get9XUserList**](--systemsecurity-get9xuserlist.md) " und " [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) " verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6ffc-143">The **\_\_NTLMUser9X** class is used as an input parameter for the [**\_\_SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) and [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ffc-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6ffc-144">Requirements</span></span>



| <span data-ttu-id="b6ffc-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6ffc-145">Requirement</span></span> | <span data-ttu-id="b6ffc-146">Wert</span><span class="sxs-lookup"><span data-stu-id="b6ffc-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b6ffc-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6ffc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ffc-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6ffc-148">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b6ffc-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6ffc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ffc-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6ffc-150">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b6ffc-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6ffc-151">Namespace</span></span><br/>                | <span data-ttu-id="b6ffc-152">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="b6ffc-152">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b6ffc-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6ffc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ffc-154">**\_\_Securityrelatedclass**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-154">**\_\_SecurityRelatedClass**</span></span>](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[<span data-ttu-id="b6ffc-155">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="b6ffc-155">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="b6ffc-156">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="b6ffc-156">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

