---
description: Stellt eine Sicherheitsbeschreibung dar.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216322"
---
# <a name="__securitydescriptor-class"></a><span data-ttu-id="f56fb-103">\_\_SecurityDescriptor-Klasse</span><span class="sxs-lookup"><span data-stu-id="f56fb-103">\_\_SecurityDescriptor class</span></span>

<span data-ttu-id="f56fb-104">Die abstrakte System Klasse **\_ \_ securityDescriptor** stellt eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)dar.</span><span class="sxs-lookup"><span data-stu-id="f56fb-104">The **\_\_SecurityDescriptor** abstract system class represents a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="f56fb-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="f56fb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f56fb-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f56fb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f56fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f56fb-107">Syntax</span></span>

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="f56fb-108">Member</span><span class="sxs-lookup"><span data-stu-id="f56fb-108">Members</span></span>

<span data-ttu-id="f56fb-109">Die **\_ \_ securityDescriptor** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f56fb-109">The **\_\_SecurityDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="f56fb-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f56fb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f56fb-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f56fb-111">Properties</span></span>

<span data-ttu-id="f56fb-112">Die **\_ \_ securityDescriptor** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f56fb-112">The **\_\_SecurityDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f56fb-113">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="f56fb-113">**ControlFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56fb-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f56fb-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f56fb-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f56fb-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f56fb-116">Bitflags, die Informationen über den Inhalt und das Format des Deskriptors bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f56fb-116">Bit flags that provide information about the descriptor's contents and format.</span></span> <span data-ttu-id="f56fb-117">Eine Beschreibung der Flags finden Sie in der Eigenschaft " **ControlFlags** " in der Win32-Klasse " [**\_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ".</span><span class="sxs-lookup"><span data-stu-id="f56fb-117">See the **ControlFlags** property in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class for a description of the flags.</span></span>

</dd> <dt>

<span data-ttu-id="f56fb-118">**DACL**</span><span class="sxs-lookup"><span data-stu-id="f56fb-118">**DACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56fb-119">Datentyp: **[**\_ \_ ACE**](--ace.md)** -Array</span><span class="sxs-lookup"><span data-stu-id="f56fb-119">Data type: **[**\_\_ACE**](--ace.md)** array</span></span>
</dt> <dt>

<span data-ttu-id="f56fb-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f56fb-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f56fb-121">Ein Array von [**\_ \_ ACE**](--ace.md) -Einträgen, die den Zugriff auf das-Objekt angeben.</span><span class="sxs-lookup"><span data-stu-id="f56fb-121">An array of [**\_\_ACE**](--ace.md) entries that specify access to the object.</span></span>

</dd> <dt>

<span data-ttu-id="f56fb-122">**Gruppieren**</span><span class="sxs-lookup"><span data-stu-id="f56fb-122">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56fb-123">Datentyp: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="f56fb-123">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f56fb-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f56fb-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f56fb-125">ACE, der den Vertrauens nehmer identifiziert, der die Gruppe des Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="f56fb-125">ACE that identifies the trustee representing the group of the object.</span></span>

</dd> <dt>

<span data-ttu-id="f56fb-126">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="f56fb-126">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56fb-127">Datentyp: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="f56fb-127">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f56fb-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f56fb-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f56fb-129">ACE, der den Vertrauens nehmer identifiziert, der den Besitzer des Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="f56fb-129">ACE that identifies the trustee representing the owner of the object.</span></span>

</dd> <dt>

<span data-ttu-id="f56fb-130">**SACL**</span><span class="sxs-lookup"><span data-stu-id="f56fb-130">**SACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56fb-131">Datentyp: **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="f56fb-131">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f56fb-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f56fb-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f56fb-133">Ein Array von [**\_ \_ ACE**](--ace.md) -Einträgen, das Benutzer und Gruppen identifiziert, für die Überwachungsinformationen gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="f56fb-133">An array of [**\_\_ACE**](--ace.md) entries that identifies users and groups for which auditing information is gathered.</span></span>

</dd> <dt>

<span data-ttu-id="f56fb-134">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="f56fb-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f56fb-135">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f56fb-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f56fb-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f56fb-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f56fb-137">Uhrzeit im [CIM- \_ DateTime](cim-datetime.md) -Format, als die Sicherheits Beschreibung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f56fb-137">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f56fb-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f56fb-138">Remarks</span></span>

<span data-ttu-id="f56fb-139">Diese Klasse stellt Eigenschaften bereit, die von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="f56fb-139">This class provides properties inherited by [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="f56fb-140">Weitere Informationen finden Sie unter [WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f56fb-140">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="f56fb-141">Weitere Informationen zu ACEs finden Sie unter [Access Control-Komponenten](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="f56fb-141">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="f56fb-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f56fb-142">Requirements</span></span>



| <span data-ttu-id="f56fb-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f56fb-143">Requirement</span></span> | <span data-ttu-id="f56fb-144">Wert</span><span class="sxs-lookup"><span data-stu-id="f56fb-144">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f56fb-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f56fb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f56fb-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f56fb-146">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f56fb-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f56fb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f56fb-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f56fb-148">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f56fb-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="f56fb-149">Namespace</span></span><br/>                | <span data-ttu-id="f56fb-150">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="f56fb-150">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f56fb-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f56fb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f56fb-152">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="f56fb-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f56fb-153">**Win32- \_ securityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f56fb-153">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="f56fb-154">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="f56fb-154">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

