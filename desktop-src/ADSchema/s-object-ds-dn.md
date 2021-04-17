---
title: Object (DS-DN)-Syntax
description: Eine Zeichenfolge, die einen Distinguished Name (DN) enthält.
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- AD-Schema der Object (DS-DN)-Syntax
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519351"
---
# <a name="objectds-dn-syntax"></a><span data-ttu-id="2907f-104">Object (DS-DN)-Syntax</span><span class="sxs-lookup"><span data-stu-id="2907f-104">Object(DS-DN) syntax</span></span>

<span data-ttu-id="2907f-105">Eine Zeichenfolge, die einen Distinguished Name (DN) enthält.</span><span class="sxs-lookup"><span data-stu-id="2907f-105">String that contains a distinguished name (DN).</span></span> <span data-ttu-id="2907f-106">Für Attribute mit dieser Syntax verarbeitet Active Directory Attributwerte als Verweise auf das Objekt, das durch den DN identifiziert wird, und aktualisiert den Wert automatisch, wenn das Objekt verschoben oder umbenannt wird.</span><span class="sxs-lookup"><span data-stu-id="2907f-106">For attributes with this syntax, Active Directory handles attribute values as references to the object identified by the DN and automatically updates the value if the object is moved or renamed.</span></span> <span data-ttu-id="2907f-107">Geben Sie für Abfragen, die Attribute der DN-Syntax in einem Filter enthalten, vollständige Distinguished Names an.</span><span class="sxs-lookup"><span data-stu-id="2907f-107">For queries that include attributes of DN syntax in a filter, specify full distinguished names.</span></span> <span data-ttu-id="2907f-108">Platzhalter (z. b. CN = John \* ) werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2907f-108">Wildcards (for example, cn=John\*) are not supported.</span></span>



| <span data-ttu-id="2907f-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2907f-109">Entry</span></span> | <span data-ttu-id="2907f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="2907f-110">Value</span></span> |
|--------------|------------------------------------------------------------------------|
| <span data-ttu-id="2907f-111">Name</span><span class="sxs-lookup"><span data-stu-id="2907f-111">Name</span></span>         | <span data-ttu-id="2907f-112">Object(DS-DN)</span><span class="sxs-lookup"><span data-stu-id="2907f-112">Object(DS-DN)</span></span>                                                          |
| <span data-ttu-id="2907f-113">Syntax-ID</span><span class="sxs-lookup"><span data-stu-id="2907f-113">Syntax ID</span></span>    | <span data-ttu-id="2907f-114">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="2907f-114">2.5.5.1</span></span>                                                                |
| <span data-ttu-id="2907f-115">OM-ID</span><span class="sxs-lookup"><span data-stu-id="2907f-115">OM ID</span></span>        | <span data-ttu-id="2907f-116">127</span><span class="sxs-lookup"><span data-stu-id="2907f-116">127</span></span>                                                                    |
| <span data-ttu-id="2907f-117">MAPI-Typ</span><span class="sxs-lookup"><span data-stu-id="2907f-117">MAPI Type</span></span>    | <span data-ttu-id="2907f-118">OBJECT</span><span class="sxs-lookup"><span data-stu-id="2907f-118">OBJECT</span></span>                                                                 |
| <span data-ttu-id="2907f-119">ADS-Typ</span><span class="sxs-lookup"><span data-stu-id="2907f-119">ADS Type</span></span>     | <span data-ttu-id="2907f-120">adstype- \_ DN- \_ Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2907f-120">ADSTYPE\_DN\_STRING</span></span>                                                    |
| <span data-ttu-id="2907f-121">Varianttyp</span><span class="sxs-lookup"><span data-stu-id="2907f-121">Variant Type</span></span> | <span data-ttu-id="2907f-122">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="2907f-122">VT\_BSTR</span></span>                                                               |
| <span data-ttu-id="2907f-123">SDS-Typ</span><span class="sxs-lookup"><span data-stu-id="2907f-123">SDS Type</span></span>     | [<span data-ttu-id="2907f-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2907f-124">System.String</span></span>](/dotnet/api/system.string) |



## <a name="see-also"></a><span data-ttu-id="2907f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2907f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2907f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2907f-126">System.String</span></span>](/dotnet/api/system.string)
</dt> </dl>

 

 
