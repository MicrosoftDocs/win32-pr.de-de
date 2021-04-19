---
description: Wird als Handle für einen Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) oder CNG-CSP von CryptoAPI verwendet.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352628"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>hcryptprov- \_ oder \_ NCrypt- \_ Schlüssel \_ handle

Der Datentyp " **hcryptprov" \_ oder " \_ NCrypt \_ Key \_ handle** " wird als Handle für einen [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) oder CNG-CSP verwendet. Dieses Handle muss ein [**hcryptprov**](hcryptprov.md) -Handle sein, das mithilfe der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion oder eines **NCrypt- \_ Schlüssel \_ handle** -Handles erstellt wurde, der mit der [**ncryptopenkey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) -Funktion erstellt wurde. Neue Anwendungen sollten immer das **NCrypt- \_ Schlüssel \_ handle** an einen CNG-CSP übergeben.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



 

 
