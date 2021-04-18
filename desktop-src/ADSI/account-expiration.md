---
title: Konto Ablauf (LDAP-Anbieter)
description: Um das Ablaufdatum des Kontos festzulegen, legen Sie die IADsUser. AccountExpirationDate-Eigenschaft auf den gewünschten Datumswert fest.
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- Konto Ablauf ADSI, LDAP-Anbieter
- LDAP-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Konto Ablauf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03ea33d8d5abb219c2b562aa05058b5dec45919
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106337253"
---
# <a name="account-expiration-ldap-provider"></a><span data-ttu-id="68d0d-105">Konto Ablauf (LDAP-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="68d0d-105">Account Expiration (LDAP Provider)</span></span>

<span data-ttu-id="68d0d-106">Um das Ablaufdatum des Kontos festzulegen, legen Sie die [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) -Eigenschaft auf den gewünschten Datumswert fest.</span><span class="sxs-lookup"><span data-stu-id="68d0d-106">To set the account expiration date, set the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property to the desired date value.</span></span> <span data-ttu-id="68d0d-107">Um das Ablaufdatum des Kontos zu deaktivieren, legen Sie das [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires) -Attribut auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="68d0d-107">To disable the account expiration date, set the [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute to zero.</span></span> <span data-ttu-id="68d0d-108">In den folgenden Codebeispielen wird gezeigt, wie das Ablaufdatum festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="68d0d-108">The following code examples show how to set the expiration date.</span></span>


```VB
Public Sub SetUserAccountExpirationDate(User As IADsUser, ExpirationDate As Date)
    If 0 = ExpirationDate Then
        ' Disable the account expiration date.
        User.Put "accountExpires", 0
    Else
        ' Set the new account expiration date.
        User.AccountExpirationDate = ExpirationDate
    End If
    
    User.SetInfo
 
End Sub
```




```C++
/***************************************************************************

    SetUserAccountExpirationDate()

***************************************************************************/

HRESULT SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
    if(!pUser) 
    {
        return E_INVALIDARG;
    }

    HRESULT hr;

    if(!date || date < 0) 
    {
        // Account never expires. Set the accountExpires attribute to zero.
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        
        hr = pUser->Put(CComBSTR("accountExpires"), var); 

        VariantClear(&var);
    }
    else 
    {
        // Account expires on date.
        hr = pUser->put_AccountExpirationDate(date); 
    }

    if(S_OK == hr)
    {
        hr = pUser->SetInfo();
    }

    return hr;
}
```



> [!Note]  
> <span data-ttu-id="68d0d-109">Das [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires) -Attribut enthält das Ablaufdatum des Kontos.</span><span class="sxs-lookup"><span data-stu-id="68d0d-109">The [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) attribute contains the account expire date.</span></span> <span data-ttu-id="68d0d-110">Das MMC-Snap-in "Active Directory-Benutzer und-Computer" zeigt das Datum an, an dem das Konto am Ende von abläuft.</span><span class="sxs-lookup"><span data-stu-id="68d0d-110">The Active Directory Users and Computers MMC snap-in displays the date that the account will expire at the end of.</span></span> <span data-ttu-id="68d0d-111">Das heißt, das MMC-Snap-in "Active Directory-Benutzer und-Computer" zeigt das Ablaufdatum des Kontos als einen Tag vor dem Datum im **AccountExpires** -Attribut an.</span><span class="sxs-lookup"><span data-stu-id="68d0d-111">That is, the Active Directory Users and Computers MMC snap-in will display the account expiration date as one day earlier than the date contained in the **accountExpires** attribute.</span></span>

 

 

 