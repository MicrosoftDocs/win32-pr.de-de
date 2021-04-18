---
title: Komplexer querylisttype-Typ
description: Definiert eine Liste von Abfragen, die eine Reihe von Selektoren und Unterdrückern enthalten können, mit denen Ereignisse in das Resultset eingeschlossen oder daraus ausgeschlossen werden.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- Querylisttype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338538"
---
# <a name="querylisttype-complex-type"></a><span data-ttu-id="d056f-104">Komplexer querylisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="d056f-104">QueryListType Complex Type</span></span>

<span data-ttu-id="d056f-105">Definiert eine Liste von Abfragen, die eine Reihe von Selektoren und Unterdrückern enthalten können, mit denen Ereignisse in das Resultset eingeschlossen oder daraus ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d056f-105">Defines a list of queries that can contain a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d056f-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d056f-106">Child elements</span></span>



| <span data-ttu-id="d056f-107">Element</span><span class="sxs-lookup"><span data-stu-id="d056f-107">Element</span></span>                                                  | <span data-ttu-id="d056f-108">type</span><span class="sxs-lookup"><span data-stu-id="d056f-108">Type</span></span>                                                   | <span data-ttu-id="d056f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d056f-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d056f-110">**Query**</span><span class="sxs-lookup"><span data-stu-id="d056f-110">**Query**</span></span>](queryschema-query-querylisttype-element.md) | [<span data-ttu-id="d056f-111">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="d056f-111">**QueryType**</span></span>](queryschema-querytype-complextype.md) | <span data-ttu-id="d056f-112">Definiert einen Satz von Selektoren und Unterdrückern, die verwendet werden, um Ereignisse in das Resultset einzuschließen oder Ereignisse aus dem Resultset auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="d056f-112">Defines a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d056f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d056f-113">Requirements</span></span>



| <span data-ttu-id="d056f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d056f-114">Requirement</span></span> | <span data-ttu-id="d056f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d056f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d056f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d056f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d056f-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d056f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d056f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d056f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d056f-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d056f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





