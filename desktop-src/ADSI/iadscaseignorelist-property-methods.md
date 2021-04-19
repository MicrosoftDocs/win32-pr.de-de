---
title: Iadscaseignorelist-Eigenschafts Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadscaseignorelist-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- Iadscaseignorelist-Eigenschafts Methoden ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aabf26508c3e38e117ad25721af8bece5d69b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342461"
---
# <a name="iadscaseignorelist-property-methods"></a><span data-ttu-id="95642-105">Iadscaseignorelist-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="95642-105">IADsCaseIgnoreList Property Methods</span></span>

<span data-ttu-id="95642-106">Die-Eigenschaften Methode der [**iadscaseignorelist**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="95642-106">The property method of the [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) interface sets the property described in the following table.</span></span> <span data-ttu-id="95642-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="95642-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="95642-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95642-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="95642-109">**Caseignorelist**</span><span class="sxs-lookup"><span data-stu-id="95642-109">**CaseIgnoreList**</span></span>
<span data-ttu-id="95642-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="95642-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="95642-111">Eine geordnete Sequenz von Zeichen folgen ohne Beachtung</span><span class="sxs-lookup"><span data-stu-id="95642-111">An ordered sequence of case insensitive strings.</span></span>

<dt>

<span data-ttu-id="95642-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="95642-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="95642-113">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="95642-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="95642-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95642-114">Requirements</span></span>



| <span data-ttu-id="95642-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95642-115">Requirement</span></span> | <span data-ttu-id="95642-116">Wert</span><span class="sxs-lookup"><span data-stu-id="95642-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95642-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95642-117">Minimum supported client</span></span><br/> | <span data-ttu-id="95642-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95642-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95642-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95642-119">Minimum supported server</span></span><br/> | <span data-ttu-id="95642-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95642-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95642-121">Header</span><span class="sxs-lookup"><span data-stu-id="95642-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="95642-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="95642-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="95642-123">DLL</span><span class="sxs-lookup"><span data-stu-id="95642-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95642-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95642-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="95642-125">IID</span><span class="sxs-lookup"><span data-stu-id="95642-125">IID</span></span><br/>                      | <span data-ttu-id="95642-126">IID \_ iadscaseignorelist als 7b66b533-4680-11d1-a3b4-00c04fb950 DC definiert.</span><span class="sxs-lookup"><span data-stu-id="95642-126">IID\_IADsCaseIgnoreList is defined as 7B66B533-4680-11D1-A3B4-00C04FB950DC</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="95642-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95642-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95642-128">**IADsCaseIgnoreList**</span><span class="sxs-lookup"><span data-stu-id="95642-128">**IADsCaseIgnoreList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[<span data-ttu-id="95642-129">**Liste der anzeigen \_ caseignore \_**</span><span class="sxs-lookup"><span data-stu-id="95642-129">**ADS\_CASEIGNORE\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





