---
title: Intervall Syntax
description: Stellt einen Zeitintervall Wert dar.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Intervall Syntax-AD-Schema
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104392242"
---
# <a name="interval-syntax"></a><span data-ttu-id="b7d09-104">Intervall Syntax</span><span class="sxs-lookup"><span data-stu-id="b7d09-104">Interval syntax</span></span>

<span data-ttu-id="b7d09-105">Stellt einen Zeitintervall Wert dar.</span><span class="sxs-lookup"><span data-stu-id="b7d09-105">Represents a time interval value.</span></span> <span data-ttu-id="b7d09-106">Die tatsächlichen Zeiteinheiten hängen davon ab, welches Attribut diese Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7d09-106">The actual time units depend on which attribute is using this syntax.</span></span> <span data-ttu-id="b7d09-107">Diese Syntax ist identisch mit der [**LargeInteger**](s-largeinteger.md) -Syntax, mit dem Unterschied, dass die hohen und niedrigen Werte ganze Zahlen ohne Vorzeichen sind.</span><span class="sxs-lookup"><span data-stu-id="b7d09-107">This syntax is identical to the [**LargeInteger**](s-largeinteger.md) syntax, except the high and low values are unsigned integers.</span></span>



| <span data-ttu-id="b7d09-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7d09-108">Entry</span></span> | <span data-ttu-id="b7d09-109">Wert</span><span class="sxs-lookup"><span data-stu-id="b7d09-109">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d09-110">Name</span><span class="sxs-lookup"><span data-stu-id="b7d09-110">Name</span></span>         | <span data-ttu-id="b7d09-111">Intervall</span><span class="sxs-lookup"><span data-stu-id="b7d09-111">Interval</span></span>                                                                           |
| <span data-ttu-id="b7d09-112">Syntax-ID</span><span class="sxs-lookup"><span data-stu-id="b7d09-112">Syntax ID</span></span>    | <span data-ttu-id="b7d09-113">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="b7d09-113">2.5.5.16</span></span>                                                                           |
| <span data-ttu-id="b7d09-114">OM-ID</span><span class="sxs-lookup"><span data-stu-id="b7d09-114">OM ID</span></span>        | <span data-ttu-id="b7d09-115">65</span><span class="sxs-lookup"><span data-stu-id="b7d09-115">65</span></span>                                                                                 |
| <span data-ttu-id="b7d09-116">MAPI-Typ</span><span class="sxs-lookup"><span data-stu-id="b7d09-116">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="b7d09-117">ADS-Typ</span><span class="sxs-lookup"><span data-stu-id="b7d09-117">ADS Type</span></span>     | <span data-ttu-id="b7d09-118">\_hohe Ganzzahl von adstype \_</span><span class="sxs-lookup"><span data-stu-id="b7d09-118">ADSTYPE\_LARGE\_INTEGER</span></span>                                                            |
| <span data-ttu-id="b7d09-119">Varianttyp</span><span class="sxs-lookup"><span data-stu-id="b7d09-119">Variant Type</span></span> | <span data-ttu-id="b7d09-120">VT \_ -Verteilung</span><span class="sxs-lookup"><span data-stu-id="b7d09-120">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="b7d09-121">SDS-Typ</span><span class="sxs-lookup"><span data-stu-id="b7d09-121">SDS Type</span></span>     | <span data-ttu-id="b7d09-122">Ein COM-Objekt, das in [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)umgewandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b7d09-122">A COM object that can be cast to an [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span></span> |



## <a name="see-also"></a><span data-ttu-id="b7d09-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7d09-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d09-124">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="b7d09-124">**IADsLargeInteger**</span></span>](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[<span data-ttu-id="b7d09-125">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="b7d09-125">**LargeInteger**</span></span>](s-largeinteger.md)
</dt> </dl>

 

 
