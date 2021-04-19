---
title: Kennwort läuft nie ab (WinNT-Anbieter)
description: Wenn Sie diese Option mit dem WinNT ADSI-Anbieter aktivieren möchten, legen Sie das Flag für die ADS-Berechtigung "nicht \_ \_ ablaufen" \_ \_ passwd (0x10000) für das UserFlags-Attribut fest. Hinweis für Windows 2000 und höher verwenden Sie den LDAP ADSI-Anbieter für Benutzer Verwaltungsvorgänge, wie hier gezeigt.
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- Kennwort läuft nie ab (WinNT-Anbieter)
- Kennwort läuft nie ab ADSI, WinNT-Anbieter
- WinNT-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Kennwort läuft nie ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106371873"
---
# <a name="password-never-expires-winnt-provider"></a><span data-ttu-id="e5a69-106">Kennwort läuft nie ab (WinNT-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="e5a69-106">Password Never Expires (WinNT Provider)</span></span>

<span data-ttu-id="e5a69-107">Wenn Sie diese Option mit dem WinNT ADSI-Anbieter aktivieren möchten, legen Sie das Flag für die ADS-Berechtigung "nicht **\_ ablaufen" \_ \_ \_ passwd** (0x10000) für das **UserFlags** -Attribut fest.</span><span class="sxs-lookup"><span data-stu-id="e5a69-107">To enable this option using the WinNT ADSI provider, set the **ADS\_UF\_DONT\_EXPIRE\_PASSWD** (0x10000) flag on the **UserFlags** attribute.</span></span>

> [!Note]  
> <span data-ttu-id="e5a69-108">Verwenden Sie für Windows 2000 und höher den LDAP ADSI-Anbieter für Benutzer Verwaltungsvorgänge, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e5a69-108">For Windows 2000 and later, use the LDAP ADSI provider for user management operations as shown.</span></span> <span data-ttu-id="e5a69-109">Weitere Informationen finden Sie unter [Kennwort läuft nie ab (LDAP-Anbieter)](password-never-expires.md).</span><span class="sxs-lookup"><span data-stu-id="e5a69-109">For more information, see [Password Never Expires (LDAP Provider)](password-never-expires.md).</span></span>

 

## <a name="example-1"></a><span data-ttu-id="e5a69-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5a69-110">Example 1</span></span>

<span data-ttu-id="e5a69-111">Im folgenden Codebeispiel wird gezeigt, wie die Option Kennwort läuft nie ab mithilfe von Visual Basic mit ADSI festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e5a69-111">The following code example shows how to set the password never expires option using Visual Basic with ADSI.</span></span>


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="e5a69-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5a69-112">Example 2</span></span>

<span data-ttu-id="e5a69-113">Im folgenden Codebeispiel wird gezeigt, wie die Option Kennwort läuft nie ab mithilfe von C++ mit ADSI festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e5a69-113">The following code example shows how to set the password never expires option using C++ with ADSI.</span></span>


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




