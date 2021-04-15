---
title: Konto deaktiviert (WinNT-Anbieter)
description: Wenn Sie den WinNT-Anbieter verwenden, kann ein Konto mithilfe der IADsUser. accountdeaktiviert-Eigenschaft aktiviert oder deaktiviert werden.
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- Konto deaktiviert (WinNT-Anbieter)
- Konto deaktiviert ADSI, WinNT-Anbieter
- WinNT-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Konto deaktiviert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99b1fe45b71eda14547703f8721b2a13d581b8e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104394034"
---
# <a name="account-disabled-winnt-provider"></a><span data-ttu-id="c0779-106">Konto deaktiviert (WinNT-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="c0779-106">Account Disabled (WinNT Provider)</span></span>

<span data-ttu-id="c0779-107">Wenn Sie den WinNT-Anbieter verwenden, kann ein Konto mithilfe der [**IADsUser. accountdeaktiviert**](iadsuser-property-methods.md) -Eigenschaft aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c0779-107">When using the WinNT provider, an account can be enabled or disabled using the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0779-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0779-108">Example 1</span></span>

<span data-ttu-id="c0779-109">Im folgenden Codebeispiel wird gezeigt, wie Sie ein Konto mit Visual Basic mit ADSI deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0779-109">The following code example shows how to disable an account using Visual Basic with ADSI.</span></span>


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a><span data-ttu-id="c0779-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c0779-110">Example 2</span></span>

<span data-ttu-id="c0779-111">Im folgenden Codebeispiel wird gezeigt, wie Sie ein Konto mit C++ mit ADSI deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0779-111">The following code example shows how to disable an account using C++ with ADSI.</span></span>


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




