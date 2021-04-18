---
title: Iadsproperty-Eigenschaften Methoden (IADs. h)
description: Lesen und schreiben Sie die in der folgenden Tabelle beschriebenen Eigenschaften.
ms.assetid: dd348a3c-0386-4fa2-984d-cdea6f09bd72
ms.tgt_platform: multiple
keywords:
- Iadsproperty-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsProperty Property Methods
- IADsProperty.OID
- IADsProperty.get_OID
- IADsProperty.put_OID
- IADsProperty.Syntax
- IADsProperty.get_Syntax
- IADsProperty.put_Syntax
- IADsProperty.MaxRange
- IADsProperty.get_MaxRange
- IADsProperty.put_MaxRange
- IADsProperty.MinRange
- IADsProperty.get_MinRange
- IADsProperty.put_MinRange
- IADsProperty.MultiValued
- IADsProperty.get_MultiValued
- IADsProperty.put_MultiValued
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233bd5411e1c82956ef745255418a1b176af5900
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340975"
---
# <a name="iadsproperty-property-methods"></a><span data-ttu-id="d5439-104">Iadsproperty-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="d5439-104">IADsProperty Property Methods</span></span>

<span data-ttu-id="d5439-105">Die Eigenschaften Methoden der [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) -Schnittstelle lesen und schreiben die in der folgenden Tabelle beschriebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d5439-105">The property methods of the [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interface read and write the properties described in the following table.</span></span> <span data-ttu-id="d5439-106">Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d5439-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d5439-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d5439-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d5439-108">**Maxrange**</span><span class="sxs-lookup"><span data-stu-id="d5439-108">**MaxRange**</span></span>
<span data-ttu-id="d5439-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d5439-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="d5439-110">Obere Grenze der Werte.</span><span class="sxs-lookup"><span data-stu-id="d5439-110">Upper limit of values.</span></span>

<dt>

