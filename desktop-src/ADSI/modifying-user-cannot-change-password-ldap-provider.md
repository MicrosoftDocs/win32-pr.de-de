---
title: Ändern des Benutzerkennworts kann nicht geändert werden (LDAP-Anbieter)
description: Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann.
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- Ändern von Benutzer kann Kennwort nicht ändern (LDAP-Anbieter) ADSI
- User Cannot Change Password (LDAP Provider) ADSI , modifying
- LDAP-Anbieter ADSI , Benutzerverwaltungsbeispiele, Benutzer muss Kennwort bei der nächsten Anmeldung ändern, Ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec664f9a79e0de4ff0b75ae31abd8dc1532cd17c0d3d35a934e094da45eb3383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179018"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a>Ändern des Benutzerkennworts kann nicht geändert werden (LDAP-Anbieter)

Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann. Um diese Berechtigung zu verweigern, legen Sie zwei ACEs in der DACL (Discretionary Access Control List) der Sicherheitsbeschreibung des Benutzerobjekts mit dem **ACE-Typ ADS \_ ACETYPE ACCESS \_ \_ DENIED \_ OBJECT** fest. Ein ACE verweigert dem Benutzer die Berechtigung, und ein anderer ACE verweigert die Berechtigung für die Gruppe Jeder. Beide ACEs sind objektspezifische Deny-ACEs, die die GUID der erweiterten Berechtigung zum Ändern von Kennwörtern angeben. Um diese Berechtigung zu erteilen, legen Sie die gleichen ACEs mit dem **ACE-Typ ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT** fest.

Im folgenden Verfahren wird beschrieben, wie AcEs für diese Berechtigung geändert oder hinzugefügt werden.

**So ändern oder fügen Sie die ACEs für diese Berechtigung hinzu**

1.  Binden sie an das Benutzerobjekt.
2.  Beziehen Sie [**das IADsSecurityDescriptor-Objekt**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) aus der **ntSecurityDescriptor-Eigenschaft** des Benutzerobjekts.
3.  Abrufen einer [**IADsAccessControlList-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) für den Sicherheitsdeskriptor aus der [**IADsSecurityDescriptor.DiscretionaryAcl-Eigenschaft.**](iadssecuritydescriptor-property-methods.md)
4.  Enumerieren Sie die ACEs für das Objekt, und suchen Sie nach den ACEs, die über die Änderungskennwort-GUID ({AB721A53-1E2F-11D0-9819-00AA0040529B}) für die [**IADsAccessControlEntry.ObjectType-Eigenschaft**](iadsaccesscontrolentry-property-methods.md) und "Everyone" oder "NT AUTHORITY SELF" für die \\ **IADsAccessControlEntry.Trustee-Eigenschaft** verfügen.

    > [!Note]  
    > Die Zeichenfolgen "Everyone" und "NT AUTHORITY SELF" werden basierend auf der Sprache des ersten \\ Domänencontrollers in der Domäne lokalisiert. Aus diesem Grund sollten die Zeichenfolgen nicht direkt verwendet werden. Die Kontonamen sollten zur Laufzeit durch Aufrufen der [**LookupAccountSid-Funktion**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) mit der SID für die bekannten Sicherheitsprinzipale "Everyone" ("S-1-1-0") und "NT AUTHORITY \\ SELF" ("S-1-5-10") ermittelt werden. Die **Beispielfunktionen GetSidAccountName,** **GetSidAccountName \_ Everyone** und **GetSidAccountName \_ Self** C++ unter Lesen von Benutzer kann Kennwort nicht ändern [(LDAP-Anbieter)](reading-user-cannot-change-password-ldap-provider.md) veranschaulichen dies.

     

