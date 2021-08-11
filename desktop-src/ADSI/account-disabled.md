---
title: Konto deaktiviert (LDAP-Anbieter)
description: Um ein Benutzerkonto zu deaktivieren, legen Sie die AccountDisabled-Eigenschaft in der IADsUser-Schnittstelle auf TRUE fest. Dies ähnelt dem WinNT-Anbieter. Die folgenden Codebeispiele zeigen, wie Sie ein Benutzerkonto deaktivieren.
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- Konto deaktiviert ADSI, LDAP-Anbieter
- LDAP-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Konto deaktiviert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf753da0770e19504d496be20ba350f79bd4788a797eb5241e68261df844b626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181444"
---
# <a name="account-disabled-ldap-provider"></a>Konto deaktiviert (LDAP-Anbieter)

Um ein Benutzerkonto zu deaktivieren, legen Sie die AccountDisabled-Eigenschaft in der [**IADsUser-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsuser) auf **TRUE** fest. Dies ähnelt dem WinNT-Anbieter. Die folgenden Codebeispiele zeigen, wie Sie ein Benutzerkonto deaktivieren.

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



 

 