<span data-ttu-id="d5439-111">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5439-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d5439-112">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="d5439-112">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxRange(
  [out] LONG* lnMaxRange
);
HRESULT put_MaxRange(
  [in] LONG lnMaxRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5439-113">**Minrange**</span><span class="sxs-lookup"><span data-stu-id="d5439-113">**MinRange**</span></span>
<span data-ttu-id="d5439-114"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d5439-114"></dt> <dd> <dl></span></span>

<span data-ttu-id="d5439-115">Niedrigerer Grenzwert für Werte.</span><span class="sxs-lookup"><span data-stu-id="d5439-115">Lower limit of values.</span></span>

<dt>

<span data-ttu-id="d5439-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5439-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d5439-117">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="d5439-117">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinRange(
  [out] LONG* lnMinRange
);
HRESULT put_MinRange(
  [in] LONG lnMinRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5439-118">**Mehrwertigen**</span><span class="sxs-lookup"><span data-stu-id="d5439-118">**MultiValued**</span></span>
<span data-ttu-id="d5439-119"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d5439-119"></dt> <dd> <dl></span></span>

<span data-ttu-id="d5439-120">Gibt an, ob eine Eigenschaft einzelne oder mehrere Werte unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5439-120">Whether property supports single or multiple values.</span></span>

<dt>

<span data-ttu-id="d5439-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5439-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d5439-122">Skript Datentyp: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d5439-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MultiValued(
  [out] VARIANT_BOOL* fMultivalued
);
HRESULT put_MultiValued(
  [in] VARIANT_BOOL fMultivalued
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5439-123">**OID**</span><span class="sxs-lookup"><span data-stu-id="d5439-123">**OID**</span></span>
<span data-ttu-id="d5439-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d5439-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="d5439-125">Verzeichnis spezifischer Objekt Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d5439-125">Directory-specific object identifier.</span></span>

<dt>

<span data-ttu-id="d5439-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5439-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d5439-127">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d5439-127">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* bstrOID
);
HRESULT put_OID(
  [out] BSTR* bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5439-128">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="d5439-128">**Syntax**</span></span>
<span data-ttu-id="d5439-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d5439-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="d5439-130">Relativer Pfad des Syntax Objekts.</span><span class="sxs-lookup"><span data-stu-id="d5439-130">Relative path of syntax object.</span></span>

<dt>

<span data-ttu-id="d5439-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="d5439-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d5439-132">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d5439-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Syntax(
  [out] BSTR* bstrSyntax
);
HRESULT put_Syntax(
  [in] BSTR* bstrSyntax
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="d5439-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5439-133">Examples</span></span>

<span data-ttu-id="d5439-134">Im folgenden Codebeispiel wird das **OperatingSystem** -Attribut eines Computers in einem Netzwerk über den WinNT-Anbieter untersucht.</span><span class="sxs-lookup"><span data-stu-id="d5439-134">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sc As IADsContainer

On Error GoTo Cleanup
 
Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystem")
 
MsgBox "Attribute:  " & pr.Name
MsgBox "Syntax:     " & pr.Syntax
MsgBox "MaxRange:   " & pr.MaxRange
MsgBox "MinRange:   " & pr.MinRange
MsgBox "Multivalued:" & pr.Multivalued

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sc = Nothing
```



<span data-ttu-id="d5439-135">Im folgenden Codebeispiel wird das **OperatingSystem** -Attribut eines Computers in einem Netzwerk über den WinNT-Anbieter untersucht.</span><span class="sxs-lookup"><span data-stu-id="d5439-135">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="d5439-136">Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="d5439-136">For brevity, error checking is omitted.</span></span>


```C++
IADs *pADs = NULL;
IADsClass *pCls = NULL;
IADsProperty* pProp = NULL;
IADsContainer *pCont = NULL;
long lval;
short bval;
HRESULT hr = CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine,computer",
                  IID_IADs, (void**)&pADs);
if(FAILED(hr))
    goto Cleanup;

BSTR bstr;
hr = pADs->get_Schema(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsClass, (void**)&pCls);
hr = pCls->get_Parent(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr))
    goto Cleanup;
SysFreeString(bstr);

hr = pCont->GetObject(CComBSTR("Property"), CComBSTR("OperatingSystem"), (IDispatch**)&pProp);
if(FAILED(hr))
    goto Cleanup;

hr = pProp->get_Name(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Name : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_Syntax(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Syntax : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_MaxRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MaxRange : %d\n",lval);
SysFreeString(bstr);

hr = pProp->get_MinRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MinRange : %d\n", lval);
SysFreeString(bstr);

hr = pProp->get_Multivalued(&bval);
if(FAILED(hr))
    goto Cleanup;
printf(" MultiValued : %b\n",bval);
SysFreeString(bstr);

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    if(pCont)
        pCont->Release();

    if(pProp)
        pProp->Release(); 
 
CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="d5439-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5439-137">Requirements</span></span>



| <span data-ttu-id="d5439-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5439-138">Requirement</span></span> | <span data-ttu-id="d5439-139">Wert</span><span class="sxs-lookup"><span data-stu-id="d5439-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5439-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5439-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d5439-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5439-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5439-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5439-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d5439-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5439-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5439-144">Header</span><span class="sxs-lookup"><span data-stu-id="d5439-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5439-145"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5439-145"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d5439-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d5439-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5439-147"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5439-147"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d5439-148">IID</span><span class="sxs-lookup"><span data-stu-id="d5439-148">IID</span></span><br/>                      | <span data-ttu-id="d5439-149">IID \_ iadsproperty ist als C8F93DD3-4AE0-11CF-9E73-00AA004A5691 definiert.</span><span class="sxs-lookup"><span data-stu-id="d5439-149">IID\_IADsProperty is defined as C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d5439-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5439-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5439-151">**Iadsclass**</span><span class="sxs-lookup"><span data-stu-id="d5439-151">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="d5439-152">**Iadsproperty**</span><span class="sxs-lookup"><span data-stu-id="d5439-152">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="d5439-153">**Iadssyntax**</span><span class="sxs-lookup"><span data-stu-id="d5439-153">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





