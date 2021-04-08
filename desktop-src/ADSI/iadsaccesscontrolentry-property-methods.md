---
title: IADsAccessControlEntry-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der IADsAccessControlEntry-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften ermittelt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: dce11723-0e30-4baa-8666-0a32f0968ebb
ms.tgt_platform: multiple
keywords:
- IADsAccessControlEntry-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsAccessControlEntry Property Methods
- IADsAccessControlEntry.AccessMask
- IADsAccessControlEntry.get_AccessMask
- IADsAccessControlEntry.put_AccessMask
- IADsAccessControlEntry.AceType
- IADsAccessControlEntry.get_AceType
- IADsAccessControlEntry.put_AceType
- IADsAccessControlEntry.AceFlags
- IADsAccessControlEntry.get_AceFlags
- IADsAccessControlEntry.put_AceFlags
- IADsAccessControlEntry.Flags
- IADsAccessControlEntry.get_Flags
- IADsAccessControlEntry.put_Flags
- IADsAccessControlEntry.ObjectType
- IADsAccessControlEntry.get_ObjectType
- IADsAccessControlEntry.put_ObjectType
- IADsAccessControlEntry.InheritedObjectType
- IADsAccessControlEntry.get_InheritedObjectType
- IADsAccessControlEntry.put_InheritedObjectType
- IADsAccessControlEntry.Trustee
- IADsAccessControlEntry.get_Trustee
- IADsAccessControlEntry.put_Trustee
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8539807f21944ab6f4b2c03f04b14a53dffdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740528"
---
# <a name="iadsaccesscontrolentry-property-methods"></a><span data-ttu-id="fd670-105">IADsAccessControlEntry-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="fd670-105">IADsAccessControlEntry Property Methods</span></span>

