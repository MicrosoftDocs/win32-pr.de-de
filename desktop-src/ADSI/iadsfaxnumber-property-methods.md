---
title: Iadsfaxnumber-Eigenschafts Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsfaxnumber-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- Iadsfaxnumber-Eigenschafts Methoden ADSI
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342856"
---
# <a name="iadsfaxnumber-property-methods"></a><span data-ttu-id="58915-105">Iadsfaxnumber-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="58915-105">IADsFaxNumber Property Methods</span></span>

<span data-ttu-id="58915-106">Die-Eigenschaften Methode der [**iadsfaxnumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="58915-106">The property method of the [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) interface sets the property described in the following table.</span></span> <span data-ttu-id="58915-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="58915-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="58915-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="58915-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="58915-109">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="58915-109">**Parameters**</span></span>
<span data-ttu-id="58915-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="58915-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="58915-111">Die Parameter für den faxcomputer.</span><span class="sxs-lookup"><span data-stu-id="58915-111">The parameters for the fax machine.</span></span>

<dt>

<span data-ttu-id="58915-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="58915-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="58915-113">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="58915-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="58915-114">**TelephoneNumber**</span><span class="sxs-lookup"><span data-stu-id="58915-114">**TelephoneNumber**</span></span>
<span data-ttu-id="58915-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="58915-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="58915-116">Die Telefonnummer des faxcomputers.</span><span class="sxs-lookup"><span data-stu-id="58915-116">The telephone number of the fax machine.</span></span>

<dt>

<span data-ttu-id="58915-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="58915-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="58915-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="58915-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="58915-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58915-119">Requirements</span></span>



| <span data-ttu-id="58915-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58915-120">Requirement</span></span> | <span data-ttu-id="58915-121">Wert</span><span class="sxs-lookup"><span data-stu-id="58915-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58915-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58915-122">Minimum supported client</span></span><br/> | <span data-ttu-id="58915-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58915-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58915-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58915-124">Minimum supported server</span></span><br/> | <span data-ttu-id="58915-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58915-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58915-126">Header</span><span class="sxs-lookup"><span data-stu-id="58915-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="58915-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="58915-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="58915-128">DLL</span><span class="sxs-lookup"><span data-stu-id="58915-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58915-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58915-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="58915-130">IID</span><span class="sxs-lookup"><span data-stu-id="58915-130">IID</span></span><br/>                      | <span data-ttu-id="58915-131">IID \_ iadsfaxnumber ist als A910DEA9-4680-11d1-0A3B-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="58915-131">IID\_IADsFaxNumber is defined as A910DEA9-4680-11D1-0A3B-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="58915-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58915-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58915-133">**IADsFaxNumber**</span><span class="sxs-lookup"><span data-stu-id="58915-133">**IADsFaxNumber**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[<span data-ttu-id="58915-134">**\_Faxnummer des ADS**</span><span class="sxs-lookup"><span data-stu-id="58915-134">**ADS\_FAXNUMBER**</span></span>](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 





