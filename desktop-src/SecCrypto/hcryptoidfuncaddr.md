---
description: Stellt ein Handle für eine installierbare OID-Funktion (Object Identifier) dar.
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb36bdd98332842d89533c9c34a880aecdc8555cd64bb03888c0bd146cea3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006548"
---
# <a name="hcryptoidfuncaddr"></a>HCRYPTOIDFUNCADDR

Der **HCRYPTOIDFUNCADDR-Datentyp** stellt ein Handle für eine installierbare OID-Funktion [*(Object Identifier)*](../secgloss/o-gly.md) dar. Die [**Funktionen CryptGetDefaultOIDFunctionAddress,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)und [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) und [**die CERT STORE \_ \_ PROV \_ INFO-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) verwenden diesen Datentyp.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
