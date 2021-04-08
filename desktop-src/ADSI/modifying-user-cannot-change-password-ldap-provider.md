---
title: Ändern des Benutzers kann das Kennwort nicht ändern (LDAP-Anbieter)
description: Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann.
ms.assetid: 9d5c2d6a-9997-4d0c-b896-bf1b578e64ac
ms.tgt_platform: multiple
keywords:
- Ändern des Benutzers kann das Kennwort nicht ändern (LDAP-Anbieter) ADSI
- Der Benutzer kann das Kennwort (LDAP-Anbieter) ADSI nicht ändern, ändern
- LDAP-Anbieter ADSI, Benutzer Verwaltungs Beispiele, Benutzer muss Kennwort bei der nächsten Anmeldung ändern, ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1628b113c2f15278bc72e41aa79e4be03a98f2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730273"
---
# <a name="modifying-user-cannot-change-password-ldap-provider"></a>Ändern des Benutzers kann das Kennwort nicht ändern (LDAP-Anbieter)

Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann. Um diese Berechtigung zu verweigern, legen Sie zwei ACEs in der Sicherheits Beschreibung freigegebene Zugriffs Steuerungs Liste (DACL) des User-Objekts mit dem AD-Objekt-ACE-Typ " **\_ \_ Zugriff \_ verweigert \_** "-Objekt des Typs ADS fest. Ein ACE verweigert dem Benutzer die Berechtigung, und ein anderer ACE verweigert der Gruppe jeder die Berechtigung. Beide ACEs sind objektspezifische deny-ACEs, die die GUID der erweiterten Berechtigung zum Ändern von Kenn Wörtern angeben. Wenn Sie diese Berechtigung erteilen möchten, legen Sie die gleichen ACEs mit dem AD-Objekt-ACE-Typ für den Zugriff auf das **\_ \_ \_ \_ Objekt** "

Im folgenden Verfahren wird beschrieben, wie Sie ACEs für diese Berechtigung ändern oder hinzufügen.

**So können Sie die ACEs für diese Berechtigung ändern oder hinzufügen**

1.  Binden an das Benutzerobjekt.
2.  Rufen Sie das [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) -Objekt aus der **ntSecurityDescriptor** -Eigenschaft des User-Objekts ab.
3.  Rufen Sie die [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist) -Schnittstelle für die Sicherheits Beschreibung aus der [**IADsSecurityDescriptor. diskretionaryacl**](iadssecuritydescriptor-property-methods.md) -Eigenschaft ab.
4.  Zählen Sie die ACEs für das Objekt auf, und suchen Sie nach den ACEs mit der Änderungs Kennwort-GUID ({AB721A53-1E2F-11D0-9819-00AA0040529B}) für die [**IADsAccessControlEntry. ObjectType**](iadsaccesscontrolentry-property-methods.md) -Eigenschaft und "alle" oder "NT Authority \\ Self" für die **IADsAccessControlEntry. Treuhänder** -Eigenschaft.

    > [!Note]  
    > Die Zeichen folgen "jeder" und "NT Authority \\ Self" werden basierend auf der Sprache des ersten Domänen Controllers in der Domäne lokalisiert. Aus diesem Grund sollten die Zeichen folgen nicht direkt verwendet werden. Die Kontonamen sollten zur Laufzeit abgerufen werden, indem die [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) -Funktion mit der sid für "alle" ("s-1-1-0") und "NT Authority \\ Self" ("s-1-5-10") bekannte Sicherheits Prinzipale aufgerufen wird. Die Funktionen " **getsidaccountname**", " **getsidaccountname" " \_ jeder**" und " **getsidaccountname \_ Self** C++ example", die unter [Lesen von Benutzern nicht geändert werden können (LDAP-Anbieter)](reading-user-cannot-change-password-ldap-provider.md) veranschaulichen, wie dies zu tun ist.

     

