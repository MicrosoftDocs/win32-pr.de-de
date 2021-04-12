---
title: Iadshold-Eigenschaften Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadshold-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- Iadshold-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae2499efb461e6c13397fdaef75e515f0a1a21a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105135"
---
# <a name="iadshold-property-methods"></a><span data-ttu-id="5635d-105">Iadshold-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="5635d-105">IADsHold Property Methods</span></span>

<span data-ttu-id="5635d-106">Die-Eigenschaften Methode der [**iadshold**](/windows/desktop/api/Iads/nn-iads-iadshold) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5635d-106">The property method of the [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) interface sets the property described in the following table.</span></span> <span data-ttu-id="5635d-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5635d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5635d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5635d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5635d-109">**Amount (Betrag)**</span><span class="sxs-lookup"><span data-stu-id="5635d-109">**Amount**</span></span>
<span data-ttu-id="5635d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5635d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5635d-111">Die Menge der Gebühren, die für den Benutzer für den Zeitraum erhoben werden, während der Server den Konto Saldo des Benutzers prüft.</span><span class="sxs-lookup"><span data-stu-id="5635d-111">The amount of charges levied against the user for the period on hold while the server checks the account balance of the user.</span></span>

<dt>

<span data-ttu-id="5635d-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5635d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5635d-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="5635d-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5635d-114">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="5635d-114">**ObjectName**</span></span>
<span data-ttu-id="5635d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5635d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="5635d-116">Der Name des Objekts, das einen angehaltenen Benutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5635d-116">The name of the object representing a user on hold.</span></span>

<dt>

<span data-ttu-id="5635d-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="5635d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5635d-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5635d-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="5635d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5635d-119">Requirements</span></span>



| <span data-ttu-id="5635d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5635d-120">Requirement</span></span> | <span data-ttu-id="5635d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5635d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5635d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5635d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5635d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5635d-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5635d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5635d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5635d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5635d-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5635d-126">Header</span><span class="sxs-lookup"><span data-stu-id="5635d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5635d-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5635d-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5635d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5635d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5635d-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5635d-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5635d-130">IID</span><span class="sxs-lookup"><span data-stu-id="5635d-130">IID</span></span><br/>                      | <span data-ttu-id="5635d-131">IID \_ iadshold ist als B3EB3B37-4080-11d1-A3AC-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="5635d-131">IID\_IADsHold is defined as B3EB3B37-4080-11D1-A3AC-00C04FB950DC</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5635d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5635d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5635d-133">**IADsHold**</span><span class="sxs-lookup"><span data-stu-id="5635d-133">**IADsHold**</span></span>](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





