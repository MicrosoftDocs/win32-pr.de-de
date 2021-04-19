---
description: Stellt ein Handle für eine installierbare Objekt Bezeichner-Funktion (OID) dar.
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: Hcryptoidfuncaddr (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350386"
---
# <a name="hcryptoidfuncaddr"></a>Hcryptoidfuncaddr

Der **hcryptoidfuncaddr** -Datentyp stellt ein Handle für eine installierbare [*Objekt Bezeichner*](../secgloss/o-gly.md) -Funktion (OID) dar. Die Funktionen " [**cryptgetdefaultoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)", " [**cryptgetoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)" und " [**cryptfreoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) " und " [**CERT \_ Store \_ Prov \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) " verwenden diesen Datentyp.


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



 

 
