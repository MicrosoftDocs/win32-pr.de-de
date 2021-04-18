---
title: Komplexer keywordlisttype-Typ
description: Definiert eine Liste von Schlüsselwörtern zum Kategorisieren von Ereignissen. | Komplexer keywordlisttype-Typ
ms.assetid: 7aeb5ca1-b23f-40f5-a77b-894deaf9c6bb
keywords:
- Keywordlisttype, komplexer Typ EventLog
topic_type:
- apiref
api_name:
- KeywordListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7132e2e85015aaf9d38adbd6278ea4d3e1296446
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365262"
---
# <a name="keywordlisttype-complex-type"></a><span data-ttu-id="6284a-105">Komplexer keywordlisttype-Typ</span><span class="sxs-lookup"><span data-stu-id="6284a-105">KeywordListType Complex Type</span></span>

<span data-ttu-id="6284a-106">Definiert eine Liste von Schlüsselwörtern zum Kategorisieren von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="6284a-106">Defines a list of keywords that categorize events.</span></span>

``` syntax
<xs:complexType name="KeywordListType">
    <xs:sequence>
        <xs:element name="keyword"
            type="KeywordType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="6284a-107">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6284a-107">Child elements</span></span>



| <span data-ttu-id="6284a-108">Element</span><span class="sxs-lookup"><span data-stu-id="6284a-108">Element</span></span>                                                                | <span data-ttu-id="6284a-109">type</span><span class="sxs-lookup"><span data-stu-id="6284a-109">Type</span></span>                                                               | <span data-ttu-id="6284a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6284a-110">Description</span></span>                                                                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6284a-111">**Schlüsselwort**</span><span class="sxs-lookup"><span data-stu-id="6284a-111">**keyword**</span></span>](eventmanifestschema-keyword-keywordlisttype-element.md) | [<span data-ttu-id="6284a-112">**Keywordtype**</span><span class="sxs-lookup"><span data-stu-id="6284a-112">**KeywordType**</span></span>](eventmanifestschema-keywordtype-complextype.md) | <span data-ttu-id="6284a-113">Definiert ein Schlüsselwort, das eine Kategorie von Ereignissen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6284a-113">Defines a keyword that identifies a category of events.</span></span> <span data-ttu-id="6284a-114">Sie können maximal 48 Schlüsselwörter angeben.</span><span class="sxs-lookup"><span data-stu-id="6284a-114">You can specify a maximum of 48 keywords.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6284a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6284a-115">Requirements</span></span>



| <span data-ttu-id="6284a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6284a-116">Requirement</span></span> | <span data-ttu-id="6284a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6284a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6284a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6284a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6284a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6284a-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6284a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6284a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6284a-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6284a-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