5.  Ändern Sie die [**IADsAccessControlEntry.AceType-Eigenschaft**](iadsaccesscontrolentry-property-methods.md) der ACEs, die in **ADS \_ ACETYPE \_ ACCESS \_ DENIED \_ OBJECT** gefunden wurden, wenn der Benutzer sein Kennwort nicht ändern kann, oder **ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT,** wenn der Benutzer sein Kennwort ändern kann.
6.  Wenn der ACE "Everyone" nicht gefunden wird, erstellen Sie ein neues [**IADsAccessControlEntry-Objekt,**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) das die in der folgenden Tabelle gezeigten Eigenschaftswerte enthält, und fügen Sie den neuen Eintrag mit der [**IADsAccessControlList.AddAce-Methode**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) zur ACL hinzu.
7.  Wenn der ACE "NT AUTHORITY SELF" nicht gefunden wird, erstellen Sie ein neues IADsAccessControlEntry-Objekt mit den gleichen Eigenschaftswerten wie in der folgenden Tabelle, außer dass die Vertrauensinhaber-Eigenschaft den Kontonamen für \\ SID "S-1-5-10" ("NT AUTHORITY [](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) [](iadsaccesscontrolentry-property-methods.md) \\ SELF") enthält. Fügen Sie den Eintrag der ACL mit der [**IADsAccessControlList.AddAce-Methode**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) hinzu.
8.  Um die **ntSecurityDescriptor-Eigenschaft** des -Objekts zu aktualisieren, rufen Sie die [**IADs.Put-Methode**](/windows/desktop/api/Iads/nf-iads-iads-put) mit dem gleichen [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) auf, den Sie in Schritt 2 erhalten haben.
9.  Übertragen Sie die lokalen Änderungen mit der [**IADs.SetInfo-Methode auf den**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Server.
10. Wenn einer der ACEs erstellt wurde, müssen Sie die ACL neu anordnen, damit die ACEs in der richtigen Reihenfolge sind. Rufen Sie hierzu die [**GetNamedSecurityInfo-Funktion**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) mit dem LDAP-ADsPath des Objekts und dann die [**SetNamedSecurityInfo-Funktion**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) mit der gleichen DACL auf. Diese Neuanordnung erfolgt automatisch, wenn die ACEs hinzugefügt werden.

In der folgenden Tabelle sind die [**IADsAccessControlEntry-Objekteigenschaftswerte**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) aufgeführt.



| IADsAccessControlEntry-Eigenschaft                                        | Wert                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Accessmask**](iadsaccesscontrolentry-property-methods.md)          | **ADS \_ RIGHT \_ DS \_ CONTROL \_ ACCESS**                                                                                                                                   |
| [**AceType**](iadsaccesscontrolentry-property-methods.md)             | **ADS \_ ACETYPE \_ ACCESS \_ DENIED \_ OBJECT,** wenn der Benutzer sein Kennwort nicht ändern kann, oder **ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT,** wenn der Benutzer sein Kennwort ändern kann. |
| [**AceFlags**](iadsaccesscontrolentry-property-methods.md)            | 0                                                                                                                                                                     |
| [**Flaggen**](iadsaccesscontrolentry-property-methods.md)               | **\_ \_ ADS-FLAG-OBJEKTTYP \_ \_ VORHANDEN**                                                                                                                                  |
| [**ObjektType**](iadsaccesscontrolentry-property-methods.md)          | "{AB721A53-1E2F-11D0-9819-00AA0040529B}" ist die GUID zum Ändern des Kennworts in Zeichenfolgenform.                                                                            |
| [**Inheritedobjecttype**](iadsaccesscontrolentry-property-methods.md) | Nicht verwendet                                                                                                                                                              |
| [**Treuhänder**](iadsaccesscontrolentry-property-methods.md)             | Kontoname für SID "S-1-1-0" (Jeder).                                                                                                                            |



 

## <a name="example-code"></a>Beispielcode

Das folgende Codebeispiel zeigt, wie Sie eine Schnittstelle zum Ändern einer DACL abrufen. Die [**IADsObjectOptions-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) kann durch Festlegen der **\_ \_ \_ DACL-Option ADS SECURITY INFO verwendet** werden.

> [!Note]  
> Um den in diesem Beispiel dokumentierten Code verwenden zu können, müssen Sie Administrator sein. Wenn Sie kein Administrator sind, müssen Sie zusätzlichen Code hinzufügen, der eine Schnittstelle verwendet, die es einem Benutzer ermöglicht, die Art und Weise zu ändern, wie der clientseitige Cache zurück an den Active Directory-Domäne Service geleert wird.

 


