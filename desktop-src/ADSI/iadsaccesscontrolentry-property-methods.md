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
# <a name="iadsaccesscontrolentry-property-methods"></a>IADsAccessControlEntry-Eigenschaften Methoden

Mit den Eigenschafts Methoden der [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften ermittelt oder festgelegt. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**AccessMask**
</dt> <dd> <dl>

Enthält einen Satz von Flags, der Zugriffsberechtigungen für das-Objekt angibt. Gültige Werte für Active Directory-Objekte werden in der Enumeration der [**ADS- \_ Rechte \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum) Enumeration definiert.

Weitere Informationen und eine Liste möglicher Werte für Datei-oder Dateifreigabe Objekte finden Sie unter [Datei Sicherheit und Zugriffsrechte](/windows/desktop/FileIO/file-security-and-access-rights).

Weitere Informationen und eine Liste möglicher Werte für Registrierungs Objekte finden Sie unter [Sicherheit und Zugriffsrechte für den Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights).

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**AceFlags**
</dt> <dd> <dl>

Enthält einen Satz von Flags, der angibt, ob andere Container oder Objekte den ACE erben können. Gültige Werte für Active Directory-Objekt werden in der Enumeration der [**ADS- \_ \_ aceflag**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum) -Enumeration definiert.

Weitere Informationen und mögliche Werte für Datei-, Dateifreigabe-und Registrierungs Objekte finden Sie unter dem **AceFlags** -Member der [**ACE- \_ Header**](/windows/desktop/api/winnt/ns-winnt-ace_header) Struktur.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**AceType**
</dt> <dd> <dl>

Enthält einen Wert, der den Typ des ACE angibt. Gültige Werte für Active Directory-Objekte werden in der [**ADS \_ \_**](/windows/win32/api/iads/ne-iads-ads_acetype_enum) -Enumeration des-Enumerationstyps definiert.

Weitere Informationen und mögliche Werte für Datei-, Dateifreigabe-und Registrierungs Objekte finden Sie unter dem Element " **AceType** " der [**ACE- \_ Header**](/windows/desktop/api/winnt/ns-winnt-ace_header) Struktur.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Flags**
</dt> <dd> <dl>

Ein Flag, das angibt, ob der ACE einen Objekttyp oder vererbten Objekttyp aufweist. Gültige Flags werden in der AD-Flag- [**\_ \_ enumerationenumeration**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum) definiert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Ereritedobjecttype**
</dt> <dd> <dl>

Ein Flag, das den Typ eines untergeordneten Objekts eines ADSI-Objekts angibt. Der Wert ist eine **GUID** für ein Objekt im Zeichen folgen Format. Wenn eine solche **GUID** festgelegt ist, gilt der ACE nur für das Objekt, auf das von der **GUID** verwiesen wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

**ObjectType**
</dt> <dd> <dl>

Ein Flag, das den ADSI-Objekttyp angibt. Der Wert ist eine **GUID** für eine Eigenschaft oder ein Objekt im Zeichen folgen Format. Die **GUID** bezieht sich auf eine Eigenschaft, wenn ADS mit der rechten DS- **\_ \_ \_ Lese \_** -und Werbe Zugriffs Maske für die **\_ Rechte \_ DS- \_ Schreib \_** Zugriff verwendet werden. Der **GUID** gibt ein Objekt an, wenn ADS, die von der **\_ rechten Seite \_ \_ \_** untergeordnet sind, untergeordnete und ADS rechts-untergeordneten Zugriffs Masken **\_ \_ \_ Löschen \_** verwenden

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

**Stiftungs**
</dt> <dd> <dl>

Enthält den Namen des Kontos, für das der ACE gilt.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird veranschaulicht, wie einer freigegebenen ACL mithilfe der [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Eigenschaften Methoden Einträge hinzugefügt werden.


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



Im folgenden Codebeispiel werden Zugriffs Steuerungs Einträge angezeigt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                            |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsAccessControlEntry ist als B4F3A14C-9BDD-11D0-852C-00C04FD8D503 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> </dl>

 

