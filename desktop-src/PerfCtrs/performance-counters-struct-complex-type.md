---
description: Definiert eine-Struktur, die einen oder mehrere-Werte enthält.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: komplexer Strukturtyp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348013"
---
# <a name="struct-complex-type"></a><span data-ttu-id="92c17-103">komplexer Strukturtyp</span><span class="sxs-lookup"><span data-stu-id="92c17-103">struct Complex Type</span></span>

<span data-ttu-id="92c17-104">Definiert eine-Struktur, die einen oder mehrere-Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="92c17-104">Defines a structure that contains one or more counter values.</span></span>

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="92c17-105">Attributes</span><span class="sxs-lookup"><span data-stu-id="92c17-105">Attributes</span></span>



| <span data-ttu-id="92c17-106">Name</span><span class="sxs-lookup"><span data-stu-id="92c17-106">Name</span></span> | <span data-ttu-id="92c17-107">type</span><span class="sxs-lookup"><span data-stu-id="92c17-107">Type</span></span>                                                                    | <span data-ttu-id="92c17-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92c17-108">Description</span></span>                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92c17-109">name</span><span class="sxs-lookup"><span data-stu-id="92c17-109">name</span></span> | [<span data-ttu-id="92c17-110">**man: csymboltype**</span><span class="sxs-lookup"><span data-stu-id="92c17-110">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="92c17-111">Der Name der Struktur.</span><span class="sxs-lookup"><span data-stu-id="92c17-111">The name of the structure.</span></span><br/>                                                                                                            |
| <span data-ttu-id="92c17-112">type</span><span class="sxs-lookup"><span data-stu-id="92c17-112">type</span></span> | [<span data-ttu-id="92c17-113">**man: csymboltype**</span><span class="sxs-lookup"><span data-stu-id="92c17-113">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="92c17-114">Ein symbolischer Name, der die-Struktur bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="92c17-114">A symbolic name that identifies the structure.</span></span> <span data-ttu-id="92c17-115">Das [ctrpp](ctrpp.md) -Tool erstellt eine Struktur Variable mit diesem Namen, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="92c17-115">The [CTRPP](ctrpp.md) tool creates a struct variable with this name that you can use.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="92c17-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92c17-116">Requirements</span></span>



| <span data-ttu-id="92c17-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92c17-117">Requirement</span></span> | <span data-ttu-id="92c17-118">Wert</span><span class="sxs-lookup"><span data-stu-id="92c17-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92c17-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92c17-119">Minimum supported client</span></span><br/> | <span data-ttu-id="92c17-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92c17-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92c17-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92c17-121">Minimum supported server</span></span><br/> | <span data-ttu-id="92c17-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92c17-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




