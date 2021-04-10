---
title: IADsDNWithBinary-Eigenschafts Methoden (IADs. h)
description: Die-Eigenschaften Methode der IADsDNWithBinary-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- IADsDNWithBinary-Eigenschafts Methoden ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105147"
---
# <a name="iadsdnwithbinary-property-methods"></a><span data-ttu-id="ab0f7-105">IADsDNWithBinary-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="ab0f7-105">IADsDNWithBinary Property Methods</span></span>

<span data-ttu-id="ab0f7-106">Die-Eigenschaften Methode der [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ab0f7-106">The property method of the [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) interface sets the property described in the following table.</span></span> <span data-ttu-id="ab0f7-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ab0f7-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ab0f7-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ab0f7-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ab0f7-109">**Binaryvalue**</span><span class="sxs-lookup"><span data-stu-id="ab0f7-109">**BinaryValue**</span></span>
<span data-ttu-id="ab0f7-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ab0f7-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ab0f7-111">Die GUID eines einem DN zugeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="ab0f7-111">The GUID of an object associated with a DN.</span></span>

<dt>

<span data-ttu-id="ab0f7-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab0f7-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ab0f7-113">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ab0f7-113">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ab0f7-114">**Dnstring**</span><span class="sxs-lookup"><span data-stu-id="ab0f7-114">**DNString**</span></span>
<span data-ttu-id="ab0f7-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ab0f7-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="ab0f7-116">Die DN-Zeichenfolge, die der GUID eines Objekts zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ab0f7-116">The DN string associated with the GUID of an object.</span></span>

<dt>

<span data-ttu-id="ab0f7-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ab0f7-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ab0f7-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ab0f7-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a><span data-ttu-id="ab0f7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab0f7-119">Requirements</span></span>



| <span data-ttu-id="ab0f7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab0f7-120">Requirement</span></span> | <span data-ttu-id="ab0f7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ab0f7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0f7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab0f7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0f7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab0f7-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab0f7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab0f7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0f7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab0f7-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab0f7-126">Header</span><span class="sxs-lookup"><span data-stu-id="ab0f7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab0f7-127"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab0f7-127"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ab0f7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ab0f7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab0f7-129"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab0f7-129"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab0f7-130">IID</span><span class="sxs-lookup"><span data-stu-id="ab0f7-130">IID</span></span><br/>                      | <span data-ttu-id="ab0f7-131">IID \_ IADsDNWithBinary ist als 7e99c0a2-s935-11d2-ba96-00c04sb6d0d1 definiert.</span><span class="sxs-lookup"><span data-stu-id="ab0f7-131">IID\_IADsDNWithBinary is defined as 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="ab0f7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab0f7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0f7-133">**IADsDNWithBinary**</span><span class="sxs-lookup"><span data-stu-id="ab0f7-133">**IADsDNWithBinary**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[<span data-ttu-id="ab0f7-134">**ADS \_ DN \_ mit \_ Binär**</span><span class="sxs-lookup"><span data-stu-id="ab0f7-134">**ADS\_DN\_WITH\_BINARY**</span></span>](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 





