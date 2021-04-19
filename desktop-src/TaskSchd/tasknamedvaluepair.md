---
title: Tasknamedvaluepair-Objekt
description: Skript Objekt, das verwendet wird, um ein Name-Wert-Paar zu erstellen, in dem der Name dem Wert zugeordnet ist.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Tasknamedvaluepair-Objekt Taskplaner
- Tasknamedvaluepair-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341996"
---
# <a name="tasknamedvaluepair-object"></a><span data-ttu-id="ea7c1-105">Tasknamedvaluepair-Objekt</span><span class="sxs-lookup"><span data-stu-id="ea7c1-105">TaskNamedValuePair object</span></span>

<span data-ttu-id="ea7c1-106">Skript Objekt, das verwendet wird, um ein Name-Wert-Paar zu erstellen, in dem der Name dem Wert zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ea7c1-106">Scripting object that is used to create a name-value pair in which the name is associated with the value.</span></span>

## <a name="members"></a><span data-ttu-id="ea7c1-107">Member</span><span class="sxs-lookup"><span data-stu-id="ea7c1-107">Members</span></span>

<span data-ttu-id="ea7c1-108">Das **tasknamedvaluepair** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ea7c1-108">The **TaskNamedValuePair** object has these types of members:</span></span>

-   [<span data-ttu-id="ea7c1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea7c1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ea7c1-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ea7c1-110">Properties</span></span>

<span data-ttu-id="ea7c1-111">Das **tasknamedvaluepair** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ea7c1-111">The **TaskNamedValuePair** object has these properties.</span></span>



| <span data-ttu-id="ea7c1-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ea7c1-112">Property</span></span>                                             | <span data-ttu-id="ea7c1-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea7c1-113">Description</span></span>                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea7c1-114">**Name**</span><span class="sxs-lookup"><span data-stu-id="ea7c1-114">**Name**</span></span>](tasknamedvaluepair-name.md)<br/>   | <span data-ttu-id="ea7c1-115">Ruft den Namen ab, der einem Wert in einem Name-Wert-Paar zugeordnet ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="ea7c1-115">Gets or sets the name that is associated with a value in a name-value pair.</span></span><br/> |
| [<span data-ttu-id="ea7c1-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ea7c1-116">**Value**</span></span>](tasknamedvaluepair-value.md)<br/> | <span data-ttu-id="ea7c1-117">Ruft den Wert ab, der einem Namen in einem Name-Wert-Paar zugeordnet ist, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="ea7c1-117">Gets or sets the value that is associated with a name in a name-value pair.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea7c1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea7c1-118">Remarks</span></span>

<span data-ttu-id="ea7c1-119">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird ein Name-Wert-Paar mit dem [**valuequeries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="ea7c1-119">When reading or writing your own XML for a task, a name-value pair is specified using the [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea7c1-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea7c1-120">Requirements</span></span>



| <span data-ttu-id="ea7c1-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea7c1-121">Requirement</span></span> | <span data-ttu-id="ea7c1-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ea7c1-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea7c1-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea7c1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ea7c1-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea7c1-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ea7c1-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea7c1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ea7c1-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea7c1-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ea7c1-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ea7c1-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea7c1-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ea7c1-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ea7c1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ea7c1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea7c1-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea7c1-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea7c1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea7c1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea7c1-132">**Tasknamedvaluecollection**</span><span class="sxs-lookup"><span data-stu-id="ea7c1-132">**TaskNamedValueCollection**</span></span>](tasknamedvaluecollection.md)
</dt> </dl>

 

 





