---
description: Meldet ein instanzlöschungsereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das beim Löschen einer Instanz aus dem Namespace generiert wird.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: __InstanceDeletionEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360697"
---
# <a name="__instancedeletionevent-class"></a><span data-ttu-id="53c4b-103">\_\_Instancedeletionevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="53c4b-103">\_\_InstanceDeletionEvent class</span></span>

<span data-ttu-id="53c4b-104">Die **\_ \_ instancedeletionevent** -System Klasse meldet ein instanzlöschungsereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das beim Löschen einer Instanz aus dem-Namespace generiert wird.</span><span class="sxs-lookup"><span data-stu-id="53c4b-104">The **\_\_InstanceDeletionEvent** system class reports an instance deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance is deleted from the namespace.</span></span>

<span data-ttu-id="53c4b-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="53c4b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="53c4b-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="53c4b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c4b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="53c4b-107">Syntax</span></span>

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="53c4b-108">Member</span><span class="sxs-lookup"><span data-stu-id="53c4b-108">Members</span></span>

<span data-ttu-id="53c4b-109">Die **\_ \_ instancedeletionevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="53c4b-109">The **\_\_InstanceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="53c4b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53c4b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53c4b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53c4b-111">Properties</span></span>

<span data-ttu-id="53c4b-112">Die **\_ \_ instancedeletionevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="53c4b-112">The **\_\_InstanceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="53c4b-113">**Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53c4b-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53c4b-114">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="53c4b-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="53c4b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53c4b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53c4b-116">Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können.</span><span class="sxs-lookup"><span data-stu-id="53c4b-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="53c4b-117">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="53c4b-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="53c4b-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="53c4b-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53c4b-119">Datentyp: **Object**</span><span class="sxs-lookup"><span data-stu-id="53c4b-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="53c4b-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53c4b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53c4b-121">Kopie der-Instanz, die gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="53c4b-121">Copy of the instance that was deleted.</span></span> <span data-ttu-id="53c4b-122">Diese Eigenschaft wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="53c4b-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="53c4b-123">**\_Erstellungszeit**</span><span class="sxs-lookup"><span data-stu-id="53c4b-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53c4b-124">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="53c4b-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="53c4b-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="53c4b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="53c4b-126">Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="53c4b-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="53c4b-127">Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt.</span><span class="sxs-lookup"><span data-stu-id="53c4b-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="53c4b-128">Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor.</span><span class="sxs-lookup"><span data-stu-id="53c4b-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="53c4b-129">Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="53c4b-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="53c4b-130">Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="53c4b-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53c4b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53c4b-131">Remarks</span></span>

<span data-ttu-id="53c4b-132">Die **\_ \_ instancedeletionevent** -Klasse wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="53c4b-132">The **\_\_InstanceDeletionEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="53c4b-133">**Löschen einer Ressource: \_ \_ instancedeletionevent**</span><span class="sxs-lookup"><span data-stu-id="53c4b-133">**Deletion of a resource: \_\_InstanceDeletionEvent**</span></span>

<span data-ttu-id="53c4b-134">Wenn Sie sicherstellen möchten, dass ein bestimmtes antivirenüberprüfungs Programm weiterhin auf einem Computer ausgeführt wird, können Sie ein Skript schreiben, mit dem die Prozesse auf dem Computer überwacht werden, um zu bestimmen, ob die Prozesse angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="53c4b-134">If you want to ensure that a particular antivirus scanner program continues to run on a computer, you can write a script that monitors the processes on the computer to determine whether any of them stop.</span></span>

<span data-ttu-id="53c4b-135">Benachrichtigungs Abfragen, die eine Benachrichtigung über das Löschen einer Ressource anfordern und systeminterne Ereignisse verwenden, verwenden alle eine Syntax ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="53c4b-135">Notification queries that request notification of the deletion of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a><span data-ttu-id="53c4b-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53c4b-136">Examples</span></span>

<span data-ttu-id="53c4b-137">Im Codebeispiel für das [Monitor Process](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) Delete-Ereignis VBScript in der TechNet Gallery wird **\_ \_ instancedeletionevent** verwendet, um das erste Vorkommen eines Lösch Ereignisses für eine WMI-Instanz für den [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process)zu überwachen</span><span class="sxs-lookup"><span data-stu-id="53c4b-137">The [Monitor process deletion event](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript code sample on TechNet Gallery uses **\_\_InstanceDeletionEvent** to monitor the first occurrence of a WMI instance deletion event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="53c4b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53c4b-138">Requirements</span></span>



| <span data-ttu-id="53c4b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53c4b-139">Requirement</span></span> | <span data-ttu-id="53c4b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="53c4b-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="53c4b-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53c4b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="53c4b-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53c4b-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="53c4b-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53c4b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="53c4b-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53c4b-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="53c4b-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="53c4b-145">Namespace</span></span><br/>                | <span data-ttu-id="53c4b-146">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="53c4b-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="53c4b-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53c4b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c4b-148">**\_\_Instanceoperationevent**</span><span class="sxs-lookup"><span data-stu-id="53c4b-148">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="53c4b-149">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="53c4b-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

