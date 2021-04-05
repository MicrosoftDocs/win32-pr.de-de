---
title: Iadspropertyentry-Eigenschaften Methoden (IADs. h)
description: Gewähren Sie Zugriff auf die folgenden Eigenschaften.
ms.assetid: 73b0f6d4-55db-46cf-a781-e10bc4fcf2db
ms.tgt_platform: multiple
keywords:
- Iadspropertyentry-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPropertyEntry Property Methods
- IADsPropertyEntry.Name
- IADsPropertyEntry.get_Name
- IADsPropertyEntry.put_Name
- IADsPropertyEntry.ADsType
- IADsPropertyEntry.get_ADsType
- IADsPropertyEntry.put_ADsType
- IADsPropertyEntry.ControlCode
- IADsPropertyEntry.get_ControlCode
- IADsPropertyEntry.put_ControlCode
- IADsPropertyEntry.Values
- IADsPropertyEntry.get_Values
- IADsPropertyEntry.put_Values
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e82344b2b659395bb14c0500fde3214530e000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859254"
---
# <a name="iadspropertyentry-property-methods"></a><span data-ttu-id="7a7ec-104">Iadspropertyentry-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="7a7ec-104">IADsPropertyEntry Property Methods</span></span>

<span data-ttu-id="7a7ec-105">Die Eigenschaften Methoden der [**iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) -Schnittstelle ermöglichen den Zugriff auf die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-105">The property methods of the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface provide access to the following properties.</span></span> <span data-ttu-id="7a7ec-106">Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="7a7ec-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7a7ec-107">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a7ec-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="7a7ec-108">**Adstype**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-108">**ADsType**</span></span>
<span data-ttu-id="7a7ec-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a7ec-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a7ec-110">Der Datentyp der **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-110">The data type of the **Name** property.</span></span> <span data-ttu-id="7a7ec-111">Die Werte des-Datentyps werden in der [**adstyetenum**](/windows/win32/api/iads/ne-iads-adstypeenum) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-111">The values of the data type is defined in the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration.</span></span>

<dt>

