---
title: Komplexer QueryType-Typ
description: Definiert einen Satz von Auswahl-und Unterdrückungs Abfragen, die verwendet werden, um Ereignisse in das Resultset einzuschließen oder Ereignisse aus dem Resultset auszuschließen.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- QueryType Complex-Typ EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103575"
---
# <a name="querytype-complex-type"></a><span data-ttu-id="0c23e-104">Komplexer QueryType-Typ</span><span class="sxs-lookup"><span data-stu-id="0c23e-104">QueryType Complex Type</span></span>

<span data-ttu-id="0c23e-105">Definiert einen Satz von Auswahl-und Unterdrückungs Abfragen, die verwendet werden, um Ereignisse in das Resultset einzuschließen oder Ereignisse aus dem Resultset auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="0c23e-105">Defines a set of selector and suppressor queries that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0c23e-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0c23e-106">Child elements</span></span>



| <span data-ttu-id="0c23e-107">Element</span><span class="sxs-lookup"><span data-stu-id="0c23e-107">Element</span></span>                                                    | <span data-ttu-id="0c23e-108">type</span><span class="sxs-lookup"><span data-stu-id="0c23e-108">Type</span></span> | <span data-ttu-id="0c23e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c23e-109">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c23e-110">**Select**</span><span class="sxs-lookup"><span data-stu-id="0c23e-110">**Select**</span></span>](queryschema-select-querytype-element.md)     |      | <span data-ttu-id="0c23e-111">Eine XPath-Abfrage, die die Ereignisse identifiziert, die im Resultset der Abfrage enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="0c23e-111">An XPath query that identifies the events to include in the query result set.</span></span> <span data-ttu-id="0c23e-112">Geben Sie den XPath im Textkörper dieses Elements an.</span><span class="sxs-lookup"><span data-stu-id="0c23e-112">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="0c23e-113">Der XPath ist auf 32-Ausdrücke beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0c23e-113">The XPath is limited to 32 expressions.</span></span><br/>   |
| [<span data-ttu-id="0c23e-114">**Suppress**</span><span class="sxs-lookup"><span data-stu-id="0c23e-114">**Suppress**</span></span>](queryschema-suppress-querytype-element.md) |      | <span data-ttu-id="0c23e-115">Eine XPath-Abfrage, die die aus dem Abfrageresultset auszuschließenden Ereignisse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0c23e-115">An XPath query that identifies the events to exclude from the query result set.</span></span> <span data-ttu-id="0c23e-116">Geben Sie den XPath im Textkörper dieses Elements an.</span><span class="sxs-lookup"><span data-stu-id="0c23e-116">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="0c23e-117">Der XPath ist auf 32-Ausdrücke beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0c23e-117">The XPath is limited to 32 expressions.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0c23e-118">Attributes</span><span class="sxs-lookup"><span data-stu-id="0c23e-118">Attributes</span></span>



