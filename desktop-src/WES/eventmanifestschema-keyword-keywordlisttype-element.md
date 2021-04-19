---
title: Schlüsselwort (keywordlisttype)-Element
description: Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen bezeichnet. | Schlüsselwort (keywordlisttype)-Element
ms.assetid: c921eb01-f1b0-455c-8ff9-06895f1e40f9
keywords:
- Schlüsselwort Element EventLog
topic_type:
- apiref
api_name:
- keyword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4b1b0b60502339db55c3227add9bb5a263200aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353308"
---
# <a name="keyword-keywordlisttype-element"></a><span data-ttu-id="97880-105">Schlüsselwort (keywordlisttype)-Element</span><span class="sxs-lookup"><span data-stu-id="97880-105">keyword (KeywordListType) Element</span></span>

<span data-ttu-id="97880-106">Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="97880-106">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="97880-107">Ein Schlüsselwort ist ein Tag, das Sie an ein Ereignis anfügen, um Ereignisse auf der Grundlage ihrer Verwendung zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="97880-107">A keyword is a tag that you attach to an event to group events based on their usage.</span></span>

``` syntax
<xs:element name="keyword"
    type="KeywordType"
 />
```

<span data-ttu-id="97880-108">Das **Schlüsselwort** Element wird durch den komplexen Typ [**keywordlisttype**](eventmanifestschema-keywordlisttype-complextype.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="97880-108">The **keyword** element is defined by the [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="97880-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97880-109">Requirements</span></span>



| <span data-ttu-id="97880-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97880-110">Requirement</span></span> | <span data-ttu-id="97880-111">Wert</span><span class="sxs-lookup"><span data-stu-id="97880-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97880-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97880-112">Minimum supported client</span></span><br/> | <span data-ttu-id="97880-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97880-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="97880-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97880-114">Minimum supported server</span></span><br/> | <span data-ttu-id="97880-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97880-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97880-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97880-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="97880-117">**Übergeordnete Elemente**</span><span class="sxs-lookup"><span data-stu-id="97880-117">**Parent elements**</span></span>
</dt> <dt>

[<span data-ttu-id="97880-118">**Schlüsselwörter (ProviderType)**</span><span class="sxs-lookup"><span data-stu-id="97880-118">**keywords (ProviderType)**</span></span>](eventmanifestschema-keywords-providertype-element.md)
</dt> <dt>

[<span data-ttu-id="97880-119">**Schlüsselwörter (metadataType)**</span><span class="sxs-lookup"><span data-stu-id="97880-119">**keywords (MetadataType)**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)
</dt> </dl>

 

 





