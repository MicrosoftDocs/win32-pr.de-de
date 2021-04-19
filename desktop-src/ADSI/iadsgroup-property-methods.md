---
title: IADsGroup-Eigenschaften Methoden (IADs. h)
description: Eigenschaften Methoden der IADsGroup-Schnittstelle.
ms.assetid: a8aa88d4-4695-47bc-bf7f-a17236a5671c
ms.tgt_platform: multiple
keywords:
- IADsGroup-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsGroup Property Methods
- IADsGroup.Description
- IADsGroup.get_Description
- IADsGroup.put_Description
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 665cb91a55298012e4e906c2972da5371e3960be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346320"
---
# <a name="iadsgroup-property-methods"></a><span data-ttu-id="f0db9-104">IADsGroup-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="f0db9-104">IADsGroup Property Methods</span></span>

<span data-ttu-id="f0db9-105">Mit den Eigenschafts Methoden der [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) -Schnittstelle werden die folgenden Eigenschaften gelesen und geschrieben.</span><span class="sxs-lookup"><span data-stu-id="f0db9-105">The property methods of the [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) interface read and write the following properties.</span></span> <span data-ttu-id="f0db9-106">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f0db9-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f0db9-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f0db9-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f0db9-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0db9-108">**Description**</span></span>
<span data-ttu-id="f0db9-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f0db9-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="f0db9-110">Gibt die Textbeschreibung der Gruppenmitgliedschaft an.</span><span class="sxs-lookup"><span data-stu-id="f0db9-110">Indicates the textual description of the group membership.</span></span>

<dt>

<span data-ttu-id="f0db9-111">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f0db9-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f0db9-112">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f0db9-112">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="f0db9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f0db9-113">Remarks</span></span>

### <a name="using-iadsgroup-to-retrieve-descriptions-of-built-in-groups"></a><span data-ttu-id="f0db9-114">Verwenden von IADsGroup zum Abrufen von Beschreibungen integrierter Gruppen</span><span class="sxs-lookup"><span data-stu-id="f0db9-114">Using IADsGroup to Retrieve Descriptions of Built-in Groups</span></span>

<span data-ttu-id="f0db9-115">In den folgenden Beispielen wird gezeigt, wie Informationen zu Windows-Gruppen Objekten nach Namen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f0db9-115">The following examples show how to retrieve information about Windows group objects by name.</span></span> <span data-ttu-id="f0db9-116">In einer mehrsprachigen Umgebung sind integrierte Gruppen manchmal durch unterschiedliche lokalisierte Namen bekannt. Dies bedeutet, dass Sie nicht direkt mithilfe von Zeichen folgen Bezeichnerzeichen (z. b. "Winnt://Microsoft/Administrators") abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="f0db9-116">In a multilingual environment, built-in groups are sometimes known by different localized names, which means that they cannot be retrieved directly by using string identifiers such as "WinNT://Microsoft/Administrators".</span></span> <span data-ttu-id="f0db9-117">In diesem Fall kann der Benutzer an das bekannte SID-Objekt für die Gruppe binden, den lokalisierten Gruppennamen abrufen und ihn für die GetObject-Methode bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f0db9-117">In that case, the user can bind to the well-known SID object for the group, retrieve the localized group name, and supply that to the GetObject method.</span></span> <span data-ttu-id="f0db9-118">Weitere Informationen finden Sie unter [Bekannte SIDs](/windows/desktop/SecAuthZ/well-known-sids).</span><span class="sxs-lookup"><span data-stu-id="f0db9-118">For more information, see [Well-known SIDs](/windows/desktop/SecAuthZ/well-known-sids).</span></span>

## <a name="examples"></a><span data-ttu-id="f0db9-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0db9-119">Examples</span></span>

<span data-ttu-id="f0db9-120">Im folgenden Visual Basic Beispiel wird gezeigt, wie eine Bindung an ein Gruppen Objekt und die Beschreibung der Gruppe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f0db9-120">The following Visual Basic example shows how to bind to a group object and display the description of the group.</span></span>


```VB
Dim grp As IADsGroup
On Error GoTo Cleanup

Set grp = GetObject("WinNT://Microsoft/Administrators")
Debug.Print grp.Description

Cleanup
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set grp = Nothing
```



<span data-ttu-id="f0db9-121">Im folgenden C++-Beispiel wird gezeigt, wie eine Bindung an ein Gruppen Objekt erfolgen und die Beschreibung der Gruppe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f0db9-121">The following C++ example shows how to bind to a group object and display the description of the group.</span></span>


```C++
IADsGroup *pGroup = NULL;
HRESULT hr = S_OK;
LPWSTR adsPath = L"WinNT://localHost/Administrators";
BSTR bstr;

hr = ADsGetObject(adsPath,IID_IADsGroup,(void**)&pGroup);

if(FAILED(hr)) {goto Cleanup;}

hr = pGroup->get_Description(&bstr);
if(FAILED(hr)) {goto Cleanup;}

printf("Description: %S\n",bstr);

Cleanup:
    SysFreeString(bstr);
    if(pGroup) 
        pGroup->Release();

    return hr;
```



## <a name="requirements"></a><span data-ttu-id="f0db9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0db9-122">Requirements</span></span>



| <span data-ttu-id="f0db9-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0db9-123">Requirement</span></span> | <span data-ttu-id="f0db9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="f0db9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0db9-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0db9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f0db9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0db9-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0db9-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0db9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f0db9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0db9-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0db9-129">Header</span><span class="sxs-lookup"><span data-stu-id="f0db9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0db9-130"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0db9-130"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f0db9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f0db9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0db9-132"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0db9-132"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0db9-133">IID</span><span class="sxs-lookup"><span data-stu-id="f0db9-133">IID</span></span><br/>                      | <span data-ttu-id="f0db9-134">IID \_ IADsGroup ist als 27636b00-410f-11CF-B1FF-02608c9e7553 definiert.</span><span class="sxs-lookup"><span data-stu-id="f0db9-134">IID\_IADsGroup is defined as 27636B00-410F-11CF-B1FF-02608C9E7553</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f0db9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0db9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0db9-136">**IADs**</span><span class="sxs-lookup"><span data-stu-id="f0db9-136">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="f0db9-137">**IADsGroup**</span><span class="sxs-lookup"><span data-stu-id="f0db9-137">**IADsGroup**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsgroup)
</dt> <dt>

[<span data-ttu-id="f0db9-138">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="f0db9-138">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