<span data-ttu-id="fd670-106">Mit den Eigenschafts Methoden der [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften ermittelt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd670-106">The property methods of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="fd670-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="fd670-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fd670-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd670-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="fd670-109">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="fd670-109">**AccessMask**</span></span>
<span data-ttu-id="fd670-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd670-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd670-111">Enthält einen Satz von Flags, der Zugriffsberechtigungen für das-Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="fd670-111">Contains a set of flags that specifies access privileges for the object.</span></span> <span data-ttu-id="fd670-112">Gültige Werte für Active Directory-Objekte werden in der Enumeration der [**ADS- \_ Rechte \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum) Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="fd670-112">Valid values for Active Directory objects are defined in the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration.</span></span>

<span data-ttu-id="fd670-113">Weitere Informationen und eine Liste möglicher Werte für Datei-oder Dateifreigabe Objekte finden Sie unter [Datei Sicherheit und Zugriffsrechte](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="fd670-113">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="fd670-114">Weitere Informationen und eine Liste möglicher Werte für Registrierungs Objekte finden Sie unter [Sicherheit und Zugriffsrechte für den Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="fd670-114">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

<dt>

<span data-ttu-id="fd670-115">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd670-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd670-116">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="fd670-116">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AccessMask(
  [out] LONG* plnAccessMask
);
HRESULT put_AccessMask(
  [in] LONG lnAccessMask
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd670-117">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="fd670-117">**AceFlags**</span></span>
<span data-ttu-id="fd670-118"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd670-118"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd670-119">Enthält einen Satz von Flags, der angibt, ob andere Container oder Objekte den ACE erben können.</span><span class="sxs-lookup"><span data-stu-id="fd670-119">Contains a set of flags that specifies if other containers or objects can inherit the ACE.</span></span> <span data-ttu-id="fd670-120">Gültige Werte für Active Directory-Objekt werden in der Enumeration der [**ADS- \_ \_ aceflag**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) -Enumeration definiert.</span><span class="sxs-lookup"><span data-stu-id="fd670-120">Valid values for Active Directory object are defined in the [**ADS\_ACEFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) enumeration.</span></span>

<span data-ttu-id="fd670-121">Weitere Informationen und mögliche Werte für Datei-, Dateifreigabe-und Registrierungs Objekte finden Sie unter dem **AceFlags** -Member der [**ACE- \_ Header**](/windows/desktop/api/winnt/ns-winnt-ace_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="fd670-121">For more information and possible values for file, file share, and registry objects, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="fd670-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd670-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd670-123">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="fd670-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceFlags(
  [out] LONG* plnAceFlags
);
HRESULT put_AceFlags(
  [in] LONG lnAceFlags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd670-124">**AceType**</span><span class="sxs-lookup"><span data-stu-id="fd670-124">**AceType**</span></span>
<span data-ttu-id="fd670-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd670-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd670-126">Enthält einen Wert, der den Typ des ACE angibt.</span><span class="sxs-lookup"><span data-stu-id="fd670-126">Contains a value that indicates the type of ACE.</span></span> <span data-ttu-id="fd670-127">Gültige Werte für Active Directory-Objekte werden in der [**ADS \_ \_**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) -Enumeration des-Enumerationstyps definiert.</span><span class="sxs-lookup"><span data-stu-id="fd670-127">Valid values for Active Directory objects are defined in the [**ADS\_ACETYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) enumeration.</span></span>

<span data-ttu-id="fd670-128">Weitere Informationen und mögliche Werte für Datei-, Dateifreigabe-und Registrierungs Objekte finden Sie unter dem Element " **AceType** " der [**ACE- \_ Header**](/windows/desktop/api/winnt/ns-winnt-ace_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="fd670-128">For more information and possible values for file, file share, and registry objects, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

<dt>

<span data-ttu-id="fd670-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd670-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd670-130">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="fd670-130">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AceType(
  [out] LONG* plAceType
);
HRESULT put_AceType(
  [in] LONG lnAceType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd670-131">**Flags**</span><span class="sxs-lookup"><span data-stu-id="fd670-131">**Flags**</span></span>
<span data-ttu-id="fd670-132"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd670-132"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd670-133">Ein Flag, das angibt, ob der ACE einen Objekttyp oder vererbten Objekttyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="fd670-133">A flag that indicates if the ACE has an object type or inherited object type.</span></span> <span data-ttu-id="fd670-134">Gültige Flags werden in der AD-Flag- [**\_ \_ enumerationenumeration**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) definiert.</span><span class="sxs-lookup"><span data-stu-id="fd670-134">Valid flags are defined in the [**ADS\_FLAGTYPE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="fd670-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd670-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd670-136">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="fd670-136">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Flags(
  [out] LONG* lnflags
);
HRESULT put_Flags(
  [in] LONG lnflags
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd670-137">**Ereritedobjecttype**</span><span class="sxs-lookup"><span data-stu-id="fd670-137">**InheritedObjectType**</span></span>
<span data-ttu-id="fd670-138"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd670-138"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd670-139">Ein Flag, das den Typ eines untergeordneten Objekts eines ADSI-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="fd670-139">A flag that indicates the type of a child object of an ADSI object.</span></span> <span data-ttu-id="fd670-140">Der Wert ist eine **GUID** für ein Objekt im Zeichen folgen Format.</span><span class="sxs-lookup"><span data-stu-id="fd670-140">Its value is a **GUID** to an object in string format.</span></span> <span data-ttu-id="fd670-141">Wenn eine solche **GUID** festgelegt ist, gilt der ACE nur für das Objekt, auf das von der **GUID** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fd670-141">When such a **GUID** is set, the ACE applies only to the object referred to by the **GUID**.</span></span>

<dt>

<span data-ttu-id="fd670-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd670-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd670-143">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fd670-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_InheritedObjectType(
  [out] BSTR* bstrInheritedObjectType
);
HRESULT put_InheritedObjectType(
  [in] BSTR bstrInheritedObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd670-144">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="fd670-144">**ObjectType**</span></span>
<span data-ttu-id="fd670-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd670-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd670-146">Ein Flag, das den ADSI-Objekttyp angibt.</span><span class="sxs-lookup"><span data-stu-id="fd670-146">A flag that indicates the ADSI object type.</span></span> <span data-ttu-id="fd670-147">Der Wert ist eine **GUID** für eine Eigenschaft oder ein Objekt im Zeichen folgen Format.</span><span class="sxs-lookup"><span data-stu-id="fd670-147">Its value is a **GUID** to a property or an object in string format.</span></span> <span data-ttu-id="fd670-148">Die **GUID** bezieht sich auf eine Eigenschaft, wenn ADS mit der rechten DS- **\_ \_ \_ Lese \_** -und Werbe Zugriffs Maske für die **\_ Rechte \_ DS- \_ Schreib \_** Zugriff verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd670-148">The **GUID** refers to a property when **ADS\_RIGHT\_DS\_READ\_PROP** and **ADS\_RIGHT\_DS\_WRITE\_PROP** access masks are used.</span></span> <span data-ttu-id="fd670-149">Der **GUID** gibt ein Objekt an, wenn ADS, die von der **\_ rechten Seite \_ \_ \_** untergeordnet sind, untergeordnete und ADS rechts-untergeordneten Zugriffs Masken **\_ \_ \_ Löschen \_** verwenden</span><span class="sxs-lookup"><span data-stu-id="fd670-149">The **GUID** specifies an object when **ADS\_RIGHT\_DS\_CREATE\_CHILD** and **ADS\_RIGHT\_DS\_DELETE\_CHILD** access masks are used.</span></span>

<dt>

<span data-ttu-id="fd670-150">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd670-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd670-151">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fd670-151">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectType(
  [out] BSTR* bstrObjectType
);
HRESULT put_ObjectType(
  [in] BSTR bstrObjectType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="fd670-152">**Stiftungs**</span><span class="sxs-lookup"><span data-stu-id="fd670-152">**Trustee**</span></span>
<span data-ttu-id="fd670-153"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fd670-153"></dt> <dd> <dl></span></span>

<span data-ttu-id="fd670-154">Enthält den Namen des Kontos, für das der ACE gilt.</span><span class="sxs-lookup"><span data-stu-id="fd670-154">Contains the name of the account that the ACE applies to.</span></span>

<dt>

<span data-ttu-id="fd670-155">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fd670-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd670-156">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fd670-156">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Trustee(
  [out] BSTR* pbstrSecurityId
);
HRESULT put_Trustee(
  [in] BSTR bstrSecurityId
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="fd670-157">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd670-157">Examples</span></span>

<span data-ttu-id="fd670-158">Im folgenden Codebeispiel wird veranschaulicht, wie einer freigegebenen ACL mithilfe der [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Eigenschaften Methoden Einträge hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fd670-158">The following code example shows how to add entries to a discretionary ACL using the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property methods.</span></span>


```VB
Dim x As IADs
Dim sd As IADsSecurityDescriptor
Dim ace As IADsAccessControlEntry
Dim Dacl As IADsAccessControlList
Dim Ace1 As New AccessControlEntry
Dim Ace2 As New AccessControlEntry

On Error GoTo Cleanup
 
Set x = GetObject("LDAP://OU=Sales, DC=Fabrikam,DC=com")
Set sd = x.Get("ntSecurityDescriptor")
Set Dacl = sd.DiscretionaryAcl
 
' Show the existing ACEs.
For Each ace In Dacl
  Debug.Print ace.Trustee
Next
 
 
' Setup the first ACE.
Ace1.AccessMask = -1 'Full Permission (Allowed)
Ace1.AceType = ADS_ACETYPE_ACCESS_ALLOWED
Ace1.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace1.Trustee = "ACTIVED\Administrator"
 
' Setup the 2nd ACE.
Ace2.AccessMask = -1 'Full Permission (Denied)
Ace2.AceType = ADS_ACETYPE_ACCESS_DENIED
Ace2.AceFlags = ADS_ACEFLAG_INHERIT_ACE
Ace2.Trustee = "ACTIVED\Andyhar"
 
' Add the ACEs to the Discretionary ACL.
Dacl.AddAce Ace1
Dacl.AddAce Ace2
 
sd.DiscretionaryAcl = Dacl
x.Put "ntSecurityDescriptor", Array(sd)
x.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set x = Nothing
    Set sd = Nothing
    Set ace = Nothing
    Set Dacl = Nothing
    Set Ace1 = Nothing
    Set Ace2 = Nothing
    Set obj = Nothing
    Set cls = Nothing
```



<span data-ttu-id="fd670-159">Im folgenden Codebeispiel werden Zugriffs Steuerungs Einträge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd670-159">The following code example displays access-control entries.</span></span>


```C++
IADs *pADs = NULL;
IDispatch *pDisp = NULL;
IADsSecurityDescriptor *pSD = NULL;
VARIANT var;
HRESULT hr = S_OK;
 
VariantInit(&var);

hr = ADsOpenObject(L"LDAP://OU=Sales, DC=Fabrikam,DC=com",NULL,NULL,
                   ADS_SECURE_AUTHENTICATION, IID_IADs,(void**)&pADs);
if(FAILED(hr)) {goto Cleanup;}

hr = pADs->Get(CComBSTR("ntSecurityDescriptor"),&var);
if(FAILED(hr)) {goto Cleanup;}

pDisp = V_DISPATCH(&var);

hr = pDisp->QueryInterface(IID_IADsSecurityDescriptor,(void**)&pSD);
if(FAILED(hr)) {goto Cleanup;}
pDisp->Release();


pSD->get_DiscretionaryAcl(&pDisp);

hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
if(FAILED(hr)) {goto Cleanup;}

hr = DisplayAccessInfo(pSD);
if(FAILED(hr)) {goto Cleanup;}
VariantClear(&var);

Cleanup:
    if(pADs) pADs->Release();
    if(pDisp) pDisp->Release();
    if(pSD) pSD->Release();
    return hr;



HRESULT DisplayAccessInfo(IADsSecurityDescriptor *pSD)
{
    LPWSTR lpszFunction = L"DisplayAccessInfo";
    IDispatch *pDisp = NULL;
    IADsAccessControlList *pACL = NULL;
    IADsAccessControlEntry *pACE = NULL;
    IEnumVARIANT *pEnum = NULL;
    IUnknown *pUnk = NULL;
    HRESULT hr = S_OK;
    ULONG nFetch = 0;
    BSTR bstrValue = NULL;
    VARIANT var;
    LPWSTR lpszOutput = NULL;
    LPWSTR lpszMask = NULL;
    size_t nLength = 0;
    
    VariantInit(&var);
    
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if(FAILED(hr)){goto Cleanup;}
    hr = pDisp->QueryInterface(IID_IADsAccessControlList,(void**)&pACL);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pACL->get__NewEnum(&pUnk);
    if(FAILED(hr)){goto Cleanup;}
    
    hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
    
    if(FAILED(hr)){goto Cleanup;}
    hr = pEnum->Next(1,&var,&nFetch);
    
    while(hr == S_OK)
    {
        if(nFetch==1)
        {
            if(VT_DISPATCH != V_VT(&var))
            {
                goto Cleanup;
            }
            
            pDisp = V_DISPATCH(&var);
            hr = pDisp->QueryInterface(IID_IADsAccessControlEntry,(void**)&pACE);
            
            if(SUCCEEDED(hr))
            {
                lpszMask = L"Trustee: %s";
                hr = pACE->get_Trustee(&bstrValue);
                nLength = wcslen(lpszMask) + wcslen(bstrValue) + 1;
                lpszOutput = new WCHAR[nLength];
                swprintf_s(lpszOutput,lpszMask,bstrValue);
                printf(lpszOutput);
                delete [] lpszOutput;
                SysFreeString(bstrValue);
                
                pACE->Release();
                pACE = NULL;
                pDisp->Release();
                pDisp = NULL;
            }       
            
            VariantClear(&var);
        }       
        hr = pEnum->Next(1,&var,&nFetch);
    }
    
Cleanup:
    if(pDisp) pDisp->Release();
    if(pACL) pACL->Release();
    if(pACE) pACE->Release();
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(szValue) SysFreeString(szValue);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="fd670-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd670-160">Requirements</span></span>



| <span data-ttu-id="fd670-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd670-161">Requirement</span></span> | <span data-ttu-id="fd670-162">Wert</span><span class="sxs-lookup"><span data-stu-id="fd670-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd670-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd670-163">Minimum supported client</span></span><br/> | <span data-ttu-id="fd670-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd670-164">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="fd670-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd670-165">Minimum supported server</span></span><br/> | <span data-ttu-id="fd670-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd670-166">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fd670-167">Header</span><span class="sxs-lookup"><span data-stu-id="fd670-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd670-168"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd670-168"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="fd670-169">DLL</span><span class="sxs-lookup"><span data-stu-id="fd670-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd670-170"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd670-170"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="fd670-171">IID</span><span class="sxs-lookup"><span data-stu-id="fd670-171">IID</span></span><br/>                      | <span data-ttu-id="fd670-172">IID \_ IADsAccessControlEntry ist als B4F3A14C-9BDD-11D0-852C-00C04FD8D503 definiert.</span><span class="sxs-lookup"><span data-stu-id="fd670-172">IID\_IADsAccessControlEntry is defined as B4F3A14C-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd670-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd670-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd670-174">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="fd670-174">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="fd670-175">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="fd670-175">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[<span data-ttu-id="fd670-176">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fd670-176">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

