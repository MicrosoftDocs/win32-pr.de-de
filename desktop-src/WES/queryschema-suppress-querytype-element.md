---
title: Unterdrücken (QueryType)-Element
description: Eine XPath-Abfrage, die die aus dem Abfrageresultset auszuschließenden Ereignisse identifiziert.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Element EventLog unterdrücken
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106329"
---
# <a name="suppress-querytype-element"></a><span data-ttu-id="0f90d-104">Unterdrücken (QueryType)-Element</span><span class="sxs-lookup"><span data-stu-id="0f90d-104">Suppress (QueryType) Element</span></span>

<span data-ttu-id="0f90d-105">Eine XPath-Abfrage, die die aus dem Abfrageresultset auszuschließenden Ereignisse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0f90d-105">An XPath query that identifies the events to exclude from the query result set.</span></span>

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="0f90d-106">Das unter **drücken** -Element wird durch den komplexen [**QueryType**](queryschema-querytype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="0f90d-106">The **Suppress** element is defined by the [**QueryType**](queryschema-querytype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="0f90d-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="0f90d-107">Attributes</span></span>



| <span data-ttu-id="0f90d-108">Name</span><span class="sxs-lookup"><span data-stu-id="0f90d-108">Name</span></span> | <span data-ttu-id="0f90d-109">type</span><span class="sxs-lookup"><span data-stu-id="0f90d-109">Type</span></span>   | <span data-ttu-id="0f90d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f90d-110">Description</span></span>                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f90d-111">`Path`</span><span class="sxs-lookup"><span data-stu-id="0f90d-111">Path</span></span> | <span data-ttu-id="0f90d-112">anyURI</span><span class="sxs-lookup"><span data-stu-id="0f90d-112">anyURI</span></span> | <span data-ttu-id="0f90d-113">Der Name des Kanals oder der Pfad zu der Protokolldatei, in der die Ereignisse enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0f90d-113">The name of the channel or the path to the log file that contains the events.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0f90d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f90d-114">Requirements</span></span>



| <span data-ttu-id="0f90d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f90d-115">Requirement</span></span> | <span data-ttu-id="0f90d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0f90d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f90d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f90d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f90d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f90d-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f90d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f90d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f90d-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f90d-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0f90d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f90d-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f90d-122">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="0f90d-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="0f90d-123">**Query (querylisttype)**</span><span class="sxs-lookup"><span data-stu-id="0f90d-123">**Query (QueryListType)**</span></span>](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





