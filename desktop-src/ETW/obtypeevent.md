---
description: Stellt die Ereignistyp Klasse für Objekttyp Ereignisse dar, die mit dem Anfang und dem Ende der Datensammlung verknüpft sind.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: Obtypeevent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131881"
---
# <a name="obtypeevent-class"></a><span data-ttu-id="b10ac-103">Obtypeevent-Klasse</span><span class="sxs-lookup"><span data-stu-id="b10ac-103">ObTypeEvent class</span></span>

<span data-ttu-id="b10ac-104">Stellt die Ereignistyp Klasse für Objekttyp Ereignisse dar, die mit dem Anfang und dem Ende der Datensammlung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="b10ac-104">Represents the event type class for object type events related to the beginning and end of data collection.</span></span> <span data-ttu-id="b10ac-105">Dieses Ereignis umfasst die Zuordnung der Typindex Werte zu den Typnamen.</span><span class="sxs-lookup"><span data-stu-id="b10ac-105">This event involves the mapping of the type index values to the type names.</span></span>

<span data-ttu-id="b10ac-106">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b10ac-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b10ac-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b10ac-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a><span data-ttu-id="b10ac-108">Member</span><span class="sxs-lookup"><span data-stu-id="b10ac-108">Members</span></span>

<span data-ttu-id="b10ac-109">Die **obtypeevent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b10ac-109">The **ObTypeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b10ac-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b10ac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b10ac-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b10ac-111">Properties</span></span>

<span data-ttu-id="b10ac-112">Die **obtypeevent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b10ac-112">The **ObTypeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b10ac-113">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="b10ac-113">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b10ac-114">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b10ac-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b10ac-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b10ac-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b10ac-116">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="b10ac-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b10ac-117">Der Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="b10ac-117">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="b10ac-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b10ac-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b10ac-119">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b10ac-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b10ac-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b10ac-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b10ac-121">Qualifizierer: [**wmidataid**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="b10ac-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="b10ac-122">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="b10ac-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b10ac-123">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="b10ac-123">**TypeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b10ac-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b10ac-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b10ac-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b10ac-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b10ac-126">Qualifizierer: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**stringbeendigung**](event-tracing-mof-qualifiers.md) ("nullterminiert"), [**wmidataid**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="b10ac-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="b10ac-127">Der Typname.</span><span class="sxs-lookup"><span data-stu-id="b10ac-127">The type name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b10ac-128">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b10ac-128">Requirements</span></span>



| <span data-ttu-id="b10ac-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b10ac-129">Requirement</span></span> | <span data-ttu-id="b10ac-130">Wert</span><span class="sxs-lookup"><span data-stu-id="b10ac-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b10ac-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b10ac-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b10ac-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b10ac-132">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b10ac-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b10ac-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b10ac-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b10ac-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b10ac-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b10ac-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b10ac-136"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b10ac-136"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




