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
# <a name="account-expiration-winnt-provider"></a>Konto Ablauf (WinNT-Anbieter)

Wenn Sie den WinNT-Anbieter verwenden, kann das Ablaufdatum des Kontos mithilfe der [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) -Eigenschaft festgelegt werden.

Um das Ablaufdatum des Kontos festzulegen, legen Sie die [**IADsUser. AccountExpirationDate**](iadsuser-property-methods.md) -Eigenschaft auf den gewünschten Datumswert fest. Um das Ablaufdatum des Kontos so festzulegen, dass es nie abläuft, legen Sie diese Eigenschaft auf "January 1, 1970" fest.

## <a name="example-1"></a>Beispiel 1

Im folgenden Codebeispiel wird gezeigt, wie das Ablaufdatum des Kontos mithilfe Visual Basic mit ADSI festgelegt wird.


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a>Beispiel 2

Im folgenden Codebeispiel wird gezeigt, wie das Ablaufdatum des Kontos mithilfe von C++ mit ADSI festgelegt wird.


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



 

 




