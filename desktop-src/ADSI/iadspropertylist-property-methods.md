---
title: IADsPropertyList-Eigenschaften Methoden (IADs. h)
description: Die Eigenschaften Methoden der IADsPropertyList-Schnittstelle lesen die in der folgenden Tabelle beschriebenen Eigenschaften. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 3564b61a-5950-4d00-8ea1-86fecd5c6c4e
ms.tgt_platform: multiple
keywords:
- IADsPropertyList-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPropertyList Property Methods
- IADsPropertyList.PropertyCount
- IADsPropertyList.get_PropertyCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f13494eeb502122216ffa0c73c24d5b707588e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859253"
---
# <a name="iadspropertylist-property-methods"></a><span data-ttu-id="4a2f5-105">IADsPropertyList-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="4a2f5-105">IADsPropertyList Property Methods</span></span>

<span data-ttu-id="4a2f5-106">Die Eigenschaften Methoden der [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Schnittstelle lesen die in der folgenden Tabelle beschriebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-106">The property methods of the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface read the properties described in the following table.</span></span> <span data-ttu-id="4a2f5-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="4a2f5-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4a2f5-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a2f5-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="4a2f5-109">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="4a2f5-109">**PropertyCount**</span></span>
<span data-ttu-id="4a2f5-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="4a2f5-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="4a2f5-111">Die Anzahl der Elemente in der Eigenschaften Liste.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-111">The number of items in the property list.</span></span>

<dt>

<span data-ttu-id="4a2f5-112">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4a2f5-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a2f5-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="4a2f5-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PropertyCount(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="4a2f5-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a2f5-114">Examples</span></span>

<span data-ttu-id="4a2f5-115">Im folgenden Codebeispiel wird gezeigt, wie die Anzahl von Elementen in einer Eigenschaften Liste bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-115">The following code example shows how to determine number of items in a property list.</span></span>


```VB
Dim propList As IADsPropertyList
Dim count As Long

On Error GoTo Cleanup
 
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
 
propList.GetInfo
count = propList.PropertyCount
Debug.Print "Number of Properties Found: " & count

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set propList = Nothing
```



<span data-ttu-id="4a2f5-116">Im folgenden Codebeispiel wird gezeigt, wie die Anzahl von Elementen in einer Eigenschaften Liste bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-116">The following code example shows how to determine number of items in a property list.</span></span>


```C++
int GetPropertyCacheCount(LPWSTR adsPath)
{
    IADsPropertyList *pList;
    IADs *pObj;
    HRESULT hr = S_OK;

    if(!adsPath)
    {
        _tprintf(TEXT("Invalid ADsPath."));
        return -1;
    }

    HRESULT hr = ADsGetObject(adsPath,
                          IID_IADsPropertyList,
                          (void**)&pList);
    // Initialize the property cache.
    hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
    pObj->GetInfo();
    pObj->Release();

    // Get the property count.
    hr = pList->get_PropertyCount(&count);
    pList->Release();

    // Return the property count if it succeeded, otherwise
    // return -1.

    if(SUCCEEDED(hr))
    {
        return count;
    }
    else
    {
        return -1;
    }

}
```



## <a name="requirements"></a><span data-ttu-id="4a2f5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a2f5-117">Requirements</span></span>



| <span data-ttu-id="4a2f5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a2f5-118">Requirement</span></span> | <span data-ttu-id="4a2f5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4a2f5-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2f5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a2f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2f5-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a2f5-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a2f5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a2f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2f5-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a2f5-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a2f5-124">Header</span><span class="sxs-lookup"><span data-stu-id="4a2f5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a2f5-125"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2f5-125"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="4a2f5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4a2f5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a2f5-127"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a2f5-127"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="4a2f5-128">IID</span><span class="sxs-lookup"><span data-stu-id="4a2f5-128">IID</span></span><br/>                      | <span data-ttu-id="4a2f5-129">IID \_ IADsPropertyList ist als C6F602B6-8F69-11D0-8528-00C04FD8D503 definiert.</span><span class="sxs-lookup"><span data-stu-id="4a2f5-129">IID\_IADsPropertyList is defined as C6F602B6-8F69-11D0-8528-00C04FD8D503</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="4a2f5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a2f5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2f5-131">**IADsPropertyList**</span><span class="sxs-lookup"><span data-stu-id="4a2f5-131">**IADsPropertyList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
</dt> <dt>

[<span data-ttu-id="4a2f5-132">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="4a2f5-132">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





