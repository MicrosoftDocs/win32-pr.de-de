---
title: Eigenschaften Methoden von iadsoctetlist (IADs. h)
description: Die-Eigenschaften Methode der iadsoctetlist-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- Eigenschaften Methoden von iadsoctetlist ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3631adaf00cf599214296e1792ffab8697ba5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956906"
---
# <a name="iadsoctetlist-property-methods"></a><span data-ttu-id="85dd3-105">Eigenschaften Methoden von iadsoctetlist</span><span class="sxs-lookup"><span data-stu-id="85dd3-105">IADsOctetList Property Methods</span></span>

<span data-ttu-id="85dd3-106">Die-Eigenschaften Methode der [**iadsoctetlist**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="85dd3-106">The property method of the [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) interface sets the property described in the following table.</span></span> <span data-ttu-id="85dd3-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="85dd3-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="85dd3-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85dd3-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="85dd3-109">**Oktetlist**</span><span class="sxs-lookup"><span data-stu-id="85dd3-109">**OctetList**</span></span>
<span data-ttu-id="85dd3-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="85dd3-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="85dd3-111">Eine geordnete Sequenz von Byte Arrays.</span><span class="sxs-lookup"><span data-stu-id="85dd3-111">An ordered sequence of byte arrays.</span></span>

<dt>

<span data-ttu-id="85dd3-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="85dd3-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="85dd3-113">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="85dd3-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="85dd3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85dd3-114">Requirements</span></span>



| <span data-ttu-id="85dd3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85dd3-115">Requirement</span></span> | <span data-ttu-id="85dd3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="85dd3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85dd3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85dd3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="85dd3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85dd3-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85dd3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85dd3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="85dd3-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85dd3-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85dd3-121">Header</span><span class="sxs-lookup"><span data-stu-id="85dd3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="85dd3-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="85dd3-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="85dd3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="85dd3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85dd3-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85dd3-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="85dd3-125">IID</span><span class="sxs-lookup"><span data-stu-id="85dd3-125">IID</span></span><br/>                      | <span data-ttu-id="85dd3-126">IID \_ iadsoctetlist ist definiert als 7b28b80f -4680-11d1-a3b4-00c04sb950 DC</span><span class="sxs-lookup"><span data-stu-id="85dd3-126">IID\_IADsOctetList is defined as 7B28B80F-4680-11D1-A3B4-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="85dd3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85dd3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85dd3-128">**IADsOctetList**</span><span class="sxs-lookup"><span data-stu-id="85dd3-128">**IADsOctetList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[<span data-ttu-id="85dd3-129">**Liste der ADS- \_ Oktett \_**</span><span class="sxs-lookup"><span data-stu-id="85dd3-129">**ADS\_OCTET\_LIST**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 





