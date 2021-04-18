---
title: Iadssyntax-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadssyntax-Schnittstelle werden die in der folgenden Tabelle aufgeführten Eigenschaften festgelegt oder festgelegt. Weitere Informationen zu Eigenschafts Methoden finden Sie unter Interface Property Methods.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- Iadssyntax-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517657"
---
# <a name="iadssyntax-property-methods"></a><span data-ttu-id="0fa67-105">Iadssyntax-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="0fa67-105">IADsSyntax Property Methods</span></span>

<span data-ttu-id="0fa67-106">Mit den Eigenschafts Methoden der [**iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) -Schnittstelle werden die in der folgenden Tabelle aufgeführten Eigenschaften festgelegt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0fa67-106">The property methods of the [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="0fa67-107">Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0fa67-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0fa67-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0fa67-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0fa67-109">**Oleautodatatype**</span><span class="sxs-lookup"><span data-stu-id="0fa67-109">**OleAutoDataType**</span></span>
<span data-ttu-id="0fa67-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0fa67-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0fa67-111">Ruft eine **Länge** ab und legt Sie fest, die den Wert der **VT \_ xxx** -Konstante für den Automatisierungs Datentyp enthält, der diese Syntax darstellt.</span><span class="sxs-lookup"><span data-stu-id="0fa67-111">Retrieves and sets a **LONG** that contains the value of the **VT\_xxx** constant for the Automation data type that represents this syntax.</span></span>

<span data-ttu-id="0fa67-112">Active Directory unterstützt die folgenden **VT \_ xxx** -Konstanten für den Automatisierungs Datentyp, der diese Syntax darstellt:</span><span class="sxs-lookup"><span data-stu-id="0fa67-112">Active Directory supports the following **VT\_xxx** constants for the Automation data type that represents this syntax:</span></span>

-   <span data-ttu-id="0fa67-113">**VT \_ Boolescher** bool</span><span class="sxs-lookup"><span data-stu-id="0fa67-113">**VT\_BOOL** BOOL</span></span>
-   <span data-ttu-id="0fa67-114">**VT \_ BSTR** BSTR</span><span class="sxs-lookup"><span data-stu-id="0fa67-114">**VT\_BSTR** BSTR</span></span>
-   <span data-ttu-id="0fa67-115">**VT \_ bstraut** (bstraut)</span><span class="sxs-lookup"><span data-stu-id="0fa67-115">**VT\_BSTRT** BSTRT</span></span>
-   <span data-ttu-id="0fa67-116">**VT \_ CY** -Währung</span><span class="sxs-lookup"><span data-stu-id="0fa67-116">**VT\_CY** CURRENCY</span></span>
-   <span data-ttu-id="0fa67-117">**VT \_ Datums** Datum</span><span class="sxs-lookup"><span data-stu-id="0fa67-117">**VT\_DATE** Date</span></span>
-   <span data-ttu-id="0fa67-118">**VT \_ leere** **null**</span><span class="sxs-lookup"><span data-stu-id="0fa67-118">**VT\_EMPTY** **NULL**</span></span>
-   <span data-ttu-id="0fa67-119">**VT \_ Fehler** ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0fa67-119">**VT\_ERROR** Not valid</span></span>
-   <span data-ttu-id="0fa67-120">**VT \_ I2** Short</span><span class="sxs-lookup"><span data-stu-id="0fa67-120">**VT\_I2** short</span></span>
-   <span data-ttu-id="0fa67-121">**VT \_ I4** Long</span><span class="sxs-lookup"><span data-stu-id="0fa67-121">**VT\_I4** long</span></span>
-   <span data-ttu-id="0fa67-122">**VT \_ R4** Real</span><span class="sxs-lookup"><span data-stu-id="0fa67-122">**VT\_R4** real</span></span>
-   <span data-ttu-id="0fa67-123">**VT \_ R8** Double</span><span class="sxs-lookup"><span data-stu-id="0fa67-123">**VT\_R8** double</span></span>
-   <span data-ttu-id="0fa67-124">**VT \_ UI1** Byte</span><span class="sxs-lookup"><span data-stu-id="0fa67-124">**VT\_UI1** BYTE</span></span>

<dt>

<span data-ttu-id="0fa67-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0fa67-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0fa67-126">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="0fa67-126">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="0fa67-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fa67-127">Remarks</span></span>

<span data-ttu-id="0fa67-128">Ein Array von Bytes ohne Vorzeichen, **VT \_ UI1** \| **VT \_ Array** , könnte bedeuten, dass der Anbieter eine Syntax zugeordnet hat, die keinem virtuellen Automatisierungs Typ zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fa67-128">An array of unsigned bytes, **VT\_UI1**\|**VT\_ARRAY** could mean that the provider has mapped a syntax that cannot be mapped to an Automation virtual type.</span></span>

## <a name="examples"></a><span data-ttu-id="0fa67-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0fa67-129">Examples</span></span>

<span data-ttu-id="0fa67-130">Im folgenden Codebeispiel wird die Syntax des **operatingsystemversion** -Attributs eines Computers in einem Netzwerk über den WinNT-Anbieter untersucht.</span><span class="sxs-lookup"><span data-stu-id="0fa67-130">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="0fa67-131">Die Ergebnis Syntax ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0fa67-131">The result syntax is a string.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



<span data-ttu-id="0fa67-132">Im folgenden Codebeispiel wird die Syntax des **operatingsystemversion** -Attributs eines Computers in einem Netzwerk über den WinNT-Anbieter untersucht.</span><span class="sxs-lookup"><span data-stu-id="0fa67-132">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="0fa67-133">Die Ergebnis Syntax ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0fa67-133">The result syntax is a string.</span></span> <span data-ttu-id="0fa67-134">Aus Gründen der Übersichtlichkeit wird die Fehlerüberprüfung ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="0fa67-134">For brevity, error checking is omitted.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a><span data-ttu-id="0fa67-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fa67-135">Requirements</span></span>



| <span data-ttu-id="0fa67-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fa67-136">Requirement</span></span> | <span data-ttu-id="0fa67-137">Wert</span><span class="sxs-lookup"><span data-stu-id="0fa67-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa67-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fa67-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0fa67-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fa67-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fa67-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fa67-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0fa67-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fa67-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fa67-142">Header</span><span class="sxs-lookup"><span data-stu-id="0fa67-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fa67-143"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fa67-143"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="0fa67-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0fa67-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fa67-145"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fa67-145"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="0fa67-146">IID</span><span class="sxs-lookup"><span data-stu-id="0fa67-146">IID</span></span><br/>                      | <span data-ttu-id="0fa67-147">IID \_ iadssyntax ist als C8F93DD2-4AE0-11CF-9E73-00AA004A5691 definiert.</span><span class="sxs-lookup"><span data-stu-id="0fa67-147">IID\_IADsSyntax is defined as C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0fa67-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fa67-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fa67-149">**Iadsclass**</span><span class="sxs-lookup"><span data-stu-id="0fa67-149">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="0fa67-150">**Iadsproperty**</span><span class="sxs-lookup"><span data-stu-id="0fa67-150">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="0fa67-151">**Iadssyntax**</span><span class="sxs-lookup"><span data-stu-id="0fa67-151">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





