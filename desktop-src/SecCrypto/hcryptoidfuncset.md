---
description: Stellt ein Handle für einen Satz von installierbaren OID-Funktionen (Object Identifier) dar.
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3926b78359450b780a9952aeae9d957157ebb56973a7f428824b07cbb43e9a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006468"
---
# <a name="hcryptoidfuncset"></a>HCRYPTOIDFUNCSET

Der **HCRYPTOIDFUNCSET-Datentyp** stellt ein Handle für einen Satz von installierbaren OID-Funktionen [*(Object Identifier)*](../secgloss/o-gly.md) dar. Die Funktionen [**CryptGetDefaultOIDFunctionAddress,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) [**CryptGetOIDFunctionAddress,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)und [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) verwenden diesen Datentyp.


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
