---
title: Select (QueryType)-Element
description: Eine XPath-Abfrage, die die Ereignisse identifiziert, die im Resultset der Abfrage enthalten sein sollen.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Element "EventLog" auswählen
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392156"
---
# <a name="select-querytype-element"></a><span data-ttu-id="fd186-104">Select (QueryType)-Element</span><span class="sxs-lookup"><span data-stu-id="fd186-104">Select (QueryType) Element</span></span>

<span data-ttu-id="fd186-105">Eine XPath-Abfrage, die die Ereignisse identifiziert, die im Resultset der Abfrage enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="fd186-105">An XPath query that identifies the events to include in the query result set.</span></span>

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="fd186-106">Das **Select** -Element wird durch den komplexen Typ [**QueryType**](queryschema-querytype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="fd186-106">The **Select** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="fd186-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="fd186-107">Attributes</span></span>



| <span data-ttu-id="fd186-108">Name</span><span class="sxs-lookup"><span data-stu-id="fd186-108">Name</span></span> | <span data-ttu-id="fd186-109">type</span><span class="sxs-lookup"><span data-stu-id="fd186-109">Type</span></span>   | <span data-ttu-id="fd186-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd186-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd186-111">`Path`</span><span class="sxs-lookup"><span data-stu-id="fd186-111">Path</span></span> | <span data-ttu-id="fd186-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="fd186-112">anyURI</span></span> | <span data-ttu-id="fd186-113">Der Name des Kanals oder der Pfad zu der Protokolldatei, in der die Ereignisse enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fd186-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fd186-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd186-114">Requirements</span></span>



| <span data-ttu-id="fd186-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd186-115">Requirement</span></span> | <span data-ttu-id="fd186-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fd186-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="fd186-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd186-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fd186-118">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fd186-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="fd186-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd186-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fd186-120">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="fd186-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd186-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd186-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd186-122">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="fd186-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="fd186-123">**Query (querylisttype)**</span><span class="sxs-lookup"><span data-stu-id="fd186-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





