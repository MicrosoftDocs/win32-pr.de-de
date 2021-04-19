---
description: Stellt ein Handle für einen Satz von installierbaren Funktionen für Objekt Bezeichner (OID) dar.
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: Hcryptoidfuncset (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364138"
---
# <a name="hcryptoidfuncset"></a>Hcryptoidfuncset

Der **hcryptoidfuncset** -Datentyp stellt ein Handle für einen Satz von installierbaren Funktionen für [*Objekt Bezeichner*](../secgloss/o-gly.md) (OID) dar. Die Funktionen " [**cryptgetdefaultoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress)", " [**cryptgetoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)", " [**cryptfreoidfunctionaddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)" und " [**cryptinitoidfunctionset**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) " verwenden diesen Datentyp.


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinCrypt. h</dt> </dl> |



 

 
