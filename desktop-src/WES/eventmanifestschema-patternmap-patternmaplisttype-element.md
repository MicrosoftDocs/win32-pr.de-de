---
title: patternmap (patternmaplisttype)-Element
description: Definiert eine Zuordnung zwischen zwei regulären Ausdrücken. Ein Ausdruck wird verwendet, um eine übereinstimmende Zeichenfolge in der Meldungs Zeichenfolge zu finden, und die andere wird verwendet, um die Zeichenfolge zu ändern
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- patternmap-Element EventLog
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040036"
---
# <a name="patternmap-patternmaplisttype-element"></a><span data-ttu-id="d8d5b-105">patternmap (patternmaplisttype)-Element</span><span class="sxs-lookup"><span data-stu-id="d8d5b-105">patternMap (PatternMapListType) Element</span></span>

<span data-ttu-id="d8d5b-106">Definiert eine Zuordnung zwischen zwei regulären Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="d8d5b-106">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="d8d5b-107">Ein Ausdruck wird verwendet, um eine übereinstimmende Zeichenfolge in der Meldungs Zeichenfolge zu finden, und die andere wird verwendet, um die Zeichenfolge zu ändern</span><span class="sxs-lookup"><span data-stu-id="d8d5b-107">One expression is used to find a matching string in the message string, and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

<span data-ttu-id="d8d5b-108">Das **patternmap** -Element wird durch den komplexen Typ " [**patternmaplisttype**](eventmanifestschema-patternmaplisttype-complextype.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="d8d5b-108">The **patternMap** element is defined by the [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d5b-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8d5b-109">Requirements</span></span>



| <span data-ttu-id="d8d5b-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8d5b-110">Requirement</span></span> | <span data-ttu-id="d8d5b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d8d5b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8d5b-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8d5b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d8d5b-113">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8d5b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8d5b-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8d5b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d8d5b-115">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8d5b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8d5b-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8d5b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8d5b-117">**Übergeordnetes Element**</span><span class="sxs-lookup"><span data-stu-id="d8d5b-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="d8d5b-118">**patternmaps (namedquerytype)**</span><span class="sxs-lookup"><span data-stu-id="d8d5b-118">**patternMaps (NamedQueryType)**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





