---
title: Iadsmembers-Eigenschaften Methoden (IADs. h)
description: Mit den Methoden der iadsmembers-Schnittstelle werden die in diesem Thema beschriebenen Eigenschaften gelesen und geschrieben. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: ed4e98e5-053c-4d3b-bcd0-3add96bbe120
ms.tgt_platform: multiple
keywords:
- Iadsmembers-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsMembers Property Methods
- IADsMembers.Count
- IADsMembers.get_Count
- IADsMembers.Filter
- IADsMembers.get_Filter
- IADsMembers.put_Filter
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af047d6fe52fdd7d808b1d7e5dbfb35303d3ff59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343459"
---
# <a name="iadsmembers-property-methods"></a><span data-ttu-id="1dd2c-105">Iadsmembers-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="1dd2c-105">IADsMembers Property Methods</span></span>

<span data-ttu-id="1dd2c-106">Mit den Methoden der [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) -Schnittstelle werden die in diesem Thema beschriebenen Eigenschaften gelesen und geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-106">The methods of the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface read and write the properties described in this topic.</span></span> <span data-ttu-id="1dd2c-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="1dd2c-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="1dd2c-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1dd2c-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="1dd2c-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="1dd2c-109">**Count**</span></span>
<span data-ttu-id="1dd2c-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dd2c-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dd2c-111">Gibt die Anzahl der Elemente im Container an.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-111">Indicates the number of items in the container.</span></span> <span data-ttu-id="1dd2c-112">Wenn der Filter festgelegt ist, gibt count nur die Anzahl der Elemente zurück, die der Filter Beschreibung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-112">If the filter is set then count returns only the number of items that fit the filter description.</span></span>

<dt>

<span data-ttu-id="1dd2c-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1dd2c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dd2c-114">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="1dd2c-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCountr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="1dd2c-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="1dd2c-115">**Filter**</span></span>
<span data-ttu-id="1dd2c-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="1dd2c-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="1dd2c-117">Gibt den Filter an.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-117">Indicates the filter.</span></span> <span data-ttu-id="1dd2c-118">Die Syntax der Einträge im Filter Array entspricht dem Filter, der in der [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-118">The syntax of the entries in the filter array is the same as the Filter used on the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface.</span></span>

<dt>

<span data-ttu-id="1dd2c-119">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="1dd2c-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1dd2c-120">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1dd2c-120">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="1dd2c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dd2c-121">Remarks</span></span>

<span data-ttu-id="1dd2c-122">Die ADSI-Systemanbieter unterstützen die **iadsmembers:: get \_ count** -Eigenschaften Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-122">The ADSI system providers do not support the **IADsMembers::get\_Count** property method.</span></span>

## <a name="examples"></a><span data-ttu-id="1dd2c-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1dd2c-123">Examples</span></span>

<span data-ttu-id="1dd2c-124">Im folgenden Codebeispiel wird gezeigt, wie die Eigenschaften Methoden dieser Schnittstelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-124">The following code example shows how to use the property methods of this interface.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://myComputer/someGroup")
grp.members.filter = Array("user")
For Each usr In grp.Members
    MsgBox usr.Name & "," & usr.Class & "," & usr.AdsPath
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="1dd2c-125">Im folgenden Codebeispiel wird die **iadsmembers::p UT- \_ Filter** Methode verwendet, um eine Enumeration der Auflistung von Mitgliedern einer Gruppe vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="1dd2c-125">The following code example uses the **IADsMembers::put\_Filter** method to prepare for an enumeration of the collection of members of a group.</span></span>


```C++
IADsGroup *pGroup;
HRESULT hr = S_OK;

LPWSTR grpPath = L"WinNT://myComputer/someGroup";
hr = ADsGetObject(grpPath,IID_IADsGroup,(void**)&pGroup);
if(FAILED(hr)){goto Cleanup;}

IADsMembers *pMembers;
hr = pGroup->Members(&pMembers);
if(FAILED(hr)){goto Cleanup;}

hr = pGroup->Release();

SAFEARRAY *sa = CreateSafeArray(L"user");
hr = pMembers->put_Filter(sa);
if(FAILED(hr)){goto Cleanup;}

hr = EnumMembers(pMembers);    // For more information, and a 
                               // code example, see 
                               // IADsMembers::get__NewEnum.
if(FAILED(hr)){goto Cleanup;}

Cleanup:
    if(pGroup) pGroup->Release();
    if(pMembers) pMembers->Release();
    return hr;
```



## <a name="requirements"></a><span data-ttu-id="1dd2c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dd2c-126">Requirements</span></span>



| <span data-ttu-id="1dd2c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dd2c-127">Requirement</span></span> | <span data-ttu-id="1dd2c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1dd2c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd2c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1dd2c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd2c-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1dd2c-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1dd2c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1dd2c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd2c-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dd2c-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1dd2c-133">Header</span><span class="sxs-lookup"><span data-stu-id="1dd2c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dd2c-134"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd2c-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="1dd2c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1dd2c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dd2c-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dd2c-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="1dd2c-137">IID</span><span class="sxs-lookup"><span data-stu-id="1dd2c-137">IID</span></span><br/>                      | <span data-ttu-id="1dd2c-138">IID \_ iadsmembers ist definiert als 451a0030-72ec-11CF-b03b-00aa006e0975</span><span class="sxs-lookup"><span data-stu-id="1dd2c-138">IID\_IADsMembers is defined as 451A0030-72EC-11CF-B03B-00AA006E0975</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1dd2c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dd2c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd2c-140">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="1dd2c-140">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="1dd2c-141">**Iadsmembers:: get \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="1dd2c-141">**IADsMembers::get\_\_NewEnum**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum)
</dt> <dt>

[<span data-ttu-id="1dd2c-142">**Iadsmembers**</span><span class="sxs-lookup"><span data-stu-id="1dd2c-142">**IADsMembers**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsmembers)
</dt> <dt>

[<span data-ttu-id="1dd2c-143">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="1dd2c-143">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