```C++
//
// Obtain an IADsObjectOptions interface from the object whose
// DACL you wish to modify.
//
long CanReadSetDACL = ADS_SECURITY_INFO_DACL;

CComPtr<IADsObjectOptions> spObjOps;

hr = pads->QueryInterface(IID_IADsObjectOptions, (void**)&spObjOps);

if(SUCCEEDED(hr))

{

//
// Set the option mask you want to change. In this case
// we want to change the objects security information, so we'll
// use the ADS_OPTION_SECURITY_MASK. Since we want to modify the 
// DACL, we'll set the variant to ADS_SEDCURITY_INFO_DACL flag. 
//

    CComVariant svar;
    svar = CanReadSetDACL;
    hr = spObjOps->SetOption(ADS_OPTION_SECURITY_MASK, svar); 

}
//
// The smart pointer declared for pObjOptions can be released
// or it will be destroyed and released once the pointer goes 
// out of scope.
//

```



Das folgende Codebeispiel zeigt, wie Sie die Berechtigung "Benutzer kann Kennwort nicht ändern" mithilfe des LDAP-Anbieters ändern. In diesem Codebeispiel wird die **oben definierte Hilfsprogrammfunktion GetObjectACE** verwendet.

In diesem Beispiel werden die C++-Beispielfunktionen **GetSidAccountName \_ Everyone** und **GetSidAccountName \_ Self** C++ verwendet, die unter Lesen von Benutzer kann Kennwort nicht ändern [(LDAP-Anbieter) gezeigt werden.](reading-user-cannot-change-password-ldap-provider.md)


