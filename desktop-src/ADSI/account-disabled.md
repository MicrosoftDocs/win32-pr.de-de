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
# <a name="account-disabled-ldap-provider"></a><span data-ttu-id="2c63b-107">Konto deaktiviert (LDAP-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="2c63b-107">Account Disabled (LDAP Provider)</span></span>

<span data-ttu-id="2c63b-108">Wenn Sie ein Benutzerkonto deaktivieren möchten, legen Sie die accountdeaktiviert-Eigenschaft in der [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) -Schnittstelle auf **true** fest.</span><span class="sxs-lookup"><span data-stu-id="2c63b-108">To disable a user account, set the AccountDisabled property to **TRUE** in the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="2c63b-109">Dies ähnelt dem WinNT-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2c63b-109">This is similar to the WinNT provider.</span></span> <span data-ttu-id="2c63b-110">In den folgenden Codebeispielen wird veranschaulicht, wie Sie ein Benutzerkonto deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2c63b-110">The following code examples show how to disable a user account.</span></span>

## <a name="example-1"></a><span data-ttu-id="2c63b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c63b-111">Example 1</span></span>


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



## <a name="example-2"></a><span data-ttu-id="2c63b-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2c63b-112">Example 2</span></span>


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



 

 




