---
description: Stellt einen Zugriffssteuerungseintrag (ACE) dar.
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: __ACE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485755"
---
# <a name="__ace-class"></a><span data-ttu-id="416c5-103">\_\_ACE-Klasse</span><span class="sxs-lookup"><span data-stu-id="416c5-103">\_\_ACE class</span></span>

<span data-ttu-id="416c5-104">Die **\_ \_ ACE** Abstract-System Klasse stellt einen Zugriffs Steuerungs Eintrag ([*ACE*](/windows/desktop/SecGloss/a-gly)) dar.</span><span class="sxs-lookup"><span data-stu-id="416c5-104">The **\_\_ACE** abstract system class represents an access control entry ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span></span>

<span data-ttu-id="416c5-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="416c5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="416c5-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="416c5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="416c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="416c5-107">Syntax</span></span>

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a><span data-ttu-id="416c5-108">Member</span><span class="sxs-lookup"><span data-stu-id="416c5-108">Members</span></span>

<span data-ttu-id="416c5-109">Die **\_ \_ ACE** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="416c5-109">The **\_\_ACE** class has these types of members:</span></span>

-   [<span data-ttu-id="416c5-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="416c5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="416c5-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="416c5-111">Properties</span></span>

<span data-ttu-id="416c5-112">Die **\_ \_ ACE** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="416c5-112">The **\_\_ACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="416c5-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="416c5-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416c5-114">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="416c5-114">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="416c5-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="416c5-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="416c5-116">Bitflags, die Rechte darstellen, die dem Vertrauens nehmer gewährt oder verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="416c5-116">Bit flags representing rights that are granted or denied to the trustee.</span></span> <span data-ttu-id="416c5-117">Weitere Informationen und eine Beschreibung der Flags finden Sie unter **AccessMask** -Eigenschaft in der [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Klasse "Ace".</span><span class="sxs-lookup"><span data-stu-id="416c5-117">For more information and a description of the flags, see **AccessMask** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="416c5-118">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="416c5-118">**AceFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416c5-119">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="416c5-119">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="416c5-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="416c5-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="416c5-121">Bitflags, die die Vererbung des ACE angeben.</span><span class="sxs-lookup"><span data-stu-id="416c5-121">Bit flags specifying the inheritance of the ACE.</span></span> <span data-ttu-id="416c5-122">Weitere Informationen und eine Beschreibung der Flags finden Sie unter **AceFlags** -Eigenschaft in der [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="416c5-122">For more information and a description of the flags, see **AceFlags** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="416c5-123">**AceType**</span><span class="sxs-lookup"><span data-stu-id="416c5-123">**AceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416c5-124">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="416c5-124">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="416c5-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="416c5-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="416c5-126">Der Typ des ACE-Eintrags, den diese Instanz darstellt.</span><span class="sxs-lookup"><span data-stu-id="416c5-126">The type of ACE entry that this instance represents.</span></span>

</dd> <dt>

<span data-ttu-id="416c5-127">**Guidinheritedobjecttype**</span><span class="sxs-lookup"><span data-stu-id="416c5-127">**GuidInheritedObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416c5-128">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="416c5-128">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="416c5-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="416c5-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="416c5-130">Die GUID des übergeordneten Elements des Objekts, auf das die Zugriffsrechte in der **AccessMask** -Eigenschaft angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="416c5-130">The GUID of the parent of the object to which the access rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="416c5-131">**Guidobjecttype**</span><span class="sxs-lookup"><span data-stu-id="416c5-131">**GuidObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416c5-132">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="416c5-132">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="416c5-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="416c5-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="416c5-134">Die GUID, die den Typ des Objekts angibt, auf das die Rechte in der **AccessMask** -Eigenschaft angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="416c5-134">The GUID that indicates the type of object to which the rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="416c5-135">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="416c5-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416c5-136">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="416c5-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="416c5-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="416c5-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="416c5-138">Die Zeit im CIM- [ \_ DateTime](cim-datetime.md) -Format, zu der die Sicherheits Beschreibung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="416c5-138">The time, in the [CIM\_DATETIME](cim-datetime.md) format, when the security descriptor was created.</span></span>

</dd> <dt>

<span data-ttu-id="416c5-139">**Stiftungs**</span><span class="sxs-lookup"><span data-stu-id="416c5-139">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="416c5-140">Datentyp: **[ **\_ \_ Treuhänder**](--trustee.md)**</span><span class="sxs-lookup"><span data-stu-id="416c5-140">Data type: **[**\_\_Trustee**](--trustee.md)**</span></span>
</dt> <dt>

<span data-ttu-id="416c5-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="416c5-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="416c5-142">Der Treuhänder des ACE-Eintrags, der durch diese Instanz der **\_ \_ ACE** -Klasse dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="416c5-142">The trustee of the ACE entry represented by this instance of the **\_\_ACE** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="416c5-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="416c5-143">Remarks</span></span>

<span data-ttu-id="416c5-144">Diese Klasse stellt die Eigenschaften bereit, die von der [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Klasse geerbt werden, die ein Member der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="416c5-144">This class provides the properties that are inherited by the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="416c5-145">Weitere Informationen finden Sie unter [WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="416c5-145">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="416c5-146">Weitere Informationen zu ACEs finden Sie unter [Access Control-Komponenten](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="416c5-146">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="416c5-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="416c5-147">Requirements</span></span>



| <span data-ttu-id="416c5-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="416c5-148">Requirement</span></span> | <span data-ttu-id="416c5-149">Wert</span><span class="sxs-lookup"><span data-stu-id="416c5-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="416c5-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="416c5-150">Minimum supported client</span></span><br/> | <span data-ttu-id="416c5-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="416c5-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="416c5-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="416c5-152">Minimum supported server</span></span><br/> | <span data-ttu-id="416c5-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="416c5-153">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="416c5-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="416c5-154">Namespace</span></span><br/>                | <span data-ttu-id="416c5-155">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="416c5-155">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="416c5-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="416c5-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="416c5-157">**\_\_Securityrelatedclass**</span><span class="sxs-lookup"><span data-stu-id="416c5-157">**\_\_SecurityRelatedClass**</span></span>](--securityrelatedclass.md)
</dt> <dt>

[<span data-ttu-id="416c5-158">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="416c5-158">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="416c5-159">**Win32- \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="416c5-159">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="416c5-160">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="416c5-160">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

