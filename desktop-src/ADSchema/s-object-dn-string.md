---
title: Object (DN-String)-Syntax
description: Eine Oktett-Zeichenfolge, die einen Zeichen folgen Wert und einen DN enthält.
ms.assetid: 7a5ce9f3-ac97-4936-868a-6b18f202972f
ms.tgt_platform: multiple
keywords:
- AD-Schema der Object (DN-String)-Syntax
topic_type:
- apiref
api_name:
- Object(DN-String)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 823da21325abdc426d5f58df4cdf04de19fc68b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342678"
---
# <a name="objectdn-string-syntax"></a><span data-ttu-id="69ad9-104">Object (DN-String)-Syntax</span><span class="sxs-lookup"><span data-stu-id="69ad9-104">Object(DN-String) syntax</span></span>

<span data-ttu-id="69ad9-105">Eine Oktett-Zeichenfolge, die einen Zeichen folgen Wert und einen DN enthält.</span><span class="sxs-lookup"><span data-stu-id="69ad9-105">An octet string that contains a string value and a DN.</span></span>



| <span data-ttu-id="69ad9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="69ad9-106">Entry</span></span> | <span data-ttu-id="69ad9-107">Wert</span><span class="sxs-lookup"><span data-stu-id="69ad9-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69ad9-108">Name</span><span class="sxs-lookup"><span data-stu-id="69ad9-108">Name</span></span>         | <span data-ttu-id="69ad9-109">Object(DN-String)</span><span class="sxs-lookup"><span data-stu-id="69ad9-109">Object(DN-String)</span></span>                                                                  |
| <span data-ttu-id="69ad9-110">Syntax-ID</span><span class="sxs-lookup"><span data-stu-id="69ad9-110">Syntax ID</span></span>    | <span data-ttu-id="69ad9-111">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="69ad9-111">2.5.5.14</span></span>                                                                           |
| <span data-ttu-id="69ad9-112">OM-ID</span><span class="sxs-lookup"><span data-stu-id="69ad9-112">OM ID</span></span>        | <span data-ttu-id="69ad9-113">127</span><span class="sxs-lookup"><span data-stu-id="69ad9-113">127</span></span>                                                                                |
| <span data-ttu-id="69ad9-114">MAPI-Typ</span><span class="sxs-lookup"><span data-stu-id="69ad9-114">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="69ad9-115">ADS-Typ</span><span class="sxs-lookup"><span data-stu-id="69ad9-115">ADS Type</span></span>     | <span data-ttu-id="69ad9-116">adstype \_ DN \_ mit \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="69ad9-116">ADSTYPE\_DN\_WITH\_STRING</span></span>                                                          |
| <span data-ttu-id="69ad9-117">Varianttyp</span><span class="sxs-lookup"><span data-stu-id="69ad9-117">Variant Type</span></span> | <span data-ttu-id="69ad9-118">VT \_ -Verteilung</span><span class="sxs-lookup"><span data-stu-id="69ad9-118">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="69ad9-119">SDS-Typ</span><span class="sxs-lookup"><span data-stu-id="69ad9-119">SDS Type</span></span>     | <span data-ttu-id="69ad9-120">Ein COM-Objekt, das in ein [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)-Objekt umgewandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="69ad9-120">A COM object that can be cast to an [**IADsDNWithString**](/windows/desktop/api/iads/nn-iads-iadsdnwithstring).</span></span> |



## <a name="remarks"></a><span data-ttu-id="69ad9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69ad9-121">Remarks</span></span>

<span data-ttu-id="69ad9-122">Ein Wert mit dieser Syntax weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="69ad9-122">A value with this syntax has the following format:</span></span>

``` syntax
S:<char count>:<string value>:<object DN>
```

<span data-ttu-id="69ad9-123">&lt;dabei ist "char Count &gt; " die Anzahl von Zeichen in der Zeichen &lt; Folge "String value &gt; " und " &lt; Object DN &gt; " ein definierter Name eines Objekts in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="69ad9-123">where "&lt;char count&gt;" is the number of characters in the "&lt;string value&gt;" string, and "&lt;object DN&gt;" is a distinguished name of an object in Active Directory.</span></span> <span data-ttu-id="69ad9-124">Active Directory aktualisiert den DN, wenn das Objekt, auf das verwiesen wird, verschoben oder umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="69ad9-124">Active Directory updates the DN if the object that it refers to is moved or renamed.</span></span>

## <a name="see-also"></a><span data-ttu-id="69ad9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69ad9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69ad9-126">**IADsDNWithString**</span><span class="sxs-lookup"><span data-stu-id="69ad9-126">**IADsDNWithString**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithstring)
</dt> </dl>

 

 