5.  Ändern Sie die Eigenschaft [**IADsAccessControlEntry. AceType**](iadsaccesscontrolentry-property-methods.md) der ACEs, die gefunden wurde, um das **\_ Objekt AD AceType \_ Access \_ denied \_** zu finden, wenn der Benutzer sein Kennwort nicht ändern kann oder wenn der Benutzer sein Kennwort ändern kann. **\_ \_ \_ \_**
6.  Wenn der "jeder"-ACE nicht gefunden wird, erstellen Sie ein neues [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Objekt, das die in der folgenden Tabelle gezeigten Eigenschaftswerte enthält, und fügen Sie den neuen Eintrag der ACL mit der [**IADsAccessControlList. addace**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) -Methode hinzu.
7.  Wenn der ACE "NT Authority \\ Self" nicht gefunden wird, erstellen Sie ein neues [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Objekt mit denselben Eigenschafts Werten, die in der folgenden Tabelle angezeigt werden, mit dem Unterschied, dass die Eigenschaft " [**Treuhänder**](iadsaccesscontrolentry-property-methods.md) " den Kontonamen für die SID "S-1-5-10" ("NT Authority \\ Self") enthält. Fügen Sie der ACL den Eintrag mit der [**IADsAccessControlList. addace**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace) -Methode hinzu.
8.  Um die **ntSecurityDescriptor** -Eigenschaft des-Objekts zu aktualisieren, müssen Sie die [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) -Methode mit dem gleichen [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) -Objekt abrufen, das Sie in Schritt 2 abgerufen haben.
9.  Übertragen Sie die lokalen Änderungen an den Server mit der [**IADs. * tinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode.
10. Wenn eines der ACEs erstellt wurde, müssen Sie die ACL neu anordnen, damit die ACEs in der richtigen Reihenfolge sind. Um dies zu erreichen, müssen Sie die [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) -Funktion mit dem LDAP-ADsPath des-Objekts aufrufen und dann die [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) -Funktion mit der gleichen DACL. Diese Neuanordnung erfolgt automatisch, wenn die ACEs hinzugefügt werden.

In der folgenden Tabelle sind die [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Objekt Eigenschaftswerte aufgelistet.



| IADsAccessControlEntry (Eigenschaft)                                        | Wert                                                                                                                                                                 |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](iadsaccesscontrolentry-property-methods.md)          | **Anzeigen des Zugriffs auf die \_ \_ DS- \_ Steuerung \_**                                                                                                                                   |
| [**AceType**](iadsaccesscontrolentry-property-methods.md)             | **Anzeigen \_ Der Zugriff auf das \_ \_ \_ Objekt "AceType** " wurde verweigert, wenn der Benutzer sein Kennwort nicht ändern kann oder wenn der Benutzer sein Kennwort ändern kann. **\_ \_ \_ \_** |
| [**AceFlags**](iadsaccesscontrolentry-property-methods.md)            | 0                                                                                                                                                                     |
| [**Fahren**](iadsaccesscontrolentry-property-methods.md)               | **Anzeige \_ des \_ Objekt \_ Typs \_ "ADS"**                                                                                                                                  |
| [**ObjektType**](iadsaccesscontrolentry-property-methods.md)          | "{AB721A53-1E2F-11D0-9819-00AA0040529B}". Dies ist die GUID für die Änderung des Kennworts im Zeichen folgen Format.                                                                            |
| [**Ereritedobjecttype**](iadsaccesscontrolentry-property-methods.md) | Nicht verwendet                                                                                                                                                              |
| [**Stiftungs**](iadsaccesscontrolentry-property-methods.md)             | Der Kontoname für die SID "S-1-1-0" (alle).                                                                                                                            |



 

## <a name="example-code"></a>Beispielcode

Im folgenden Codebeispiel wird gezeigt, wie eine Schnittstelle zum Ändern einer DACL abgerufen wird. Die [**iadsobjectoptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) -Schnittstelle kann verwendet werden, indem die **ADS \_ Security \_ Info \_ DACL** -Option festgelegt wird.

> [!Note]  
> Wenn Sie den in diesem Beispiel dokumentierten Code verwenden möchten, müssen Sie ein Administrator sein. Wenn Sie kein Administrator sind, müssen Sie weiteren Code hinzufügen, der eine Schnittstelle verwendet, die es einem Benutzer ermöglicht, die Art und Weise zu ändern, in der der Client seitige Cache an den Active Directory-Domäne-Dienst zurückgesendet wird.

 


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



Im folgenden Codebeispiel wird veranschaulicht, wie die Berechtigung zum Ändern des Kennworts für den Benutzer mit dem LDAP-Anbieter geändert wird. In diesem Codebeispiel wird die oben definierte Funktion " **getobjectace** " verwendet.

In diesem Beispiel werden die Funktionen " **getsidaccountname \_** all" und " **getsidaccountname \_ Self** C++ example" verwendet, die unter [Lesen von Benutzer können Kennwort nicht ändern (LDAP-Anbieter)](reading-user-cannot-change-password-ldap-provider.md).


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



Im folgenden Codebeispiel wird veranschaulicht, wie die Berechtigung zum Ändern des Kennworts für den Benutzer mit dem LDAP-Anbieter geändert wird.

> [!Note]  
> Das folgende Beispiel funktioniert nur in Domänen, in denen die primäre Sprache Englisch ist, da die Zeichen folgen "jeder" und "NT Authority \\ Self" basierend auf der Sprache des ersten Domänen Controllers in der Domäne lokalisiert werden. Es gibt keine Visual Basic Möglichkeit, die Kontonamen für einen bekannten Sicherheits Prinzipal zu erhalten, ohne die [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) -Funktion aufrufen zu müssen. Wenn Sie Visual Basic verwenden, wird empfohlen, dass Sie den WinNT-Anbieter verwenden, um die Berechtigung "Kennwort für Benutzer kann nicht geändert werden" zu ändern, wie unter [Ändern des Kennworts](modifying-user-cannot-change-password-winnt-provider.md)für das Ändern von Benutzern

 


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



 

 