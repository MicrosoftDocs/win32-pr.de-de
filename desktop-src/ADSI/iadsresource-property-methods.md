---
title: Iadsresource-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsresource-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Eine allgemeine Erörterung von Eigenschaften Methoden finden Sie unter Schnittstellen Eigenschafts Methoden.
ms.assetid: a2d6ed76-88e9-468f-928a-a038b73fb362
ms.tgt_platform: multiple
keywords:
- Iadsresource-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsResource Property Methods
- IADsResource.LockCount
- IADsResource.get_LockCount
- IADsResource.Path
- IADsResource.get_Path
- IADsResource.User
- IADsResource.get_User
- IADsResource.UserPath
- IADsResource.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0f2ab2642dd8d03062a26d096190cf7615977a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339563"
---
# <a name="iadsresource-property-methods"></a><span data-ttu-id="ce6af-105">Iadsresource-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="ce6af-105">IADsResource Property Methods</span></span>

<span data-ttu-id="ce6af-106">Mit den Eigenschafts Methoden der [**iadsresource**](/windows/desktop/api/Iads/nn-iads-iadsresource) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce6af-106">The property methods of the [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="ce6af-107">Eine allgemeine Erörterung von Eigenschaften Methoden finden Sie unter [Schnittstellen Eigenschafts Methoden](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ce6af-107">For a general discussion of property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ce6af-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce6af-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="ce6af-109">**Sperr Anzahl**</span><span class="sxs-lookup"><span data-stu-id="ce6af-109">**LockCount**</span></span>
<span data-ttu-id="ce6af-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ce6af-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="ce6af-111">Anzahl der Sperren für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="ce6af-111">Number of locks on the resource.</span></span>

<dt>

<span data-ttu-id="ce6af-112">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce6af-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce6af-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="ce6af-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockCount(
  [out] LONG* plLockCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce6af-114">**Pfad**</span><span class="sxs-lookup"><span data-stu-id="ce6af-114">**Path**</span></span>
<span data-ttu-id="ce6af-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ce6af-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="ce6af-116">Der Dateisystempfad der geöffneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="ce6af-116">The file system path of the opened resource.</span></span>

<dt>

<span data-ttu-id="ce6af-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce6af-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce6af-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ce6af-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce6af-119">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="ce6af-119">**User**</span></span>
<span data-ttu-id="ce6af-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ce6af-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="ce6af-121">Der Name des Benutzers, der die Ressource geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="ce6af-121">The name of the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="ce6af-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce6af-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce6af-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ce6af-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce6af-124">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="ce6af-124">**UserPath**</span></span>
<span data-ttu-id="ce6af-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="ce6af-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="ce6af-126">Der ADsPath des Benutzer Objekts für den Benutzer, der die Ressource geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="ce6af-126">The ADsPath of the user object for the user who opened the resource.</span></span>

<dt>

<span data-ttu-id="ce6af-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ce6af-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce6af-128">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ce6af-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="ce6af-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce6af-129">Examples</span></span>

<span data-ttu-id="ce6af-130">Im folgenden Codebeispiel wird veranschaulicht, wie Sie offene Ressourcen eines Datei Dienstanbieter untersuchen.</span><span class="sxs-lookup"><span data-stu-id="ce6af-130">The following code example shows how to examine open resources of a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate resources.
If (IsEmpty(fso) = False) Then
    For Each resource In fso.resources
        MsgBox "Resource name: " & resource.name
        MsgBox "Resource path: " & resource.path
    Next resource
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="ce6af-131">Im folgenden Codebeispiel wird eine Auflistung von Ressourcen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ce6af-131">The following code example enumerates a collection of resources.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsResource *pRes = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
IEnumVARIANT *pEnum = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
HRESULT hr = S_OK;

LPWSTR adsPath =L"WinNT://aMachine/LanmanServer";
hr = ADsGetObject(adsPath, IID_IADsFileServiceOperations,(void**)&pFso);
if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Resources(&pColl);
if(FAILED(hr)) {goto Cleanup;}


// Enumerate print jobs. Code omitted.
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
VariantInit(&var);
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsResource, (void**)&pRes);
        pRes->get_Name(&bstr);
        printf("Resource name: %S\n",bstr);
        SysFreeString(bstr);
        pRes->get_Path(&bstr);
        printf("Resource path: %S\n",bstr);
        SysFreeString(bstr);
        pRes->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pRes) pRes->Release();
    if(pDisp) pDisp->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pFso) pFso->Release();
```



## <a name="requirements"></a><span data-ttu-id="ce6af-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce6af-132">Requirements</span></span>



| <span data-ttu-id="ce6af-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce6af-133">Requirement</span></span> | <span data-ttu-id="ce6af-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ce6af-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6af-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce6af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ce6af-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce6af-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce6af-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce6af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ce6af-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce6af-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce6af-139">Header</span><span class="sxs-lookup"><span data-stu-id="ce6af-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce6af-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce6af-140"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="ce6af-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ce6af-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce6af-142"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce6af-142"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="ce6af-143">IID</span><span class="sxs-lookup"><span data-stu-id="ce6af-143">IID</span></span><br/>                      | <span data-ttu-id="ce6af-144">IID \_ iadsresource ist als 34a05b20-4aab-11CF-ae2c-00aa006ebfb9 definiert.</span><span class="sxs-lookup"><span data-stu-id="ce6af-144">IID\_IADsResource is defined as 34A05B20-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="ce6af-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce6af-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6af-146">**Iadsresource**</span><span class="sxs-lookup"><span data-stu-id="ce6af-146">**IADsResource**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsresource)
</dt> <dt>

[<span data-ttu-id="ce6af-147">**Iadsfileserviceoperations:: Resources**</span><span class="sxs-lookup"><span data-stu-id="ce6af-147">**IADsFileServiceOperations::Resources**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-resources)
</dt> </dl>

 

 





