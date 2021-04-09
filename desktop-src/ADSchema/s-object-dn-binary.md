---
title: Object (DN-Binary)-Syntax
description: Eine Oktett-Zeichenfolge, die einen binären Wert und einen Distinguished Name (DN) enthält.
ms.assetid: 1d7efc17-a99a-41bf-9812-9e8a2b2b6644
ms.tgt_platform: multiple
keywords:
- Objekt Syntax (DN-Binary) AD-Schema
topic_type:
- apiref
api_name:
- Object(DN-Binary)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e96f640ad729f203362df906bcc6afe6b82e7e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106701"
---
# <a name="objectdn-binary-syntax"></a><span data-ttu-id="f477d-104">Object (DN-Binary)-Syntax</span><span class="sxs-lookup"><span data-stu-id="f477d-104">Object(DN-Binary) syntax</span></span>

<span data-ttu-id="f477d-105">Eine Oktett-Zeichenfolge, die einen binären Wert und einen Distinguished Name (DN) enthält.</span><span class="sxs-lookup"><span data-stu-id="f477d-105">An octet string that contains a binary value and a distinguished name (DN).</span></span>



| <span data-ttu-id="f477d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f477d-106">Entry</span></span> | <span data-ttu-id="f477d-107">Wert</span><span class="sxs-lookup"><span data-stu-id="f477d-107">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f477d-108">Name</span><span class="sxs-lookup"><span data-stu-id="f477d-108">Name</span></span>         | <span data-ttu-id="f477d-109">Object(DN-Binary)</span><span class="sxs-lookup"><span data-stu-id="f477d-109">Object(DN-Binary)</span></span>                                                                  |
| <span data-ttu-id="f477d-110">Syntax-ID</span><span class="sxs-lookup"><span data-stu-id="f477d-110">Syntax ID</span></span>    | <span data-ttu-id="f477d-111">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="f477d-111">2.5.5.7</span></span>                                                                            |
| <span data-ttu-id="f477d-112">OM-ID</span><span class="sxs-lookup"><span data-stu-id="f477d-112">OM ID</span></span>        | <span data-ttu-id="f477d-113">127</span><span class="sxs-lookup"><span data-stu-id="f477d-113">127</span></span>                                                                                |
| <span data-ttu-id="f477d-114">MAPI-Typ</span><span class="sxs-lookup"><span data-stu-id="f477d-114">MAPI Type</span></span>    | <span data-ttu-id="f477d-115">TString</span><span class="sxs-lookup"><span data-stu-id="f477d-115">TSTRING</span></span>                                                                            |
| <span data-ttu-id="f477d-116">ADS-Typ</span><span class="sxs-lookup"><span data-stu-id="f477d-116">ADS Type</span></span>     | <span data-ttu-id="f477d-117">adstype \_ DN \_ mit \_ Binär</span><span class="sxs-lookup"><span data-stu-id="f477d-117">ADSTYPE\_DN\_WITH\_BINARY</span></span>                                                          |
| <span data-ttu-id="f477d-118">Varianttyp</span><span class="sxs-lookup"><span data-stu-id="f477d-118">Variant Type</span></span> | <span data-ttu-id="f477d-119">VT \_ -Verteilung</span><span class="sxs-lookup"><span data-stu-id="f477d-119">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="f477d-120">SDS-Typ</span><span class="sxs-lookup"><span data-stu-id="f477d-120">SDS Type</span></span>     | <span data-ttu-id="f477d-121">Ein COM-Objekt, das in [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)umgewandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f477d-121">A COM object that can be cast to an [**IADsDNWithBinary**](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary).</span></span> |



## <a name="remarks"></a><span data-ttu-id="f477d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f477d-122">Remarks</span></span>

<span data-ttu-id="f477d-123">Ein Wert mit dieser Syntax weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="f477d-123">A value with this syntax has the following format:</span></span>

``` syntax
B:<char count>:<binary value>:<object DN>
```

<span data-ttu-id="f477d-124">Dabei ist " &lt; char Count &gt; " die Anzahl von hexadezimalen Ziffern im " &lt; binären Wert &gt; ", " &lt; Binärwert &gt; " ist die hexadezimale Darstellung des binären Werts, und " &lt; Object DN &gt; " ist ein definierter Name.</span><span class="sxs-lookup"><span data-stu-id="f477d-124">where "&lt;char count&gt;" is the number of hexadecimal digits in "&lt;binary value&gt;", "&lt;binary value&gt;" is the hexadecimal representation of the binary value, and "&lt;object DN&gt;" is a distinguished name.</span></span> <span data-ttu-id="f477d-125">Active Directory aktualisiert den DN automatisch, wenn das Objekt, auf das es verweist, verschoben oder umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="f477d-125">Active Directory automatically updates the DN if the object that it refers to is moved or renamed.</span></span> <span data-ttu-id="f477d-126">Weitere Informationen und ein Codebeispiel, in dem diese Syntax verwendet wird, finden Sie unter [Aktivieren der Umbenennungs sicheren Bindung mit der otherWellKnownObjects-Eigenschaft](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span><span class="sxs-lookup"><span data-stu-id="f477d-126">For more information and a code example that uses this syntax, see [Enabling Rename-safe Binding with the otherWellKnownObjects Property](/windows/desktop/AD/enabling-rename-safe-binding-with-the-otherwellknownobjects-property).</span></span>

## <a name="see-also"></a><span data-ttu-id="f477d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f477d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f477d-128">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="f477d-128">**IADsDNWithBinary**</span></span>](/windows/desktop/api/iads/nn-iads-iadsdnwithbinary)
</dt> </dl>

 

 
