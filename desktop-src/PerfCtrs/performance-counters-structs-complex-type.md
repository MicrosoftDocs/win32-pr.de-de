---
description: Definiert eine Liste von-Strukturen, die Gegenwerte enthalten.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: komplexer Strukturen-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362226"
---
# <a name="structs-complex-type"></a><span data-ttu-id="b7385-103">komplexer Strukturen-Typ</span><span class="sxs-lookup"><span data-stu-id="b7385-103">structs Complex Type</span></span>

<span data-ttu-id="b7385-104">Definiert eine Liste von-Strukturen, die Gegenwerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="b7385-104">Defines a list of structures that contain counter values.</span></span>

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b7385-105">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b7385-105">Child elements</span></span>



| <span data-ttu-id="b7385-106">Element</span><span class="sxs-lookup"><span data-stu-id="b7385-106">Element</span></span>    | <span data-ttu-id="b7385-107">type</span><span class="sxs-lookup"><span data-stu-id="b7385-107">Type</span></span>                                                           | <span data-ttu-id="b7385-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7385-108">Description</span></span>                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="b7385-109">**struct**</span><span class="sxs-lookup"><span data-stu-id="b7385-109">**struct**</span></span> | [<span data-ttu-id="b7385-110">**man: struct**</span><span class="sxs-lookup"><span data-stu-id="b7385-110">**man:struct**</span></span>](performance-counters-struct-complex-type.md) | <span data-ttu-id="b7385-111">Der Name einer-Struktur, die die Werte für den Zählers enthält.</span><span class="sxs-lookup"><span data-stu-id="b7385-111">The name of a structure that contains counter values.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b7385-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7385-112">Requirements</span></span>



| <span data-ttu-id="b7385-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7385-113">Requirement</span></span> | <span data-ttu-id="b7385-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b7385-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b7385-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7385-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b7385-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7385-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b7385-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7385-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b7385-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7385-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




