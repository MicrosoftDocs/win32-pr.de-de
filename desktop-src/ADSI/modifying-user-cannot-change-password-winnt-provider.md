---
title: Ändern des Benutzerkennworts kann nicht geändert werden (WinNT-Anbieter)
description: Erfahren Sie, wie Sie einem Benutzer die Berechtigung zum Ändern eines Kennworts für den WinNT-Anbieter verweigern. Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, kann gewährt oder verweigert werden.
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- Ändern des Benutzerkennworts kann nicht geändert werden (WinNT-Anbieter)
- Benutzer kann Kennwort nicht ändern (WinNT-Anbieter), ändern
- WinNT-Anbieter ADSI , Benutzerverwaltungsbeispiele,Benutzer kann Kennwort nicht ändern,Ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33510fa36285fa49a413b84d91e29f8d5a367622
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408093"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="a6547-107">Ändern des Benutzerkennworts kann nicht geändert werden (WinNT-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="a6547-107">Modifying User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="a6547-108">Die Fähigkeit eines Benutzers, sein eigenes Kennwort zu ändern, ist eine Berechtigung, die erteilt oder verweigert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6547-108">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="a6547-109">Um diese Berechtigung zu verweigern, fügen Sie das **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE-Flag** zur **userFlags-Eigenschaft** des Benutzerobjekts hinzu.</span><span class="sxs-lookup"><span data-stu-id="a6547-109">To deny this permission, add the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag to the **userFlags** property of the user object.</span></span> <span data-ttu-id="a6547-110">Um diese Berechtigung zu erteilen, entfernen Sie das **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE-Flag** aus der **userFlags-Eigenschaft** des Benutzerobjekts.</span><span class="sxs-lookup"><span data-stu-id="a6547-110">To grant this permission, remove the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag from the **userFlags** property of the user object.</span></span>

## <a name="example-code"></a><span data-ttu-id="a6547-111">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="a6547-111">Example Code</span></span>

<span data-ttu-id="a6547-112">Das folgende Codebeispiel zeigt, wie sie das **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE-Flag** der **userFlags-Eigenschaft** eines Benutzerobjekts ändern.</span><span class="sxs-lookup"><span data-stu-id="a6547-112">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Sub SetUserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String, fUserCannotChangePassword As Boolean)
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
    
    lUserFlags = oUser.Get("userFlags")
    
    If fUserCannotChangePassword Then
        lUserFlags = lUserFlags Or ADS_UF_PASSWD_CANT_CHANGE
    Else
        lUserFlags = lUserFlags And Not ADS_UF_PASSWD_CANT_CHANGE
    End If
    
    ' Modify the userFlags property.
    oUser.Put "userFlags", lUserFlags
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



<span data-ttu-id="a6547-113">Das folgende Codebeispiel zeigt, wie sie das **ADS \_ UF \_ PASSWD \_ CANT \_ CHANGE-Flag** der **userFlags-Eigenschaft** eines Benutzerobjekts ändern.</span><span class="sxs-lookup"><span data-stu-id="a6547-113">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```C++
//***************************************************************************
//  SetUserCannotChangePassword()
//***************************************************************************

HRESULT SetUserCannotChangePassword(LPCWSTR pwszDomain,
                                    LPCWSTR pwszUser, 
                                    LPCWSTR pwszUserCred, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    if(NULL == pwszDomain || 
        NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
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
        CComBSTR sbstrPropName = "userFlags";
        CComVariant svar;
        
        hr = pads->Get(sbstrPropName, &svar);
        if(SUCCEEDED(hr))
        {
            if(fCannotChangePassword)
            {
                svar.lVal |= ADS_UF_PASSWD_CANT_CHANGE;
            }
            else
            {
                svar.lVal &= ~ADS_UF_PASSWD_CANT_CHANGE;
            }

            // Perform the change.
            hr = pads->Put(sbstrPropName, svar);

            // Commit the change.
            hr = pads->SetInfo();
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




