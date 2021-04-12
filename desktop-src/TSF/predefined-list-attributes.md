---
title: Vordefinierte Listen Attribute ("tsatyd. h")
description: Die folgenden Werte identifizieren Listen Attribute, die mit der ITF Context getappproperty-Methode abgerufen werden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Vordefinierte Listen Attribute Text Dienst-Framework
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105386"
---
# <a name="predefined-list-attributes"></a><span data-ttu-id="ac05b-105">Vordefinierte Listen Attribute</span><span class="sxs-lookup"><span data-stu-id="ac05b-105">Predefined List Attributes</span></span>

<span data-ttu-id="ac05b-106">Die folgenden Werte identifizieren Listen Attribute, die mit der [ITF context:: getappproperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ac05b-106">The following values identify list attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="ac05b-107">Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ac05b-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="ac05b-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ac05b-108">Properties</span></span>



| <span data-ttu-id="ac05b-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ac05b-109">Property</span></span>                          | <span data-ttu-id="ac05b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac05b-110">Description</span></span>                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac05b-111">Liste der "Tsat-ID" \_</span><span class="sxs-lookup"><span data-stu-id="ac05b-111">TSATTRID\_List</span></span>                    | <span data-ttu-id="ac05b-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac05b-112">Not used.</span></span>                                                                                       |
| <span data-ttu-id="ac05b-113">"- \_ \_ Levelliste"</span><span class="sxs-lookup"><span data-stu-id="ac05b-113">TSATTRID\_List\_LevelIndel</span></span>        | <span data-ttu-id="ac05b-114">Enthält die Index Ebene der Liste.</span><span class="sxs-lookup"><span data-stu-id="ac05b-114">Contains the index level of the list.</span></span> <span data-ttu-id="ac05b-115">1 ist die äußerste Ebene, 2 ist die nächste Ebene usw.</span><span class="sxs-lookup"><span data-stu-id="ac05b-115">1 is the outermost level, 2 is the next level, and so on.</span></span> |
| <span data-ttu-id="ac05b-116">Der Typ der der- \_ Liste. \_</span><span class="sxs-lookup"><span data-stu-id="ac05b-116">TSATTRID\_List\_Type</span></span>              | <span data-ttu-id="ac05b-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ac05b-117">Not used.</span></span>                                                                                       |
| <span data-ttu-id="ac05b-118">Der Typ "" der "der- \_ \_ Typ" \_</span><span class="sxs-lookup"><span data-stu-id="ac05b-118">TSATTRID\_List\_Type\_Arabic</span></span>      | <span data-ttu-id="ac05b-119">Enthält einen Wert ungleich 0 (null), wenn die Liste eine arabische Zahlenliste ist, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="ac05b-119">Contains a nonzero value if the list is an arabic numeral list or zero otherwise.</span></span>               |
| <span data-ttu-id="ac05b-120">Aufzählungs Zeichen- \_ Aufzählungs Zeichen \_ \_</span><span class="sxs-lookup"><span data-stu-id="ac05b-120">TSATTRID\_List\_Type\_Bullet</span></span>      | <span data-ttu-id="ac05b-121">Enthält einen Wert ungleich 0 (null), wenn die Liste eine Auflistungs Liste ist, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="ac05b-121">Contains a nonzero value if the list is a bulleted list or zero otherwise.</span></span>                      |
| <span data-ttu-id="ac05b-122">In der \_ Liste der \_ vom Typ "". \_</span><span class="sxs-lookup"><span data-stu-id="ac05b-122">TSATTRID\_List\_Type\_LowerLetter</span></span> | <span data-ttu-id="ac05b-123">Enthält einen Wert ungleich 0 (null), wenn die Liste eine durch klein geschriebene Liste ist oder andernfalls 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="ac05b-123">Contains a nonzero value if the list is a lowercase lettered list or zero otherwise.</span></span>            |
| <span data-ttu-id="ac05b-124">Der-Typ der der-Gruppe ist " \_ \_ \_ LowerRoman"</span><span class="sxs-lookup"><span data-stu-id="ac05b-124">TSATTRID\_List\_Type\_LowerRoman</span></span>  | <span data-ttu-id="ac05b-125">Enthält einen Wert ungleich 0 (null), wenn die Liste eine klein geschriebene römische Ziffern Liste ist, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="ac05b-125">Contains a nonzero value if the list is a lowercase roman numeral list or zero otherwise.</span></span>       |
| <span data-ttu-id="ac05b-126">Der Typ "der" \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ac05b-126">TSATTRID\_List\_Type\_UpperLetter</span></span> | <span data-ttu-id="ac05b-127">Enthält einen Wert ungleich 0 (null), wenn es sich bei der Liste um eine schreibgeschützte Großbuchstaben oder andernfalls um NULL handelt.</span><span class="sxs-lookup"><span data-stu-id="ac05b-127">Contains a nonzero value if the list is an upper-case lettered list or zero otherwise.</span></span>          |
| <span data-ttu-id="ac05b-128">Der-Typ der der-Klasse, \_ \_ \_ UpperRoman</span><span class="sxs-lookup"><span data-stu-id="ac05b-128">TSATTRID\_List\_Type\_UpperRoman</span></span>  | <span data-ttu-id="ac05b-129">Enthält einen Wert ungleich 0 (null), wenn die Liste eine römische Zahlenliste in Großbuchstaben oder andernfalls NULL ist.</span><span class="sxs-lookup"><span data-stu-id="ac05b-129">Contains a nonzero value if the list is an uppercase roman numeral list or zero otherwise.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="ac05b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac05b-130">Requirements</span></span>



| <span data-ttu-id="ac05b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac05b-131">Requirement</span></span> | <span data-ttu-id="ac05b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ac05b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac05b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac05b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ac05b-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac05b-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ac05b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac05b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ac05b-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac05b-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac05b-137">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ac05b-137">Redistributable</span></span><br/>          | <span data-ttu-id="ac05b-138">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ac05b-138">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="ac05b-139">Header</span><span class="sxs-lookup"><span data-stu-id="ac05b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac05b-140"><dt>"Tsatphd. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ac05b-140"><dt>TsAttrid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac05b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac05b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac05b-142">ITF context:: getappproperty</span><span class="sxs-lookup"><span data-stu-id="ac05b-142">ITfContext::GetAppProperty</span></span>](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

