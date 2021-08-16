---
title: Kontoablauf (WinNT-Anbieter)
description: Bei Verwendung des WinNT-Anbieters kann das Ablaufdatum des Kontos mithilfe der IADsUser.AccountExpirationDate-Eigenschaft festgelegt werden.
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- Kontoablauf ADSI, WinNT-Anbieter
- WinNT-Anbieter ADSI , Benutzerverwaltungsbeispiele, Kontoablauf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd23973a4de31fed629428be9f4df1b6cade34e77f78680a5f87c9d55c42234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838410"
---
# <a name="account-expiration-winnt-provider"></a>Kontoablauf (WinNT-Anbieter)

Bei Verwendung des WinNT-Anbieters kann das Ablaufdatum des Kontos mithilfe der [**IADsUser.AccountExpirationDate-Eigenschaft festgelegt**](iadsuser-property-methods.md) werden.

Legen Sie zum Festlegen des Ablaufdatums des Kontos die [**IADsUser.AccountExpirationDate-Eigenschaft**](iadsuser-property-methods.md) auf den gewünschten Datumswert fest. Legen Sie diese Eigenschaft auf "1. Januar 1970" fest, um das Ablaufdatum des Kontos so zu festlegen, dass es nie abläuft.

## <a name="example-1"></a>Beispiel 1

Das folgende Codebeispiel zeigt, wie Sie das Ablaufdatum des Kontos mithilfe von Visual Basic ADSI festlegen.


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

Das folgende Codebeispiel zeigt, wie Sie das Ablaufdatum des Kontos mit C++ mit ADSI festlegen.


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



 

 




