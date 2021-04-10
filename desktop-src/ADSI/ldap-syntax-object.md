---
title: LDAP-Syntax Objekt
description: Der LDAP-Anbieter verwendet die folgende Zuordnung zwischen der LDAP-Syntax und der ADSI-Syntax.
ms.assetid: a82cf8ab-9591-4489-87a6-ccfab0e01d61
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Service Providers, Mapping-Syntax zur LDAP-Syntax
- Zuordnung der ADSI-Syntax zur LDAP-Syntax ADSI
- Syntax und Zuordnung von ADSI zu LDAP ADSI
- LDAP-Dienstanbieter ADSI, Zuordnung der ADSI-Syntax zur LDAP-Syntax
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2272a0805ec32fd7ade9c4584feefb64fb1467f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100570"
---
# <a name="ldap-syntax-object"></a><span data-ttu-id="56702-107">LDAP-Syntax Objekt</span><span class="sxs-lookup"><span data-stu-id="56702-107">LDAP Syntax Object</span></span>

<span data-ttu-id="56702-108">Der LDAP-Anbieter verwendet die folgende Zuordnung zwischen der LDAP-Syntax und der ADSI-Syntax.</span><span class="sxs-lookup"><span data-stu-id="56702-108">The LDAP provider uses the following mapping between the LDAP syntax and ADSI syntax.</span></span>



| <span data-ttu-id="56702-109">LDAP-Syntax</span><span class="sxs-lookup"><span data-stu-id="56702-109">LDAP Syntax</span></span>   | <span data-ttu-id="56702-110">ADSI-Syntax (Automatisierung)</span><span class="sxs-lookup"><span data-stu-id="56702-110">ADSI Syntax (Automation)</span></span>            |
|---------------|-------------------------------------|
| <span data-ttu-id="56702-111">ADsPath</span><span class="sxs-lookup"><span data-stu-id="56702-111">ADsPath</span></span>       | <span data-ttu-id="56702-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="56702-112">VT\_BSTR</span></span>                            |
| <span data-ttu-id="56702-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="56702-113">Boolean</span></span>       | <span data-ttu-id="56702-114">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="56702-114">VT\_BOOL</span></span>                            |
| <span data-ttu-id="56702-115">Zähler</span><span class="sxs-lookup"><span data-stu-id="56702-115">Counter</span></span>       | <span data-ttu-id="56702-116">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="56702-116">VT\_I4</span></span>                              |
| <span data-ttu-id="56702-117">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="56702-117">EmailAddress</span></span>  | <span data-ttu-id="56702-118">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="56702-118">VT\_BSTR</span></span>                            |
| <span data-ttu-id="56702-119">Faxnummer</span><span class="sxs-lookup"><span data-stu-id="56702-119">FaxNumber</span></span>     | <span data-ttu-id="56702-120">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="56702-120">VT\_BSTR</span></span>                            |
| <span data-ttu-id="56702-121">Integer</span><span class="sxs-lookup"><span data-stu-id="56702-121">Integer</span></span>       | <span data-ttu-id="56702-122">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="56702-122">VT\_I4</span></span>                              |
| <span data-ttu-id="56702-123">Intervall</span><span class="sxs-lookup"><span data-stu-id="56702-123">Interval</span></span>      | <span data-ttu-id="56702-124">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="56702-124">VT\_I4</span></span>                              |
| <span data-ttu-id="56702-125">List</span><span class="sxs-lookup"><span data-stu-id="56702-125">List</span></span>          | <span data-ttu-id="56702-126">VT- \_ Variante (VT \_ BSTR \| VT- \_ Array)</span><span class="sxs-lookup"><span data-stu-id="56702-126">VT\_VARIANT (VT\_BSTR \| VT\_ARRAY)</span></span> |
| <span data-ttu-id="56702-127">Netaddress</span><span class="sxs-lookup"><span data-stu-id="56702-127">NetAddress</span></span>    | <span data-ttu-id="56702-128">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="56702-128">VT\_BSTR</span></span>                            |
| <span data-ttu-id="56702-129">Octetstring</span><span class="sxs-lookup"><span data-stu-id="56702-129">OctetString</span></span>   | <span data-ttu-id="56702-130">VT- \_ Variante</span><span class="sxs-lookup"><span data-stu-id="56702-130">VT\_VARIANT</span></span>                         |
| <span data-ttu-id="56702-131">Pfad</span><span class="sxs-lookup"><span data-stu-id="56702-131">Path</span></span>          | <span data-ttu-id="56702-132">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="56702-132">VT\_BSTR</span></span>                            |
| <span data-ttu-id="56702-133">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="56702-133">PhoneNumber</span></span>   | <span data-ttu-id="56702-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="56702-134">VT\_BSTR</span></span>                            |
| <span data-ttu-id="56702-135">PostalAddress</span><span class="sxs-lookup"><span data-stu-id="56702-135">PostalAddress</span></span> | <span data-ttu-id="56702-136">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="56702-136">VT\_BSTR</span></span>                            |
| <span data-ttu-id="56702-137">Smallinterval</span><span class="sxs-lookup"><span data-stu-id="56702-137">SmallInterval</span></span> | <span data-ttu-id="56702-138">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="56702-138">VT\_I4</span></span>                              |
| <span data-ttu-id="56702-139">String</span><span class="sxs-lookup"><span data-stu-id="56702-139">String</span></span>        | <span data-ttu-id="56702-140">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="56702-140">VT\_BSTR</span></span>                            |
| <span data-ttu-id="56702-141">Time</span><span class="sxs-lookup"><span data-stu-id="56702-141">Time</span></span>          | <span data-ttu-id="56702-142">VT- \_ Datum</span><span class="sxs-lookup"><span data-stu-id="56702-142">VT\_DATE</span></span>                            |



 

 

 




