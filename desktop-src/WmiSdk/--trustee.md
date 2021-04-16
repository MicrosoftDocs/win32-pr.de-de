---
description: Die \_ \_ abstrakte System Klasse des Vertrauens nehmers stellt einen Vertrauens nehmer dar. Es kann entweder ein Name oder eine sid (Bytearray) verwendet werden.
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530368"
---
# <a name="__trustee-class"></a><span data-ttu-id="de692-104">\_\_Treuhänder Klasse</span><span class="sxs-lookup"><span data-stu-id="de692-104">\_\_Trustee class</span></span>

<span data-ttu-id="de692-105">Die [**\_ \_ abstrakte**](--securitydescriptor.md) System Klasse des Vertrauens nehmers [*stellt einen Vertrauens*](/windows/desktop/SecGloss/t-gly)nehmer dar.</span><span class="sxs-lookup"><span data-stu-id="de692-105">The [**\_\_Trustee**](--securitydescriptor.md) abstract system class represents a [*trustee*](/windows/desktop/SecGloss/t-gly).</span></span> <span data-ttu-id="de692-106">Es kann entweder ein Name oder eine sid (Bytearray) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de692-106">Either a name or an SID (byte array) can be used.</span></span>

<span data-ttu-id="de692-107">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="de692-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="de692-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="de692-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de692-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="de692-109">Syntax</span></span>

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="de692-110">Member</span><span class="sxs-lookup"><span data-stu-id="de692-110">Members</span></span>

<span data-ttu-id="de692-111">Die **\_ \_ Treuhänder** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="de692-111">The **\_\_Trustee** class has these types of members:</span></span>

-   [<span data-ttu-id="de692-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de692-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de692-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="de692-113">Properties</span></span>

<span data-ttu-id="de692-114">Die **\_ \_ Treuhänder** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="de692-114">The **\_\_Trustee** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de692-115">**Domäne**</span><span class="sxs-lookup"><span data-stu-id="de692-115">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de692-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de692-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de692-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="de692-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="de692-118">Domänen Teil des Kontos.</span><span class="sxs-lookup"><span data-stu-id="de692-118">Domain portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="de692-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="de692-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de692-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de692-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de692-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="de692-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="de692-122">Der Namensteil des Kontos.</span><span class="sxs-lookup"><span data-stu-id="de692-122">Name portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="de692-123">**SID**</span><span class="sxs-lookup"><span data-stu-id="de692-123">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de692-124">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="de692-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="de692-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="de692-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="de692-126">Die SID des Vertrauens nehmers im binären Bytearray-Formular.</span><span class="sxs-lookup"><span data-stu-id="de692-126">The SID of the trustee in the binary byte array form.</span></span>

</dd> <dt>

<span data-ttu-id="de692-127">**SidLength**</span><span class="sxs-lookup"><span data-stu-id="de692-127">**SidLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de692-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de692-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="de692-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="de692-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="de692-130">Die Länge der sid (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="de692-130">The length of the SID in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="de692-131">**Sidstring**</span><span class="sxs-lookup"><span data-stu-id="de692-131">**SidString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de692-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="de692-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de692-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="de692-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="de692-134">Die SID des Vertrauens nehmers im Zeichen folgen Format, z. b. "S-1-1-0".</span><span class="sxs-lookup"><span data-stu-id="de692-134">The SID of the trustee in the string format, for example, "S-1-1-0".</span></span>

</dd> <dt>

<span data-ttu-id="de692-135">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="de692-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de692-136">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de692-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de692-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="de692-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de692-138">Uhrzeit im [CIM- \_ DateTime](cim-datetime.md) -Format, als die Sicherheits Beschreibung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="de692-138">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de692-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de692-139">Remarks</span></span>

<span data-ttu-id="de692-140">Diese Klasse stellt Eigenschaften bereit, die von der [**Win32- \_ Treuhänder**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) Klasse geerbt werden, die ein Member der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="de692-140">This class provides properties that are inherited by the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="de692-141">Weitere Informationen finden Sie unter [WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="de692-141">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="de692-142">Weitere Informationen zu ACEs finden Sie unter [Access Control-Komponenten](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="de692-142">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="de692-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de692-143">Requirements</span></span>



| <span data-ttu-id="de692-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de692-144">Requirement</span></span> | <span data-ttu-id="de692-145">Wert</span><span class="sxs-lookup"><span data-stu-id="de692-145">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="de692-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de692-146">Minimum supported client</span></span><br/> | <span data-ttu-id="de692-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de692-147">Windows Vista</span></span><br/>       |
| <span data-ttu-id="de692-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de692-148">Minimum supported server</span></span><br/> | <span data-ttu-id="de692-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de692-149">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="de692-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="de692-150">Namespace</span></span><br/>                | <span data-ttu-id="de692-151">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="de692-151">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="de692-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de692-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de692-153">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="de692-153">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="de692-154">**Win32- \_ Treuhänder**</span><span class="sxs-lookup"><span data-stu-id="de692-154">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[<span data-ttu-id="de692-155">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="de692-155">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

