---
description: Stellt die Ereignistyp Klasse für die Behandlung von duplikatereignissen dar.
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: Obshandduplicateevent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980688"
---
# <a name="obhandleduplicateevent-class"></a><span data-ttu-id="c7f5c-103">Obshandduplicateevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="c7f5c-103">ObHandleDuplicateEvent class</span></span>

<span data-ttu-id="c7f5c-104">Stellt die Ereignistyp Klasse für die Behandlung von duplikatereignissen dar.</span><span class="sxs-lookup"><span data-stu-id="c7f5c-104">Represents the event type class for handle duplication events.</span></span>

<span data-ttu-id="c7f5c-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7f5c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f5c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7f5c-106">Syntax</span></span>

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a><span data-ttu-id="c7f5c-107">Member</span><span class="sxs-lookup"><span data-stu-id="c7f5c-107">Members</span></span>

<span data-ttu-id="c7f5c-108">Die **obshandduplicateevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c7f5c-108">The **ObHandleDuplicateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c7f5c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7f5c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7f5c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7f5c-110">Properties</span></span>

<span data-ttu-id="c7f5c-111">Die **obshandduplicateevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c7f5c-111">The **ObHandleDuplicateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c7f5c-112">**Object**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-112">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f5c-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7f5c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-115">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Zeiger**](event-tracing-mof-qualifiers.md), [**wmidataid**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="c7f5c-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c7f5c-116">Das Objekt.</span><span class="sxs-lookup"><span data-stu-id="c7f5c-116">The object.</span></span>

</dd> <dt>

<span data-ttu-id="c7f5c-117">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-117">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f5c-118">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7f5c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-120">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="c7f5c-120">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="c7f5c-121">Der Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="c7f5c-121">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="c7f5c-122">**SourceHandle**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-122">**SourceHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f5c-123">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7f5c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-125">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="c7f5c-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="c7f5c-126">Das Handle des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="c7f5c-126">The handle of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="c7f5c-127">**TargetHandle**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-127">**TargetHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f5c-128">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7f5c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-130">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="c7f5c-130">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="c7f5c-131">Das Handle des Zielobjekts.</span><span class="sxs-lookup"><span data-stu-id="c7f5c-131">The handle of the target object.</span></span>

</dd> <dt>

<span data-ttu-id="c7f5c-132">**TargetProcessID**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-132">**TargetProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f5c-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7f5c-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c7f5c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f5c-135">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="c7f5c-135">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="c7f5c-136">Der Prozess Bezeichner des Ziels.</span><span class="sxs-lookup"><span data-stu-id="c7f5c-136">The process identifier of the target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7f5c-137">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c7f5c-137">Requirements</span></span>



| <span data-ttu-id="c7f5c-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7f5c-138">Requirement</span></span> | <span data-ttu-id="c7f5c-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c7f5c-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f5c-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c7f5c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c7f5c-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7f5c-141">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c7f5c-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c7f5c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c7f5c-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c7f5c-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c7f5c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c7f5c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7f5c-145"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c7f5c-145"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




