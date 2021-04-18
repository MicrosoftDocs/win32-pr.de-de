---
title: Konto deaktiviert (LDAP-Anbieter)
description: Wenn Sie ein Benutzerkonto deaktivieren möchten, legen Sie die accountdeaktiviert-Eigenschaft in der IADsUser-Schnittstelle auf true fest. Dies ähnelt dem WinNT-Anbieter. In den folgenden Codebeispielen wird veranschaulicht, wie Sie ein Benutzerkonto deaktivieren.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Konto deaktiviert ADSI, LDAP-Anbieter
- LDAP-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Konto deaktiviert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61fb65a06f4e2afb1b43595b955c577b2a6090
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106354972"
---
# <a name="account-disabled-ldap-provider"></a>Konto deaktiviert (LDAP-Anbieter)

Wenn Sie ein Benutzerkonto deaktivieren möchten, legen Sie die accountdeaktiviert-Eigenschaft in der [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) -Schnittstelle auf **true** fest. Dies ähnelt dem WinNT-Anbieter. In den folgenden Codebeispielen wird veranschaulicht, wie Sie ein Benutzerkonto deaktivieren.

## <a name="example-1"></a>Beispiel 1


```VB
Dim usr As IADsUser
On Error GoTo Cleanup

Set usr = GetObject("LDAP:// CN=JeffSmith, OU=Sales, DC=Fabrikam, DC=Com")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



## <a name="example-2"></a>Beispiel 2


```C++
IADsUser *pUser = NULL;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"LDAP://serv1/cn=Jeff Smith,cn=Users, dc=Fabrikam, dc=com";
hr = ADsGetObject(adsPath,IID_IADsUser,(void**)&pUser);

if(FAILED(hr)){return;}

hr = pUser->put_AccountDisabled(true);
hr = pUser->SetInfo();
```



 

 