```C++
#include <aclapi.h>

#define CHANGE_PASSWORD_GUID_W L"{AB721A53-1E2F-11D0-9819-00AA0040529B}"

/***************************************************************************

    CreateACE()

    Creates an ACE and returns the IDispatch pointer for the ACE. This 
    pointer can be passed directly to IADsAccessControlList::AddAce.

    bstrTrustee - Contains the Trustee for the ACE.

    bstrObjectType - Contains the ObjectType for the ACE.

    lAccessMask - Contains the AccessMask for the ACE.

    lACEType - Contains the ACEType for the ACE.

    lACEFlags - Contains the ACEFlags for the ACE.

    lFlags - Contains the Flags for the ACE.

***************************************************************************/

IDispatch* CreateACE(BSTR bstrTrustee, 
                     BSTR bstrObjectType, 
                     long lAccessMask, 
                     long lACEType, 
                     long lACEFlags, 
                     long lFlags)
{
    HRESULT hr;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE = NULL;

    hr = CoCreateInstance(CLSID_AccessControlEntry,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsAccessControlEntry,
                          (void**)&pACE);
    if(SUCCEEDED(hr)) 
    {
        hr = pACE->put_Trustee(bstrTrustee); 
        hr = pACE->put_ObjectType(bstrObjectType);
        hr = pACE->put_AccessMask(lAccessMask); 
        hr = pACE->put_AceType(lACEType);
        hr = pACE->put_AceFlags(lACEFlags);
        hr = pACE->put_Flags(lFlags);

        hr = pACE->QueryInterface(IID_IDispatch, (LPVOID*)&pDisp);

        pACE->Release();
    }

    return pDisp;
}

/***************************************************************************

    ReorderACEs()

    Causes the ACEs of an object DACL to be reordered properly. The ACEs are 
    automatically put in the proper order when they are added to the DACL. 
    On older systems however, this does not occur automatically, so this 
    function is necessary so the deny ACEs are ordered in the list before 
    the allow ACEs.

    pwszDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the DS object to reorder the DACL for.

***************************************************************************/

HRESULT ReorderACEs(LPCWSTR pwszDN)
{
    HRESULT hr = E_FAIL;
    DWORD dwResult;
    ACL *pdacl;
    PSECURITY_DESCRIPTOR psd;
    
    dwResult = GetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                        SE_DS_OBJECT_ALL,
                                        DACL_SECURITY_INFORMATION,
                                        NULL,
                                        NULL,
                                        &pdacl,
                                        NULL,
                                        &psd);

    if(ERROR_SUCCESS == dwResult)
    {
        dwResult = SetNamedSecurityInfoW(   (LPWSTR)pwszDN,
                                            SE_DS_OBJECT_ALL,
                                            DACL_SECURITY_INFORMATION,
                                            NULL,
                                            NULL,
                                            pdacl,
                                            NULL);

        LocalFree(psd);
        
        if(ERROR_SUCCESS == dwResult)
        {
            hr = S_OK;
        }
    }
    
    return hr;
}

/***************************************************************************

    SetUserCannotChangePassword()

    Sets the "User Cannot Change Password" permission using the LDAP provider 
    to the specified setting. To do this, find the existing 
    ACEs and modify the AceType. If the ACE is not found, a new one of the 
    proper type is created and added. The ACEs should always be present, but 
    it is possible that the default DACL excludes them, so this situation 
    will be handled correctly.

    pwszUserDN - A null-terminated Unicode string that contains the LDAP 
    ADsPath of the user object to modify.

    pwszUsername - A null-terminated Unicode string that contains the user 
    name to use for authorization. If this is NULL, the credentials of the 
    current user are used.

    pwszPassword - A null-terminated Unicode string that contains the 
    password to use for authorization. This is ignored if pwszUsername is 
    NULL.

    fCannotChangePassword - Contains the new setting for the privilege. 
    Contains nonzero if the user cannot change their password or zero if 
    the can change their password.

***************************************************************************/

HRESULT SetUserCannotChangePassword(LPCWSTR pwszUserDN, 
                                    LPCWSTR pwszUsername, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    HRESULT hr;

    CComBSTR sbstrEveryone;
    hr = GetSidAccountName_Everyone(&sbstrEveryone);
    if(FAILED(hr))
    {
        return hr;
    }

    CComBSTR sbstrSelf;
    hr = GetSidAccountName_Self(&sbstrSelf);
    if(FAILED(hr))
    {
        return hr;
    }

    if(NULL == pwszUserDN)
    {
        return E_INVALIDARG;
    }
    
    IADs *pads;

    hr = ADsOpenObject( pwszUserDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrSecDesc = "ntSecurityDescriptor";
        CComVariant svar;
        
        hr = pads->Get(sbstrSecDesc, &svar);
        if(SUCCEEDED(hr))
        {
            IADsSecurityDescriptor *psd;

            hr = svar.pdispVal->QueryInterface(IID_IADsSecurityDescriptor, (LPVOID*)&psd);
            if(SUCCEEDED(hr))
            {
                IDispatch *pDisp;

                hr = psd->get_DiscretionaryAcl(&pDisp);
                if(SUCCEEDED(hr))
                {
                    IADsAccessControlList *pACL;

                    hr = pDisp->QueryInterface(IID_IADsAccessControlList, (void**)&pACL);
                    if(SUCCEEDED(hr)) 
                    {
                        BOOL fMustReorder = FALSE;
                        /*
                        Get the existing ACE for the change password permission 
                        for Everyone. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACEEveryone = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrEveryone, &pACEEveryone);
                        if(pACEEveryone)
                        {
                            hr = pACEEveryone->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);

                            pACEEveryone->Release();
                        }
                        else
                        {
                            IDispatch *pDispEveryone = NULL;
                            
                            pDispEveryone = CreateACE(sbstrEveryone, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);
                            
                            if(pDispEveryone)
                            {
                                //add the new ACE for everyone
                                hr = pACL->AddAce(pDispEveryone);

                                pDispEveryone->Release();

                                fMustReorder = TRUE;
                            }                            
                        }
                        
                        /*
                        Get the existing ACE for the change password permission 
                        for Self. If it exists, just modify the existing 
                        ACE. If it does not exist, create a new one and add it 
                        to the ACL.
                        */
                        IADsAccessControlEntry *pACESelf = NULL;
                        hr = GetObjectACE(pACL, CHANGE_PASSWORD_GUID_W, sbstrSelf, &pACESelf);
                        if(pACESelf)
                        {
                            hr = pACESelf->put_AceType(fCannotChangePassword ? 
                                ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                ADS_ACETYPE_ACCESS_ALLOWED_OBJECT);
                        
                            pACESelf->Release();
                        }
                        else
                        {
                            IDispatch *pDispSelf = NULL;
                            
                            pDispSelf = CreateACE(sbstrSelf, 
                                CComBSTR(CHANGE_PASSWORD_GUID_W),
                                ADS_RIGHT_DS_CONTROL_ACCESS, 
                                fCannotChangePassword ? 
                                    ADS_ACETYPE_ACCESS_DENIED_OBJECT : 
                                    ADS_ACETYPE_ACCESS_ALLOWED_OBJECT, 
                                0,
                                ADS_FLAG_OBJECT_TYPE_PRESENT);

                            if(pDispSelf)
                            {
                                //add the new ACE for self
                                hr = pACL->AddAce(pDispSelf);

                                pDispSelf->Release();

                                fMustReorder = TRUE;
                            }                            
                        }

                        //update the security descriptor property
                        hr = pads->Put(sbstrSecDesc, svar);
                        
                        //commit the changes
                        hr = pads->SetInfo();

                        if(fMustReorder)
                        {
                            ReorderACEs(pwszUserDN);
                        }

                        pACL->Release();
                    }

                    pDisp->Release();
                }
                
                psd->Release();
            }
        }
    }

    return hr;
}
```



