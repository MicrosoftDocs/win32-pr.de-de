---
title: Iadenmail-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadsemail-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Iadlmail-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392117"
---
# <a name="iadsemail-property-methods"></a><span data-ttu-id="57ba7-105">Iadlmail-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="57ba7-105">IADsEmail Property Methods</span></span>

<span data-ttu-id="57ba7-106">Die-Eigenschaften Methode der [**iadsemail**](/windows/desktop/api/Iads/nn-iads-iadsemail) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="57ba7-106">The property method of the [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) interface sets the property described in the following table.</span></span> <span data-ttu-id="57ba7-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="57ba7-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="57ba7-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="57ba7-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="57ba7-109">**Adresse**</span><span class="sxs-lookup"><span data-stu-id="57ba7-109">**Address**</span></span>
<span data-ttu-id="57ba7-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="57ba7-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="57ba7-111">Die E-Mail-Adresse des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="57ba7-111">The email address of the user.</span></span>

<dt>

<span data-ttu-id="57ba7-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57ba7-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="57ba7-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="57ba7-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="57ba7-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="57ba7-114">**Type**</span></span>
<span data-ttu-id="57ba7-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="57ba7-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="57ba7-116">Der Typ der e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="57ba7-116">The type of the email message.</span></span>

<dt>

<span data-ttu-id="57ba7-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="57ba7-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="57ba7-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="57ba7-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="57ba7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57ba7-119">Requirements</span></span>



| <span data-ttu-id="57ba7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57ba7-120">Requirement</span></span> | <span data-ttu-id="57ba7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="57ba7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57ba7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57ba7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57ba7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ba7-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57ba7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57ba7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57ba7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57ba7-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57ba7-126">Header</span><span class="sxs-lookup"><span data-stu-id="57ba7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ba7-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ba7-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="57ba7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="57ba7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57ba7-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ba7-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="57ba7-130">IID</span><span class="sxs-lookup"><span data-stu-id="57ba7-130">IID</span></span><br/>                      | <span data-ttu-id="57ba7-131">IID \_ iadlmail ist als 97af011a-478e-11d1-a3b4-00c04tb950 DC definiert.</span><span class="sxs-lookup"><span data-stu-id="57ba7-131">IID\_IADsEmail is defined as 97AF011A-478E-11D1-A3B4-00C04FB950DC</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="57ba7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57ba7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ba7-133">**IADsEmail**</span><span class="sxs-lookup"><span data-stu-id="57ba7-133">**IADsEmail**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[<span data-ttu-id="57ba7-134">**Werbung \_ per e-Mail**</span><span class="sxs-lookup"><span data-stu-id="57ba7-134">**ADS\_EMAIL**</span></span>](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 





