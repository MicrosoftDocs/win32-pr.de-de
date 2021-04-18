---
title: Iadspostaladdress-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadspostaladdress-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Iadspostaladdress-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d8eeaac8fa258a2df1452b8aa261ee59b3cc85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339355"
---
# <a name="iadspostaladdress-property-methods"></a><span data-ttu-id="4b8dd-105">Iadspostaladdress-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="4b8dd-105">IADsPostalAddress Property Methods</span></span>

<span data-ttu-id="4b8dd-106">Die-Eigenschaften Methode der [**iadspostaladdress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-106">The property method of the [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) interface sets the property described in the following table.</span></span> <span data-ttu-id="4b8dd-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4b8dd-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4b8dd-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b8dd-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4b8dd-109">**PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="4b8dd-109">**PostalAddress**</span></span>
<span data-ttu-id="4b8dd-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4b8dd-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4b8dd-111">Ein Array von sechs Zeichen folgen, das die Postadresse des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-111">An array of six strings holding the postal address of the user.</span></span>

<dt>

<span data-ttu-id="4b8dd-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4b8dd-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4b8dd-113">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4b8dd-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="4b8dd-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b8dd-114">Requirements</span></span>



| <span data-ttu-id="4b8dd-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b8dd-115">Requirement</span></span> | <span data-ttu-id="4b8dd-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4b8dd-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8dd-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b8dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8dd-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b8dd-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b8dd-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b8dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8dd-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b8dd-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b8dd-121">Header</span><span class="sxs-lookup"><span data-stu-id="4b8dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b8dd-122"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b8dd-122"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4b8dd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4b8dd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b8dd-124"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b8dd-124"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4b8dd-125">IID</span><span class="sxs-lookup"><span data-stu-id="4b8dd-125">IID</span></span><br/>                      | <span data-ttu-id="4b8dd-126">IID \_ iadspostaladdress ist als 7adecf 29-4680-11d1-a3b4-00c04b950 DC definiert.</span><span class="sxs-lookup"><span data-stu-id="4b8dd-126">IID\_IADsPostalAddress is defined as 7ADECF29-4680-11D1-A3B4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="4b8dd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b8dd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8dd-128">**IADsPostalAddress**</span><span class="sxs-lookup"><span data-stu-id="4b8dd-128">**IADsPostalAddress**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[<span data-ttu-id="4b8dd-129">**Werbung \_ PostalAddress**</span><span class="sxs-lookup"><span data-stu-id="4b8dd-129">**ADS\_POSTALADDRESS**</span></span>](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 





