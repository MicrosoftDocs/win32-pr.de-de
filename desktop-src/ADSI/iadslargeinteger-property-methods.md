---
title: IADsLargeInteger-Eigenschafts Methoden (IADs. h)
description: Die Eigenschaften Methoden der IADsLargeInteger-Schnittstelle erhalten und legen die Eigenschaften fest, die in der folgenden Tabelle beschrieben werden. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- Iadslargeingeteger-Eigenschafts Methoden ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 097e9ae7387658f983c691e56e4f90ba40dea407
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340001"
---
# <a name="iadslargeinteger-property-methods"></a><span data-ttu-id="240a6-105">Iadslargeingeteger-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="240a6-105">IADsLargeInteger Property Methods</span></span>

<span data-ttu-id="240a6-106">Die Eigenschaften Methoden der [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) -Schnittstelle erhalten und legen die Eigenschaften fest, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="240a6-106">The property methods of the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface get and set the properties described in the following table.</span></span> <span data-ttu-id="240a6-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="240a6-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="240a6-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="240a6-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="240a6-109">**HighPart**</span><span class="sxs-lookup"><span data-stu-id="240a6-109">**HighPart**</span></span>
<span data-ttu-id="240a6-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="240a6-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="240a6-111">Der hohe Teil der Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="240a6-111">The high part of the integer.</span></span>

<dt>

<span data-ttu-id="240a6-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="240a6-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="240a6-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="240a6-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="240a6-114">**LowPart**</span><span class="sxs-lookup"><span data-stu-id="240a6-114">**LowPart**</span></span>
<span data-ttu-id="240a6-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="240a6-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="240a6-116">Der niedrige Teil der Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="240a6-116">The low part of the integer.</span></span>

<dt>

<span data-ttu-id="240a6-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="240a6-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="240a6-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="240a6-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="240a6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="240a6-119">Remarks</span></span>

<span data-ttu-id="240a6-120">Wenn largeint den **LargeInteger** -Typ aufweist, wird der Wert von den Werten von **highpart** und **LowPart** gemäß der folgenden Formel angegeben.</span><span class="sxs-lookup"><span data-stu-id="240a6-120">If largeInt is of the **LargeInteger** type, its value is specified by those of **HighPart** and **LowPart** according to the following formula.</span></span>


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a><span data-ttu-id="240a6-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="240a6-121">Examples</span></span>

<span data-ttu-id="240a6-122">Im folgenden Visual Basic Codebeispiel wird eine große Ganzzahl auf 43937327281 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="240a6-122">The following Visual Basic code example sets a large integer to 43937327281.</span></span>


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a><span data-ttu-id="240a6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="240a6-123">Requirements</span></span>



| <span data-ttu-id="240a6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="240a6-124">Requirement</span></span> | <span data-ttu-id="240a6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="240a6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="240a6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="240a6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="240a6-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="240a6-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="240a6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="240a6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="240a6-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="240a6-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="240a6-130">Header</span><span class="sxs-lookup"><span data-stu-id="240a6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="240a6-131"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="240a6-131"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="240a6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="240a6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="240a6-133"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="240a6-133"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="240a6-134">IID</span><span class="sxs-lookup"><span data-stu-id="240a6-134">IID</span></span><br/>                      | <span data-ttu-id="240a6-135">IID \_ IADsLargeInteger ist definiert als 9068270b-0939-11d1-8be1-00c04sd8d503</span><span class="sxs-lookup"><span data-stu-id="240a6-135">IID\_IADsLargeInteger is defined as 9068270B-0939-11D1-8BE1-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="240a6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="240a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="240a6-137">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="240a6-137">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





