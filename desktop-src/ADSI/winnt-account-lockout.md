---
title: Kontosperrung (WinNT-Anbieter)
description: Wenn die Anzahl der fehlgeschlagenen Anmeldeversuche überschritten wird, wird das Benutzerkonto für die im LockoutDuration-Attribut angegebene Anzahl von Minuten gesperrt.
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- Konto Sperre ADSI, WinNT-Anbieter
- WinNT-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Kontosperrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337873"
---
# <a name="account-lockout-winnt-provider"></a><span data-ttu-id="fea43-105">Kontosperrung (WinNT-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="fea43-105">Account Lockout (WinNT Provider)</span></span>

<span data-ttu-id="fea43-106">Wenn die Anzahl der fehlgeschlagenen Anmeldeversuche überschritten wird, wird das Benutzerkonto für die im [**LockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) -Attribut angegebene Anzahl von Minuten gesperrt.</span><span class="sxs-lookup"><span data-stu-id="fea43-106">When the number of failed logon attempts is exceeded, the user account becomes locked out for the number of minutes specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="fea43-107">Die Eigenschaft " [**IADsUser. isaccountlocked**](iadsuser-property-methods.md) " scheint die Eigenschaft zu sein, die zum Lesen und Ändern des Sperr Zustands eines Benutzerkontos verwendet werden soll, aber der WinNT ADSI-Anbieter weist Einschränkungen auf, die die Verwendung der Eigenschaft " **isaccountlocked** " einschränken.</span><span class="sxs-lookup"><span data-stu-id="fea43-107">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the WinNT ADSI provider has restrictions that limit the use of the **IsAccountLocked** property.</span></span>

## <a name="resetting-the-account-lockout-status"></a><span data-ttu-id="fea43-108">Zurücksetzen des Konto Sperr Status</span><span class="sxs-lookup"><span data-stu-id="fea43-108">Resetting the Account Lockout Status</span></span>

<span data-ttu-id="fea43-109">Bei Verwendung des WinNT-Anbieters kann die [**isaccountlocked**](iadsuser-property-methods.md) -Eigenschaft nur auf **false** festgelegt werden, wodurch das Konto entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="fea43-109">When using the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can only be set to **FALSE**, which unlocks the account.</span></span> <span data-ttu-id="fea43-110">Der Versuch, die **isaccountlocked** -Eigenschaft auf **true** festzulegen, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="fea43-110">Attempting to set the **IsAccountLocked** property to **TRUE** will fail.</span></span> <span data-ttu-id="fea43-111">Nur das System kann ein Konto sperren.</span><span class="sxs-lookup"><span data-stu-id="fea43-111">Only the system can lock an account.</span></span>

<span data-ttu-id="fea43-112">Im folgenden Codebeispiel wird veranschaulicht, wie Visual Basic mit ADSI verwendet wird, um ein Benutzerkonto zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="fea43-112">The following code example demonstrates how to use Visual Basic with ADSI to unlock a user account.</span></span>


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



<span data-ttu-id="fea43-113">Im folgenden Codebeispiel wird veranschaulicht, wie C++ mit ADSI verwendet wird, um ein Benutzerkonto zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="fea43-113">The following code example demonstrates how to use C++ with ADSI to unlock a user account.</span></span>


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a><span data-ttu-id="fea43-114">Lesen des Konto Sperr Status</span><span class="sxs-lookup"><span data-stu-id="fea43-114">Reading the Account Lockout Status</span></span>

<span data-ttu-id="fea43-115">Mit dem WinNT-Anbieter kann mithilfe der [**isaccountlocked**](iadsuser-property-methods.md) -Eigenschaft bestimmt werden, ob ein Konto gesperrt ist. Wenn ein Konto gesperrt ist, enthält die Eigenschaft " **isaccountlocked** " den Wert " **true**".</span><span class="sxs-lookup"><span data-stu-id="fea43-115">With the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can be used to determine if an account is locked out. If an account is locked out, the **IsAccountLocked** property will contain **TRUE**.</span></span> <span data-ttu-id="fea43-116">Wenn ein Konto nicht gesperrt ist, enthält die Eigenschaft **isaccountlocked** den Wert **false**.</span><span class="sxs-lookup"><span data-stu-id="fea43-116">If an account is not locked out, the **IsAccountLocked** property will contain **FALSE**.</span></span>

<span data-ttu-id="fea43-117">Im folgenden Codebeispiel wird veranschaulicht, wie Visual Basic mit ADSI verwendet wird, um zu bestimmen, ob ein Konto gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="fea43-117">The following code example demonstrates how to use Visual Basic with ADSI to determine if an account is locked out.</span></span>


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



<span data-ttu-id="fea43-118">Im folgenden Codebeispiel wird veranschaulicht, wie C++ mit ADSI verwendet wird, um zu bestimmen, ob ein Konto gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="fea43-118">The following code example demonstrates how to use C++ with ADSI to determine if an account is locked out.</span></span>


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 