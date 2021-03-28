---
description: Stellt die Ereignistyp Klasse für Objekt Handle-Ereignisse dar, die mit dem Anfang und dem Ende der Datensammlung verknüpft sind.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Obhandlerundownvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980120"
---
# <a name="obhandlerundownevent-class"></a><span data-ttu-id="6fadc-103">Obhandlerundownvent-Klasse</span><span class="sxs-lookup"><span data-stu-id="6fadc-103">ObHandleRundownEvent class</span></span>

<span data-ttu-id="6fadc-104">Stellt die Ereignistyp Klasse für Objekt Handle-Ereignisse dar, die mit dem Anfang und dem Ende der Datensammlung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6fadc-104">Represents the event type class for object handle events related to the beginning and end of data collection.</span></span> <span data-ttu-id="6fadc-105">Dieses Ereignis umfasst das Aufzählen aller Handles, wenn der rundown ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fadc-105">This event involves the enumerating of all handles when rundown is performed.</span></span>

<span data-ttu-id="6fadc-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6fadc-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fadc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fadc-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="6fadc-108">Member</span><span class="sxs-lookup"><span data-stu-id="6fadc-108">Members</span></span>

<span data-ttu-id="6fadc-109">Die **obhandlerundownetvent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6fadc-109">The **ObHandleRundownEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="6fadc-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fadc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fadc-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6fadc-111">Properties</span></span>

<span data-ttu-id="6fadc-112">Die **obhandlerundownetvent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6fadc-112">The **ObHandleRundownEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fadc-113">**Handle**</span><span class="sxs-lookup"><span data-stu-id="6fadc-113">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fadc-114">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fadc-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fadc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-116">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="6fadc-116">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="6fadc-117">Das Objekt handle.</span><span class="sxs-lookup"><span data-stu-id="6fadc-117">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="6fadc-118">**Object**</span><span class="sxs-lookup"><span data-stu-id="6fadc-118">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fadc-119">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fadc-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fadc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-121">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Zeiger**](event-tracing-mof-qualifiers.md), [**wmidataid**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="6fadc-121">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6fadc-122">Das Objekt.</span><span class="sxs-lookup"><span data-stu-id="6fadc-122">The object.</span></span>

</dd> <dt>

<span data-ttu-id="6fadc-123">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="6fadc-123">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fadc-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6fadc-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fadc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-126">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**stringbeendigung**](event-tracing-mof-qualifiers.md) ("nullterminiert"), [**wmidataid**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="6fadc-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="6fadc-127">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6fadc-127">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="6fadc-128">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="6fadc-128">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fadc-129">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6fadc-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fadc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-131">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="6fadc-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="6fadc-132">Der Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="6fadc-132">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="6fadc-133">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="6fadc-133">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fadc-134">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fadc-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6fadc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fadc-136">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="6fadc-136">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="6fadc-137">Der Prozessbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6fadc-137">The process identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fadc-138">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6fadc-138">Requirements</span></span>



| <span data-ttu-id="6fadc-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fadc-139">Requirement</span></span> | <span data-ttu-id="6fadc-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6fadc-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fadc-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6fadc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6fadc-142">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fadc-142">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6fadc-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6fadc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6fadc-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6fadc-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6fadc-145">MOF</span><span class="sxs-lookup"><span data-stu-id="6fadc-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fadc-146"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6fadc-146"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