<span data-ttu-id="7a7ec-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a7ec-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a7ec-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* plADsType
);
HRESULT put_ADsType(
  [in] LONG lADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a7ec-114">**ControlCode**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-114">**ControlCode**</span></span>
<span data-ttu-id="7a7ec-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a7ec-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a7ec-116">Eine-Konstante, die den Vorgang angibt, der für die benannte Eigenschaft ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-116">A constant that specifies the operation to be performed on the named property.</span></span> <span data-ttu-id="7a7ec-117">Der Wert wird in der Enumeration Aufzählung der [**ADS- \_ Eigenschaft \_ \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) definiert.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-117">The value is defined in the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="7a7ec-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a7ec-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a7ec-119">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-119">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ControlCode(
  [out] LONG* pControlCode
);
HRESULT put_ControlCode(
  [in] LONG lnControlCode
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a7ec-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-120">**Name**</span></span>
<span data-ttu-id="7a7ec-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a7ec-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a7ec-122">Der Name des Eigenschafts Eintrags.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-122">Name of the property entry.</span></span> <span data-ttu-id="7a7ec-123">Dieser Name muss dem Namen eines Attributs entsprechen, das im Schema definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-123">This name should correspond to the name of an attribute as defined in the schema.</span></span>

<dt>

<span data-ttu-id="7a7ec-124">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a7ec-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a7ec-125">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-125">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
HRESULT put_Name(
  [in] BSTR bstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7a7ec-126">**Werte**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-126">**Values**</span></span>
<span data-ttu-id="7a7ec-127"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7a7ec-127"></dt> <dd> <dl></span></span>

<span data-ttu-id="7a7ec-128">Ein **Variant** -Array.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-128">A **VARIANT** array.</span></span> <span data-ttu-id="7a7ec-129">Jedes Element in diesem Array stellt einen Wert der benannten Eigenschaft dar.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-129">Each element in this array represents a value of the named property.</span></span> <span data-ttu-id="7a7ec-130">Diese Eigenschaftswerte werden durch ADSI-Objekte dargestellt, die die [**iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) -und [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) -Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-130">Such property values are represented by ADSI objects implementing the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) and [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interfaces.</span></span> <span data-ttu-id="7a7ec-131">Daher enthält das **Variant** -Array ein Array von Zeigern auf die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle der ADSI-Objekte, die die **iadspropertyvalue** -und **IADsPropertyValue2** -Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-131">Therefore, the **VARIANT** array holds an array of pointers to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface on the ADSI objects implementing the **IADsPropertyValue** and **IADsPropertyValue2** interfaces.</span></span>

<dt>

<span data-ttu-id="7a7ec-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7a7ec-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a7ec-133">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Values(
  [out] VARIANT* pvValues
);
HRESULT put_Values(
  [in] VARIANT vValues
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="7a7ec-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a7ec-134">Remarks</span></span>

<span data-ttu-id="7a7ec-135">Jede Eigenschaften Methode unterstützt die standardmäßigen **HRESULT** -Rückgabewerte, einschließlich S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-135">Each property method supports the standard **HRESULT** return values, including S\_OK.</span></span> <span data-ttu-id="7a7ec-136">Weitere Informationen zu anderen Rückgabe Werten finden Sie unter [ADSI-Fehler Codes](adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7a7ec-136">For more information about other return values, see [ADSI Error Codes](adsi-error-codes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7a7ec-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a7ec-137">Examples</span></span>

<span data-ttu-id="7a7ec-138">Im folgenden Codebeispiel wird gezeigt, wie eine benannte Eigenschaft aus dem Cache abgerufen und ein neuer Eigenschaften Eintrag erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-138">The following code example shows how to retrieve a named property from the cache and create a new property entry.</span></span>


```VB
 
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup

'------------------------------------------------------------
'----- Getting IADsPropertyEntry ----------------------------
'------------------------------------------------------------
 
' Create the property list object.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a named property entry object.
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)

' Insert code to do something with propEntry
Set propEntry = Nothing
 
'------------------------------------------------------------
'---- Setting IADsPropertyEntry -----------------------------
'------------------------------------------------------------
 
' Create a property value object.
Set propVal = New PropertyValue
 
'---- Property Value -----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'---- Create a new Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' ---- Put the newly created property entry to the cache ----
propList.PutPropertyItem (propEntry)
 
' Commit the entry to the directory store.
propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="7a7ec-139">Im folgenden Codebeispiel wird gezeigt, wie Sie eine benannte Eigenschaft aus einem Cache erhalten.</span><span class="sxs-lookup"><span data-stu-id="7a7ec-139">The following code example shows how to get a named property from a cache.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADs *pObj = NULL;
VARIANT var;
long valType = ADSTYPE_CASE_IGNORE_STRING;
 
VariantInit(&var);
 
// Bind to directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){return;}
 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), valType, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Get the name and the type of the property entry.
BSTR nm = NULL;
hr = pEntry->get_Name(&nm);
printf("Property name = %S\n",nm);
VariantClear(&var);
long at;
hr = pEntry->get_ADsType(&at);
printf("Property type = %d\n",a);

Cleanup:
    if(nm)
        SysFreeString(nm);

    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pObj)
        pObj->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="7a7ec-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a7ec-140">Requirements</span></span>



| <span data-ttu-id="7a7ec-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a7ec-141">Requirement</span></span> | <span data-ttu-id="7a7ec-142">Wert</span><span class="sxs-lookup"><span data-stu-id="7a7ec-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7ec-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a7ec-143">Minimum supported client</span></span><br/> | <span data-ttu-id="7a7ec-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a7ec-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a7ec-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a7ec-145">Minimum supported server</span></span><br/> | <span data-ttu-id="7a7ec-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a7ec-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a7ec-147">Header</span><span class="sxs-lookup"><span data-stu-id="7a7ec-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a7ec-148"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a7ec-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="7a7ec-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7a7ec-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a7ec-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a7ec-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a7ec-151">IID</span><span class="sxs-lookup"><span data-stu-id="7a7ec-151">IID</span></span><br/>                      | <span data-ttu-id="7a7ec-152">IID \_ iadspropertyentry ist definiert als 05792c8e-941f -11D0-8529-00c04td8d503</span><span class="sxs-lookup"><span data-stu-id="7a7ec-152">IID\_IADsPropertyEntry is defined as 05792C8E-941F-11D0-8529-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="7a7ec-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a7ec-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a7ec-154">**Aufzählung der ADS- \_ Eigenschafts \_ Operation \_**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-154">**ADS\_PROPERTY\_OPERATION\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)
</dt> <dt>

[<span data-ttu-id="7a7ec-155">ADSI-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="7a7ec-155">ADSI Error Codes</span></span>](adsi-error-codes.md)
</dt> <dt>

[<span data-ttu-id="7a7ec-156">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-156">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="7a7ec-157">**Iadspropertyentry**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-157">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="7a7ec-158">**Iadspropertyvalue**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-158">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="7a7ec-159">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-159">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="7a7ec-160">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="7a7ec-160">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

