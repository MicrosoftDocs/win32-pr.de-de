---
title: Benutzer muss das Kennwort bei der nächsten Anmeldung ändern (WinNT-Anbieter)
description: Um diese Option zu aktivieren, legen Sie das passwordexpired-Attribut des Benutzers auf eins (1) fest. Wenn dieses Attribut auf NULL (0) festgelegt wird, kann sich der Benutzer anmelden, ohne das Kennwort zu ändern.
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- Benutzer muss das Kennwort bei der nächsten Anmeldung (WinNT-Anbieter) ADSI ändern
- Benutzer muss das Kennwort bei der nächsten Anmeldung ändern ADSI, WinNT Provider
- WinNT-Anbieter ADSI, Benutzer Verwaltungs Beispiele, Benutzer muss Kennwort bei der nächsten Anmeldung ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787be5f5f4e1534574a68c179bb699ac68c61e3e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106370393"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a><span data-ttu-id="9259a-107">Benutzer muss das Kennwort bei der nächsten Anmeldung ändern (WinNT-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="9259a-107">User Must Change Password at Next Logon (WinNT Provider)</span></span>

<span data-ttu-id="9259a-108">Um diese Option zu aktivieren, legen Sie das **passwordexpired** -Attribut des Benutzers auf eins (1) fest.</span><span class="sxs-lookup"><span data-stu-id="9259a-108">To enable this option, set the **PasswordExpired** attribute of the user to one (1).</span></span> <span data-ttu-id="9259a-109">Wenn dieses Attribut auf NULL (0) festgelegt wird, kann sich der Benutzer anmelden, ohne das Kennwort zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9259a-109">Setting this attribute to zero (0) enables the user to log on without changing the password.</span></span>

## <a name="example-1"></a><span data-ttu-id="9259a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9259a-110">Example 1</span></span>

<span data-ttu-id="9259a-111">Im folgenden Codebeispiel wird gezeigt, wie die Option Kennwort bei der nächsten Anmeldung ändern mithilfe von Visual Basic mit ADSI festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9259a-111">The following code example shows how to set the change password on next logon option using Visual Basic with ADSI.</span></span>


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="9259a-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9259a-112">Example 2</span></span>

<span data-ttu-id="9259a-113">Im folgenden Codebeispiel wird gezeigt, wie die Option Kennwort bei der nächsten Anmeldung ändern mithilfe von C++ mit ADSI festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9259a-113">The following code example shows how to set the change password on next logon option using C++ with ADSI.</span></span>


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




