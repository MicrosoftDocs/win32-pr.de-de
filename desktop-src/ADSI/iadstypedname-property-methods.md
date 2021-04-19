---
title: Iadstypedname-Eigenschafts Methoden (IADs. h)
description: Die-Eigenschaften Methode der iadstypedname-Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- Iadstypedname-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339963"
---
# <a name="iadstypedname-property-methods"></a><span data-ttu-id="31e6d-105">Iadstypedname-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="31e6d-105">IADsTypedName Property Methods</span></span>

<span data-ttu-id="31e6d-106">Die-Eigenschaften Methode der [**iadstypedname**](/windows/desktop/api/Iads/nn-iads-iadstypedname) -Schnittstelle legt die-Eigenschaft fest, die in der folgenden Tabelle beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="31e6d-106">The property method of the [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) interface sets the property described in the following table.</span></span> <span data-ttu-id="31e6d-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="31e6d-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="31e6d-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31e6d-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="31e6d-109">**Intervall**</span><span class="sxs-lookup"><span data-stu-id="31e6d-109">**Interval**</span></span>
<span data-ttu-id="31e6d-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="31e6d-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="31e6d-111">Die Frequenz des Verweises des Objekts.</span><span class="sxs-lookup"><span data-stu-id="31e6d-111">The frequency of reference of the object.</span></span>

<dt>

<span data-ttu-id="31e6d-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31e6d-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="31e6d-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="31e6d-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="31e6d-114">**Level**</span><span class="sxs-lookup"><span data-stu-id="31e6d-114">**Level**</span></span>
<span data-ttu-id="31e6d-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="31e6d-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="31e6d-116">Die dem-Objekt zugeordnete Prioritätsstufe.</span><span class="sxs-lookup"><span data-stu-id="31e6d-116">The priority level associated with the object.</span></span>

<dt>

<span data-ttu-id="31e6d-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31e6d-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="31e6d-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="31e6d-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="31e6d-119">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="31e6d-119">**ObjectName**</span></span>
<span data-ttu-id="31e6d-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="31e6d-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="31e6d-121">Der Name eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="31e6d-121">The name of an object.</span></span>

<dt>

<span data-ttu-id="31e6d-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31e6d-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="31e6d-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="31e6d-123">Scripting data type: **BSTR**</span></span>
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

 

## <a name="requirements"></a><span data-ttu-id="31e6d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31e6d-124">Requirements</span></span>



| <span data-ttu-id="31e6d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31e6d-125">Requirement</span></span> | <span data-ttu-id="31e6d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="31e6d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31e6d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31e6d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="31e6d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31e6d-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31e6d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31e6d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="31e6d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31e6d-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31e6d-131">Header</span><span class="sxs-lookup"><span data-stu-id="31e6d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="31e6d-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="31e6d-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="31e6d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="31e6d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31e6d-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31e6d-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="31e6d-135">IID</span><span class="sxs-lookup"><span data-stu-id="31e6d-135">IID</span></span><br/>                      | <span data-ttu-id="31e6d-136">IID \_ iadstypedname ist als B371A349-4080-11d1-A3AC-00C04FB950DC definiert.</span><span class="sxs-lookup"><span data-stu-id="31e6d-136">IID\_IADsTypedName is defined as B371A349-4080-11D1-A3AC-00C04FB950DC</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="31e6d-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31e6d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31e6d-138">**IADsTypedName**</span><span class="sxs-lookup"><span data-stu-id="31e6d-138">**IADsTypedName**</span></span>](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[<span data-ttu-id="31e6d-139">**ADS \_ typedName**</span><span class="sxs-lookup"><span data-stu-id="31e6d-139">**ADS\_TYPEDNAME**</span></span>](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 





