---
title: Komplexer patternmapvaluetype-Typ
description: Nicht verwendet. Definiert die regulären Ausdrücke, mit denen eine übereinstimmende Zeichenfolge in der Meldungs Zeichenfolge gesucht und geändert wird.
ms.assetid: 2ae8a268-64c0-45d1-8339-988b13d884a3
keywords:
- "\"Patternmapvaluetype\"-Ereignisprotokoll"
topic_type:
- apiref
api_name:
- PatternMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55b57b63f3e5c9e5a5c4cd15974c89f6d28439f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739729"
---
# <a name="patternmapvaluetype-complex-type"></a><span data-ttu-id="2b470-105">Komplexer patternmapvaluetype-Typ</span><span class="sxs-lookup"><span data-stu-id="2b470-105">PatternMapValueType Complex Type</span></span>

<span data-ttu-id="2b470-106">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b470-106">Not used.</span></span> <span data-ttu-id="2b470-107">Definiert die regulären Ausdrücke, mit denen eine übereinstimmende Zeichenfolge in der Meldungs Zeichenfolge gesucht und geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2b470-107">Defines the regular expressions used to find a matching string in the message string and alter it.</span></span>

``` syntax
<xs:complexType name="PatternMapValueType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="value"
                type="string"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="2b470-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2b470-108">Attributes</span></span>



| <span data-ttu-id="2b470-109">Name</span><span class="sxs-lookup"><span data-stu-id="2b470-109">Name</span></span>  | <span data-ttu-id="2b470-110">type</span><span class="sxs-lookup"><span data-stu-id="2b470-110">Type</span></span>   | <span data-ttu-id="2b470-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b470-111">Description</span></span>                                                                                               |
|-------|--------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b470-112">name</span><span class="sxs-lookup"><span data-stu-id="2b470-112">name</span></span>  | <span data-ttu-id="2b470-113">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b470-113">string</span></span> | <span data-ttu-id="2b470-114">Der reguläre Ausdruck, der zum Suchen einer übereinstimmenden Zeichenfolge in der Meldungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b470-114">The regular expression used to find a matching string in the message string.</span></span><br/>                   |
| <span data-ttu-id="2b470-115">value</span><span class="sxs-lookup"><span data-stu-id="2b470-115">value</span></span> | <span data-ttu-id="2b470-116">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b470-116">string</span></span> | <span data-ttu-id="2b470-117">Der reguläre Ausdruck zum Ändern der übereinstimmenden Zeichenfolge, die in der Meldungs Zeichenfolge gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2b470-117">The regular expression used to alter the matching string that was found in the message string.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2b470-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b470-118">Requirements</span></span>



| <span data-ttu-id="2b470-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b470-119">Requirement</span></span> | <span data-ttu-id="2b470-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2b470-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2b470-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b470-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b470-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b470-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2b470-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b470-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b470-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b470-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





