---
description: Stellt die Ereignistyp Klasse für Erstellungs-oder schließereignisse von Handles dar.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: Oblenker Event-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae293684bd09322c7193035d374e5e2bad21447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980113"
---
# <a name="obhandleevent-class"></a><span data-ttu-id="b3e2e-103">Oblenker Event-Klasse</span><span class="sxs-lookup"><span data-stu-id="b3e2e-103">ObHandleEvent class</span></span>

<span data-ttu-id="b3e2e-104">Stellt die Ereignistyp Klasse für Erstellungs-oder schließereignisse von Handles dar.</span><span class="sxs-lookup"><span data-stu-id="b3e2e-104">Represents the event type class for handle creation or closure events.</span></span>

<span data-ttu-id="b3e2e-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3e2e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e2e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3e2e-106">Syntax</span></span>

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a><span data-ttu-id="b3e2e-107">Member</span><span class="sxs-lookup"><span data-stu-id="b3e2e-107">Members</span></span>

<span data-ttu-id="b3e2e-108">Die **obshandevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b3e2e-108">The **ObHandleEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b3e2e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3e2e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3e2e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3e2e-110">Properties</span></span>

<span data-ttu-id="b3e2e-111">Die **oblenker Event** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b3e2e-111">The **ObHandleEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3e2e-112">**Handle**</span><span class="sxs-lookup"><span data-stu-id="b3e2e-112">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e2e-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3e2e-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3e2e-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3e2e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3e2e-115">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**wmidataid**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="b3e2e-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="b3e2e-116">Das Objekt handle.</span><span class="sxs-lookup"><span data-stu-id="b3e2e-116">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="b3e2e-117">**Object**</span><span class="sxs-lookup"><span data-stu-id="b3e2e-117">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e2e-118">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3e2e-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3e2e-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3e2e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3e2e-120">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Zeiger**](event-tracing-mof-qualifiers.md), [**wmidataid**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="b3e2e-120">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b3e2e-121">Das Objekt.</span><span class="sxs-lookup"><span data-stu-id="b3e2e-121">The object.</span></span>

</dd> <dt>

<span data-ttu-id="b3e2e-122">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="b3e2e-122">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e2e-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3e2e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3e2e-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3e2e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3e2e-125">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**stringbeendigung**](event-tracing-mof-qualifiers.md) ("nullterminiert"), [**wmidataid**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="b3e2e-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="b3e2e-126">Der Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="b3e2e-126">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="b3e2e-127">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="b3e2e-127">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3e2e-128">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b3e2e-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b3e2e-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b3e2e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3e2e-130">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="b3e2e-130">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="b3e2e-131">Der Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="b3e2e-131">The object type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3e2e-132">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b3e2e-132">Requirements</span></span>



| <span data-ttu-id="b3e2e-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3e2e-133">Requirement</span></span> | <span data-ttu-id="b3e2e-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b3e2e-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e2e-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3e2e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e2e-136">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3e2e-136">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b3e2e-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3e2e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e2e-138">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3e2e-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b3e2e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b3e2e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3e2e-140"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b3e2e-140"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