| <span data-ttu-id="0c23e-119">Name</span><span class="sxs-lookup"><span data-stu-id="0c23e-119">Name</span></span> | <span data-ttu-id="0c23e-120">type</span><span class="sxs-lookup"><span data-stu-id="0c23e-120">Type</span></span>   | <span data-ttu-id="0c23e-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c23e-121">Description</span></span>                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c23e-122">Id</span><span class="sxs-lookup"><span data-stu-id="0c23e-122">Id</span></span>   | <span data-ttu-id="0c23e-123">long</span><span class="sxs-lookup"><span data-stu-id="0c23e-123">long</span></span>   | <span data-ttu-id="0c23e-124">Ein Bezeichner, der diese Abfrage in der Liste der Abfragen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0c23e-124">An identifier that uniquely identifies this query in your list of queries.</span></span> <span data-ttu-id="0c23e-125">Der Bezeichner ist NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="0c23e-125">The identifier is zero-based.</span></span> <span data-ttu-id="0c23e-126">Sie müssen einen Bezeichner angeben, wenn die Abfrage Liste mehr als eine Abfrage enthält.</span><span class="sxs-lookup"><span data-stu-id="0c23e-126">You must specify an identifier if your query list contains more than one query.</span></span><br/> |
| <span data-ttu-id="0c23e-127">Pfad</span><span class="sxs-lookup"><span data-stu-id="0c23e-127">Path</span></span> | <span data-ttu-id="0c23e-128">anyURI</span><span class="sxs-lookup"><span data-stu-id="0c23e-128">anyURI</span></span> | <span data-ttu-id="0c23e-129">Der Name des Kanals oder der Pfad zu der Protokolldatei, in der die Ereignisse enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0c23e-129">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="0c23e-130">Pfad</span><span class="sxs-lookup"><span data-stu-id="0c23e-130">Path</span></span> | <span data-ttu-id="0c23e-131">anyURI</span><span class="sxs-lookup"><span data-stu-id="0c23e-131">anyURI</span></span> | <span data-ttu-id="0c23e-132">Der Name des Kanals oder der Pfad zu der Protokolldatei, in der die Ereignisse enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0c23e-132">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="0c23e-133">Pfad</span><span class="sxs-lookup"><span data-stu-id="0c23e-133">Path</span></span> | <span data-ttu-id="0c23e-134">anyURI</span><span class="sxs-lookup"><span data-stu-id="0c23e-134">anyURI</span></span> | <span data-ttu-id="0c23e-135">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c23e-135">Not used.</span></span><br/>                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="0c23e-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c23e-136">Remarks</span></span>

<span data-ttu-id="0c23e-137">Die Abfrage muss mindestens eine SELECT-Anweisung enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c23e-137">The query must have at least one select statement.</span></span> <span data-ttu-id="0c23e-138">Für jede unterdrückte Anweisung muss mindestens eine SELECT-Anweisung vorhanden sein, die denselben Pfad angibt.</span><span class="sxs-lookup"><span data-stu-id="0c23e-138">For each suppress statement, there must be at least one select statement that specifies the same path.</span></span> <span data-ttu-id="0c23e-139">Wenn die SELECT-und Unterdrückung-Abfrage dieselben Ereignisse zurückgibt, hat die Unterdrückung-Anweisung Vorrang.</span><span class="sxs-lookup"><span data-stu-id="0c23e-139">If the select and suppress query return the same events, the suppress statement takes precedence.</span></span> <span data-ttu-id="0c23e-140">Wenn Sie Ereignisse aus mehreren Quellen auswählen, werden die Ereignisse in der Reihenfolge der Zeitstempel zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c23e-140">If you select events from multiple sources, the events are returned in time stamp order.</span></span> <span data-ttu-id="0c23e-141">Wenn Sie den Systemzeitstempel verwenden und die Rate der Ereignisse hoch ist, kann es vorkommen, dass mehr als ein Ereignis denselben Zeitstempel hat.</span><span class="sxs-lookup"><span data-stu-id="0c23e-141">If you use the system time stamp and the rate of events is high, it is possible that more than one event will have the same time stamp.</span></span> <span data-ttu-id="0c23e-142">Wenn dies auftritt, wird die Reihenfolge von Ereignissen mehrdeutig, und die Ereignisse werden möglicherweise nicht in der richtigen Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c23e-142">When this occurs, the ordering of events becomes ambiguous and the events may appear out of order.</span></span>

<span data-ttu-id="0c23e-143">Wenn Sie einen Pfad für eine der Abfragen in der Abfrage Liste angeben, muss für alle Abfragen ein Pfad angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0c23e-143">If you specify a path for one of the queries in the list of queries, all of the queries must specify a path.</span></span> <span data-ttu-id="0c23e-144">Wenn Sie keinen Pfad für alle Abfragen angeben, müssen Sie den Pfad angeben, wenn Sie die [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) -oder [**evtsubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0c23e-144">If you do not specify a path for all of the queries, you must specify the path when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c23e-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c23e-145">Requirements</span></span>



| <span data-ttu-id="0c23e-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c23e-146">Requirement</span></span> | <span data-ttu-id="0c23e-147">Wert</span><span class="sxs-lookup"><span data-stu-id="0c23e-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c23e-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c23e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0c23e-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c23e-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c23e-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c23e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0c23e-151">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c23e-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