Das folgende Codebeispiel zeigt, wie Sie die Berechtigung "Benutzer kann Kennwort nicht ändern" mithilfe des LDAP-Anbieters ändern.

> [!Note]  
> Das folgende Beispiel funktioniert nur in Domänen, in denen die primäre Sprache Englisch ist, da die Zeichenfolgen "Everyone" und "NT AUTHORITY SELF" basierend auf der Sprache des ersten Domänencontrollers in der Domäne lokalisiert \\ werden. Es gibt keine Möglichkeit, Visual Basic Kontonamen für einen bekannten Sicherheitsprinzipal ohne Aufrufen der [**LookupAccountSid-Funktion zu**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) erhalten. Wenn Sie Visual Basic verwenden, wird empfohlen, den WinNT-Anbieter zu verwenden, um die Berechtigung "Benutzer kann Kennwort nicht ändern" zu ändern, wie unter Ändern des Kennworts vom Benutzer kann kein Kennwort geändert [werden (WinNT-Anbieter) gezeigt.](modifying-user-cannot-change-password-winnt-provider.md)

 


```VB
'******************************************************************************
'
'    SetUserCannotChangePassword
'
'    Sets the "User Cannot Change Password" permission using the LDAP provider
'    to the specified setting. This is accomplished by finding the existing
'    ACEs and modifying the AceType. The ACEs should always be present, but
'    it is possible that the default DACL excludes them. This function will not
'    work correctly if both ACEs are not present.
'
'    strUserDN - A string that contains the LDAP ADsPath of the user object to
'    modify.
'
'    strUsername - A string that contains the user name to use for
'    authorization. If this is an empty string, the credentials of the current
'    user are used.
'
'    strPassword - A string that contains the password to use for authorization.
'    This is ignored if strUsername is empty.
'
'    fCannotChangePassword - Contains the new setting for the privilege.
'    Contains True if the user cannot change their password or False if
'    the can change their password.
'
'******************************************************************************
Sub SetUserCannotChangePassword(strUserDN As String, strUsername As String, strPassword As String, fUserCannotChangePassword As Boolean)
    Dim oUser As IADs
    Dim oSecDesc As IADsSecurityDescriptor
    Dim oACL As IADsAccessControlList
    Dim oACE As IADsAccessControlEntry
    
    fEveryone = False
    fSelf = False
    
    If "" <> strUsername Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oUser = dso.OpenDSObject(strUserDN, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strUserDN)
    End If
    
    Set oSecDesc = oUser.Get("ntSecurityDescriptor")
    Set oACL = oSecDesc.DiscretionaryAcl
    
    ' Modify the existing entries.
    For Each oACE In oACL
        If UCase(oACE.ObjectType) = UCase(CHANGE_PASSWORD_GUID) Then
            If oACE.Trustee = "Everyone" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        
            If oACE.Trustee = "NT AUTHORITY\SELF" Then
                ' Modify the ace type of the entry.
                If fUserCannotChangePassword Then
                    oACE.AceType = ADS_ACETYPE_ACCESS_DENIED_OBJECT
                Else
                    oACE.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT
                End If
            End If
        End If
    Next
    
    ' Update the ntSecurityDescriptor property.
    oUser.Put "ntSecurityDescriptor", oSecDesc
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



 

 