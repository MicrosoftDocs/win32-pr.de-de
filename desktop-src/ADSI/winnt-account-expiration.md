---
title: Konto Ablauf (WinNT-Anbieter)
description: Wenn Sie den WinNT-Anbieter verwenden, kann das Ablaufdatum des Kontos mithilfe der IADsUser. AccountExpirationDate-Eigenschaft festgelegt werden.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- Konto Ablauf ADSI, WinNT-Anbieter
- WinNT-Anbieter ADSI, Beispiele für die Benutzerverwaltung, Konto Ablauf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4936004cbd68c853f5e6d5c76a405f2a8340d22a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106353698"
---
# <a name="account-expiration-winnt-provider"></a><span data-ttu-id="bf116-105">Konto Ablauf (WinNT-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="bf116-105">Account Expiration (WinNT Provider)</span></span>

<span data-ttu-id="bf116-106">Wenn Sie den WinNT-Anbieter verwenden, kann das Ablaufdatum des Kontos mithilfe der [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bf116-106">When using the WinNT provider, the account expiration date can be set using the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property.</span></span>

<span data-ttu-id="bf116-107">Um das Ablaufdatum des Kontos festzulegen, legen Sie die [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) -Eigenschaft auf den gewünschten Datumswert fest.</span><span class="sxs-lookup"><span data-stu-id="bf116-107">To set the account expiration date, set the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property to the desired date value.</span></span> <span data-ttu-id="bf116-108">Um das Ablaufdatum des Kontos so festzulegen, dass es nie abläuft, legen Sie diese Eigenschaft auf "January 1, 1970" fest.</span><span class="sxs-lookup"><span data-stu-id="bf116-108">To set the account expiration date to never expire, set this property to "January 1, 1970".</span></span>

## <a name="example-1"></a><span data-ttu-id="bf116-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf116-109">Example 1</span></span>

<span data-ttu-id="bf116-110">Im folgenden Codebeispiel wird gezeigt, wie das Ablaufdatum des Kontos mithilfe Visual Basic mit ADSI festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bf116-110">The following code example shows how to set the account expiration date using Visual Basic with ADSI.</span></span>


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="bf116-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bf116-111">Example 2</span></span>

<span data-ttu-id="bf116-112">Im folgenden Codebeispiel wird gezeigt, wie das Ablaufdatum des Kontos mithilfe von C++ mit ADSI festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bf116-112">The following code example shows how to set the account expiration date using C++ with ADSI.</span></span>


```C++
void SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
   if(!pUser) return;

   HRESULT hr = S_OK;
   hr = pUser->put_AccountExpirationDate(date); // Set the account to expires on date.
   
   hr = pUser->SetInfo();
   hr = pUser->Release();
   return;
}
```



 

 




