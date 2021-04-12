---
title: Komplexer Typ von patternmaplisttype
description: Nicht verwendet. Definiert eine Liste von Paaren für reguläre Ausdrücke, die zum Ändern der Meldungs Zeichenfolge verwendet werden.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- Datentyp "patternmaplisttype", Ereignisprotokoll
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340307"
---
# <a name="patternmaplisttype-complex-type"></a><span data-ttu-id="c5ce8-105">Komplexer Typ von patternmaplisttype</span><span class="sxs-lookup"><span data-stu-id="c5ce8-105">PatternMapListType Complex Type</span></span>

<span data-ttu-id="c5ce8-106">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5ce8-106">Not used.</span></span> <span data-ttu-id="c5ce8-107">Definiert eine Liste von Paaren für reguläre Ausdrücke, die zum Ändern der Meldungs Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5ce8-107">Defines a list of regular expression pairs that are used to alter the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c5ce8-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c5ce8-108">Child elements</span></span>



| <span data-ttu-id="c5ce8-109">Element</span><span class="sxs-lookup"><span data-stu-id="c5ce8-109">Element</span></span>                                                                         | <span data-ttu-id="c5ce8-110">type</span><span class="sxs-lookup"><span data-stu-id="c5ce8-110">Type</span></span>                                                                     | <span data-ttu-id="c5ce8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5ce8-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5ce8-112">**patternmap**</span><span class="sxs-lookup"><span data-stu-id="c5ce8-112">**patternMap**</span></span>](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [<span data-ttu-id="c5ce8-113">**Patternmaptype**</span><span class="sxs-lookup"><span data-stu-id="c5ce8-113">**PatternMapType**</span></span>](eventmanifestschema-patternmaptype-complextype.md) | <span data-ttu-id="c5ce8-114">Definiert eine Zuordnung zwischen zwei regulären Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="c5ce8-114">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="c5ce8-115">Ein Ausdruck wird verwendet, um nach einer übereinstimmenden Zeichenfolge in der Meldungs Zeichenfolge zu suchen, und die andere wird verwendet, um die Zeichenfolge zu ändern</span><span class="sxs-lookup"><span data-stu-id="c5ce8-115">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span> <span data-ttu-id="c5ce8-116">Die erste übereinstimmende Musterzuordnung wird verwendet, und andere Muster werden nicht ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="c5ce8-116">The first pattern mapping that matches is used and other patterns are not tried.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c5ce8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5ce8-117">Requirements</span></span>



| <span data-ttu-id="c5ce8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5ce8-118">Requirement</span></span> | <span data-ttu-id="c5ce8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c5ce8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5ce8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5ce8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ce8-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5ce8-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5ce8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5ce8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ce8-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5ce8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





