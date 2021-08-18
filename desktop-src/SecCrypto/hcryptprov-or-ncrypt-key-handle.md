---
description: Wird als Handle für einen Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) oder CNG-CSP von CryptoAPI verwendet.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982ab2a37c1a2d6035f76cac5c55dcdae44c4cf38f86138c52590c73724b53e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006338"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a>HCRYPTPROV \_ ODER \_ NCRYPT \_ KEY \_ HANDLE

Der **Datentyp HCRYPTPROV \_ OR \_ NCRYPT \_ KEY \_ HANDLE** wird als Handle für einen Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) oder CNG-CSP von CryptoAPI verwendet. Dieses Handle muss ein [**HCRYPTPROV-Handle**](hcryptprov.md) sein, das mit der [**CryptAcquireContext-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) erstellt wurde, oder ein **NCRYPT \_ KEY \_ HANDLE-Handle,** das mit der [**NCryptOpenKey-Funktion**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) erstellt wurde. Neue Anwendungen sollten immer das **NCRYPT \_ KEY \_ HANDLE-Handle** an einen CNG-CSP übergeben.


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
