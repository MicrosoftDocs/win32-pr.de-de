---
title: Syntax für Zeichen folgen (generalisierte Zeit)
description: Ein Zeit Zeichen folgen Format, das von ASN. 1-Standards definiert wird. | Syntax für Zeichen folgen (generalisierte Zeit)
ms.assetid: c69ab29b-5877-47d4-b58d-4f103758dfac
ms.tgt_platform: multiple
keywords:
- Zeichenfolge (generalisierte Zeit) Syntax AD-Schema
topic_type:
- apiref
api_name:
- String(Generalized-Time)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e754fe622d3ff6f010521b7bc9b9e4ff7a5f34
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219201"
---
# <a name="stringgeneralized-time-syntax"></a><span data-ttu-id="3f3cc-105">Syntax für Zeichen folgen (generalisierte Zeit)</span><span class="sxs-lookup"><span data-stu-id="3f3cc-105">String(Generalized-Time) syntax</span></span>

<span data-ttu-id="3f3cc-106">Ein Zeit Zeichen folgen Format, das von ASN. 1-Standards definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3f3cc-106">A time string format defined by ASN.1 standards.</span></span> <span data-ttu-id="3f3cc-107">Verwenden Sie diese Syntax zum Speichern von Zeitwerten in Generalized-Time Format.</span><span class="sxs-lookup"><span data-stu-id="3f3cc-107">Use this syntax for storing time values in Generalized-Time format.</span></span>

<span data-ttu-id="3f3cc-108">Das Format für die Generalized-Time-Syntax lautet "YYYYMMDDHHMMSS. 0z".</span><span class="sxs-lookup"><span data-stu-id="3f3cc-108">The format for the Generalized-Time syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="3f3cc-109">Ein Beispiel für einen zulässigen Wert ist "20010928060000.0 z".</span><span class="sxs-lookup"><span data-stu-id="3f3cc-109">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="3f3cc-110">"Z" weist auf keine Zeit differenzielle Abweichung hin.</span><span class="sxs-lookup"><span data-stu-id="3f3cc-110">The "Z" indicates no time differential.</span></span> <span data-ttu-id="3f3cc-111">Active Directory speichert Datum/Uhrzeit als Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="3f3cc-111">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="3f3cc-112">Wenn keine Zeit differenzielle Angabe angegeben ist, ist GMT die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="3f3cc-112">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="3f3cc-113">Wenn die Uhrzeit in einer anderen Zeitzone als GMT angegeben wird, wird die Differenz zwischen der Zeitzone und der GMT an die Zeichenfolge angefügt, nicht an "Z" in der Form "YYYYMMDDHHMMSS. 0 \[ +/- \] hhmm".</span><span class="sxs-lookup"><span data-stu-id="3f3cc-113">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="3f3cc-114">Ein Beispiel für einen zulässigen Wert ist "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="3f3cc-114">An example of an acceptable value is "20010928060000.0+0200".</span></span> <span data-ttu-id="3f3cc-115">Die differenzielle Abhängigkeit basiert auf der Formel: GMT = local + Differential.</span><span class="sxs-lookup"><span data-stu-id="3f3cc-115">The differential is based on the formula: GMT=Local+differential.</span></span>

<span data-ttu-id="3f3cc-116">Weitere Informationen finden Sie unter ISO 8601 und X680.</span><span class="sxs-lookup"><span data-stu-id="3f3cc-116">For more information, see ISO 8601 and X680.</span></span>



| <span data-ttu-id="3f3cc-117">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f3cc-117">Entry</span></span> | <span data-ttu-id="3f3cc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3f3cc-118">Value</span></span> |
|--------------|----------------------------------------------------------------------------|
| <span data-ttu-id="3f3cc-119">Name</span><span class="sxs-lookup"><span data-stu-id="3f3cc-119">Name</span></span>         | <span data-ttu-id="3f3cc-120">String(Generalized-Time)</span><span class="sxs-lookup"><span data-stu-id="3f3cc-120">String(Generalized-Time)</span></span>                                                   |
| <span data-ttu-id="3f3cc-121">Syntax-ID</span><span class="sxs-lookup"><span data-stu-id="3f3cc-121">Syntax ID</span></span>    | <span data-ttu-id="3f3cc-122">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="3f3cc-122">2.5.5.11</span></span>                                                                   |
| <span data-ttu-id="3f3cc-123">OM-ID</span><span class="sxs-lookup"><span data-stu-id="3f3cc-123">OM ID</span></span>        | <span data-ttu-id="3f3cc-124">24</span><span class="sxs-lookup"><span data-stu-id="3f3cc-124">24</span></span>                                                                         |
| <span data-ttu-id="3f3cc-125">MAPI-Typ</span><span class="sxs-lookup"><span data-stu-id="3f3cc-125">MAPI Type</span></span>    | <span data-ttu-id="3f3cc-126">SYSTIME</span><span class="sxs-lookup"><span data-stu-id="3f3cc-126">SYSTIME</span></span>                                                                    |
| <span data-ttu-id="3f3cc-127">ADS-Typ</span><span class="sxs-lookup"><span data-stu-id="3f3cc-127">ADS Type</span></span>     | <span data-ttu-id="3f3cc-128">adstype- \_ UTC- \_ Zeit</span><span class="sxs-lookup"><span data-stu-id="3f3cc-128">ADSTYPE\_UTC\_TIME</span></span>                                                         |
| <span data-ttu-id="3f3cc-129">Varianttyp</span><span class="sxs-lookup"><span data-stu-id="3f3cc-129">Variant Type</span></span> | <span data-ttu-id="3f3cc-130">VT- \_ Datum</span><span class="sxs-lookup"><span data-stu-id="3f3cc-130">VT\_DATE</span></span>                                                                   |
| <span data-ttu-id="3f3cc-131">SDS-Typ</span><span class="sxs-lookup"><span data-stu-id="3f3cc-131">SDS Type</span></span>     | [<span data-ttu-id="3f3cc-132">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="3f3cc-132">System.DateTime</span></span>](/dotnet/api/system.datetime) |



## <a name="see-also"></a><span data-ttu-id="3f3cc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f3cc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3cc-134">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="3f3cc-134">System.DateTime</span></span>](/dotnet/api/system.datetime)
</dt> </dl>

 

 
