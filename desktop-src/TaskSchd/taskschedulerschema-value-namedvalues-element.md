---
title: Value (namedValues)-Element
description: Enthält den Wert, der einem Namen in einem Name-Wert-Paar zugeordnet ist.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Value-Element Taskplaner
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743320"
---
# <a name="value-namedvalues-element"></a><span data-ttu-id="a823a-104">Value (namedValues)-Element</span><span class="sxs-lookup"><span data-stu-id="a823a-104">Value (namedValues) Element</span></span>

<span data-ttu-id="a823a-105">Enthält den Wert, der einem Namen in einem Name-Wert-Paar zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a823a-105">Contains the value that is associated with a name in a name-value pair.</span></span>

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

<span data-ttu-id="a823a-106">Das **value** -Element wird durch den komplexen [**namedValues**](taskschedulerschema-namedvalues-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="a823a-106">The **Value** element is defined by the [**namedValues**](taskschedulerschema-namedvalues-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a823a-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="a823a-107">Parent element</span></span>



| <span data-ttu-id="a823a-108">Element</span><span class="sxs-lookup"><span data-stu-id="a823a-108">Element</span></span>                                                                                              | <span data-ttu-id="a823a-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="a823a-109">Derived from</span></span>                                                       | <span data-ttu-id="a823a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a823a-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a823a-111">**Valuequeries (eventtriggertype)**</span><span class="sxs-lookup"><span data-stu-id="a823a-111">**ValueQueries (eventTriggerType)**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="a823a-112">**namedValues**</span><span class="sxs-lookup"><span data-stu-id="a823a-112">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md) | <span data-ttu-id="a823a-113">Gibt eine Auflistung von benannten XPath-Abfragen an.</span><span class="sxs-lookup"><span data-stu-id="a823a-113">Specifies a collection of named XPath queries.</span></span> <span data-ttu-id="a823a-114">Jede Abfrage in der Auflistung wird auf das letzte übereinstimmende Ereignis-XML angewendet, das von der Abonnement Abfrage zurückgegeben wird, die im [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) -Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a823a-114">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="a823a-115">Der Name der Abfrage kann als Variable in der Nachricht einer ShowMessage-Aktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a823a-115">The name of the query can be used as a variable in the message of a ShowMessage action.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a823a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a823a-116">Remarks</span></span>

<span data-ttu-id="a823a-117">Informationen zur C++-Entwicklung finden Sie unter [**Value-Eigenschaft von itasknamedvaluepair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span><span class="sxs-lookup"><span data-stu-id="a823a-117">For C++ development, see [**Value Property of ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span></span>

<span data-ttu-id="a823a-118">Informationen zur Skript Entwicklung finden Sie unter [**tasknamedvaluepair. Value**](tasknamedvaluepair-value.md).</span><span class="sxs-lookup"><span data-stu-id="a823a-118">For script development, see [**TaskNamedValuePair.Value**](tasknamedvaluepair-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a823a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a823a-119">Requirements</span></span>



| <span data-ttu-id="a823a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a823a-120">Requirement</span></span> | <span data-ttu-id="a823a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a823a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a823a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a823a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a823a-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a823a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a823a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a823a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a823a-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a823a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





