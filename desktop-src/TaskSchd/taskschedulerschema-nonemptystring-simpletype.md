---
title: nonemptystringtype simple-Typ
description: Definiert die Werte, die für eine nicht leere Text Zeichenfolge verwendet werden.
ms.assetid: cb3b1ca6-4531-467c-a27a-b27a62233514
keywords:
- nonEmptyString Simple Type Taskplaner
topic_type:
- apiref
api_name:
- nonEmptyString
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab9c9fa84c510fc4e67f6f63664a58d6d4093709
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392037"
---
# <a name="nonemptystringtype-simple-type"></a><span data-ttu-id="64e4f-104">nonemptystringtype simple-Typ</span><span class="sxs-lookup"><span data-stu-id="64e4f-104">nonEmptyStringType Simple Type</span></span>

<span data-ttu-id="64e4f-105">Definiert die Werte, die für eine nicht leere Text Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64e4f-105">Defines the values used for a non-empty string of text.</span></span>

``` syntax
<xs:simpleType name="nonEmptyString">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="1"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="64e4f-106">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="64e4f-106">Enumeration values</span></span>

<span data-ttu-id="64e4f-107">Der einfache Typ **nonEmptyString** definiert den folgenden Wert.</span><span class="sxs-lookup"><span data-stu-id="64e4f-107">The **nonEmptyString** simple type defines the following value.</span></span>



| <span data-ttu-id="64e4f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="64e4f-108">Value</span></span> | <span data-ttu-id="64e4f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64e4f-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="64e4f-110">1</span><span class="sxs-lookup"><span data-stu-id="64e4f-110">1</span></span>     | <span data-ttu-id="64e4f-111">Die Zeichenfolge enthält mindestens ein Zeichen.</span><span class="sxs-lookup"><span data-stu-id="64e4f-111">The string contains at least one character.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="64e4f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64e4f-112">Requirements</span></span>



| <span data-ttu-id="64e4f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64e4f-113">Requirement</span></span> | <span data-ttu-id="64e4f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="64e4f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="64e4f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64e4f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="64e4f-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64e4f-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="64e4f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64e4f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="64e4f-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64e4f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





