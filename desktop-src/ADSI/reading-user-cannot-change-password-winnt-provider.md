---
title: Lesebenutzer kann Kennwort nicht ändern (WinNT-Anbieter)
description: Erfahren Sie, wie Sie ermitteln, ob ein Benutzer über die Berechtigung zum Ändern eines Kennworts für den WinNT-Anbieter verfügt. Die Fähigkeit eines Benutzers, ein Kennwort zu ändern, kann gewährt oder verweigert werden.
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- Lesebenutzer kann Kennwort (WinNT-Anbieter) ADSI nicht ändern
- User Cannot Change Password (WinNT Provider) ADSI , reading
- WinNT-Anbieter ADSI, Benutzerverwaltungsbeispiele,User Cannot Change Password,reading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd075bfb6700779b60f9e578a4e89957487a2646
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405913"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>Lesebenutzer kann Kennwort nicht ändern (WinNT-Anbieter)

Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann. Lesen Sie das **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE-Flag** der **userFlags-Eigenschaft** des Benutzerobjekts, um zu ermitteln, ob dem Benutzer diese Berechtigung für den WinNT-Anbieter erteilt wurde. Das **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE-Flag** ist in der [**ADS USER FLAG \_ \_ \_ ENUM-Enumeration**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) definiert.

## <a name="example-code"></a>Beispielcode

Das folgende Codebeispiel zeigt, wie sie das **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE-Flag** der **userFlags-Eigenschaft** eines Benutzerobjekts abrufen.


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Function UserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    
    strPath = "WinNT://" + strDomain + "/" + strUser
    
    If "" <> strUserCred Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("WinNT:")
        Set oUser = dso.OpenDSObject(strPath, strUserCred, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strPath)
    End If
    
    If (oUser.Get("userFlags") And ADS_UF_PASSWD_CANT_CHANGE) <> 0 Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



Das folgende Codebeispiel zeigt, wie sie das **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE-Flag** der **userFlags-Eigenschaft** eines Benutzerobjekts abrufen.


```C++
//***************************************************************************
//
//  UserCannotChangePassword()
//
//***************************************************************************

HRESULT UserCannotChangePassword(LPCWSTR pwszDomain, 
                                 LPCWSTR pwszUser, 
                                 LPCWSTR pwszUserCred, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
{
    if(NULL == pwszDomain || NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    *pfCannotChangePassword = FALSE;

    HRESULT hr;
    IADs *pads;

    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszDomain;
    sbstrADsPath += "/";
    sbstrADsPath += pwszUser;

    hr = ADsOpenObject( sbstrADsPath,
                        pwszUserCred,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("userFlags"), &svar);
        if(SUCCEEDED(hr))
        {
            if(ADS_UF_PASSWD_CANT_CHANGE & svar.lVal)
            {
                *pfCannotChangePassword = TRUE;
            }
            else
            {
                *pfCannotChangePassword = FALSE;
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




