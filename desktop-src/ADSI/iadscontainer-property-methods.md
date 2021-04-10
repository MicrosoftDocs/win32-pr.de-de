---
title: IADsContainer-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der IADsContainer-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen und eine allgemeine Erörterung von Eigenschaften Methoden finden Sie unter Interface Property Methods.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- IADsContainer-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105152"
---
# <a name="iadscontainer-property-methods"></a><span data-ttu-id="516f6-105">IADsContainer-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="516f6-105">IADsContainer Property Methods</span></span>

<span data-ttu-id="516f6-106">Mit den Eigenschafts Methoden der [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="516f6-106">The property methods of the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="516f6-107">Weitere Informationen und eine allgemeine Erörterung von Eigenschaften Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="516f6-107">For more information, and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="516f6-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="516f6-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="516f6-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="516f6-109">**Count**</span></span>
<span data-ttu-id="516f6-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="516f6-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="516f6-111">Ruft die Anzahl der Elemente im Container ab.</span><span class="sxs-lookup"><span data-stu-id="516f6-111">Retrieves the number of items in the container.</span></span> <span data-ttu-id="516f6-112">Wenn **Filter** festgelegt ist, gibt **count** nur die Anzahl der gefilterten Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="516f6-112">When **Filter** is set, **Count** returns only the number of filtered items.</span></span>

<dt>

<span data-ttu-id="516f6-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="516f6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="516f6-114">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="516f6-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="516f6-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="516f6-115">**Filter**</span></span>
<span data-ttu-id="516f6-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="516f6-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="516f6-117">Ruft den Filter ab, mit dem Objektklassen in einer angegebenen Enumeration ausgewählt werden, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="516f6-117">Retrieves or sets the filter used to select object classes in a given enumeration.</span></span> <span data-ttu-id="516f6-118">Dabei handelt es sich um ein Variant-Array, bei dem es sich bei jedem Element um den Namen einer Schema Klasse handelt.</span><span class="sxs-lookup"><span data-stu-id="516f6-118">This is a variant array, each element of which is the name of a schema class.</span></span> <span data-ttu-id="516f6-119">Wenn **Filter** nicht festgelegt oder auf leer festgelegt ist, werden alle Objekte aller Klassen vom Enumerator abgerufen.</span><span class="sxs-lookup"><span data-stu-id="516f6-119">If **Filter** is not set or set to empty, all objects of all classes are retrieved by the enumerator.</span></span>

<dt>

<span data-ttu-id="516f6-120">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="516f6-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="516f6-121">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="516f6-121">Scripting data type: **VARIANT**</span></span>
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


</dt> </dl> </dd> <dt>

<span data-ttu-id="516f6-122">**Hinweise**</span><span class="sxs-lookup"><span data-stu-id="516f6-122">**Hints**</span></span>
<span data-ttu-id="516f6-123"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="516f6-123"></dt> <dd> <dl></span></span>

<span data-ttu-id="516f6-124">Ein Variant-Array von **BSTR** -Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="516f6-124">A variant array of **BSTR** strings.</span></span> <span data-ttu-id="516f6-125">Jedes Element identifiziert den Namen einer Eigenschaft, die in der Schema Definition gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="516f6-125">Each element identifies the name of a property found in the schema definition.</span></span> <span data-ttu-id="516f6-126">Der *vhints* -Parameter ermöglicht es dem Client, anzugeben, welche Attribute für jedes Enumerationsobjekt geladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="516f6-126">The *vHints* parameter enables the client to indicate which attributes to load for each enumerated object.</span></span> <span data-ttu-id="516f6-127">Diese Daten können verwendet werden, um den Netzwerk Zugriff zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="516f6-127">Such data may be used to optimize network access.</span></span> <span data-ttu-id="516f6-128">Die genaue Implementierung ist jedoch Anbieter spezifisch und wird zurzeit nicht vom WinNT-Anbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="516f6-128">The exact implementation, however, is provider-specific, and is currently not used by the WinNT provider.</span></span>

<dt>

<span data-ttu-id="516f6-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="516f6-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="516f6-130">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="516f6-130">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="516f6-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="516f6-131">Remarks</span></span>

<span data-ttu-id="516f6-132">Die enumerationsprozesse unter [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) und **IADsContainer:: get \_ count** werden für die enthaltenen Objekte im Cache ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="516f6-132">The enumeration processes under [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) and **IADsContainer::get\_Count** are performed against the contained objects in the cache.</span></span> <span data-ttu-id="516f6-133">Wenn ein Container eine große Anzahl von Objekten enthält, wirkt sich dies möglicherweise negativ auf die Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="516f6-133">When a container contains a large number of objects, the performance may be affected.</span></span> <span data-ttu-id="516f6-134">Um die Leistung zu verbessern, deaktivieren Sie den Cache, richten Sie eine geeignete Seitengröße ein, und verwenden Sie die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="516f6-134">To enhance performance, turn off the cache, set up an appropriate page size, and use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="516f6-135">Aus diesem Grund wird die Eigenschaft **get \_ count** im Microsoft LDAP-Anbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="516f6-135">For this reason, the **get\_Count** property is not supported in the Microsoft LDAP provider.</span></span>

## <a name="examples"></a><span data-ttu-id="516f6-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="516f6-136">Examples</span></span>

<span data-ttu-id="516f6-137">Im folgenden Visual Basic Codebeispiel wird gezeigt, wie Eigenschafts Methoden von [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="516f6-137">The following Visual Basic code example shows how property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span>


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



<span data-ttu-id="516f6-138">Im folgenden C++-Codebeispiel wird gezeigt, wie die-Eigenschaften Methoden von [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="516f6-138">The following C++ code example shows how the property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span> <span data-ttu-id="516f6-139">Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="516f6-139">For brevity, error checking is omitted.</span></span>


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="516f6-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="516f6-140">Requirements</span></span>



| <span data-ttu-id="516f6-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="516f6-141">Requirement</span></span> | <span data-ttu-id="516f6-142">Wert</span><span class="sxs-lookup"><span data-stu-id="516f6-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="516f6-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="516f6-143">Minimum supported client</span></span><br/> | <span data-ttu-id="516f6-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="516f6-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="516f6-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="516f6-145">Minimum supported server</span></span><br/> | <span data-ttu-id="516f6-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="516f6-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="516f6-147">Header</span><span class="sxs-lookup"><span data-stu-id="516f6-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="516f6-148"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="516f6-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="516f6-149">DLL</span><span class="sxs-lookup"><span data-stu-id="516f6-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="516f6-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="516f6-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="516f6-151">IID</span><span class="sxs-lookup"><span data-stu-id="516f6-151">IID</span></span><br/>                      | <span data-ttu-id="516f6-152">IID \_ IADsContainer ist definiert als 001677d0-SD16-11CE-abc4-02608c9e7553</span><span class="sxs-lookup"><span data-stu-id="516f6-152">IID\_IADsContainer is defined as 001677D0-FD16-11CE-ABC4-02608C9E7553</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="516f6-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="516f6-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516f6-154">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="516f6-154">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="516f6-155">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="516f6-155">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





