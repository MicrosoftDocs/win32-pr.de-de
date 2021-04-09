---
description: Jeder Server kann einen machineID-Registrierungsschlüssel Wert in der Registrierung festlegen, der als fester Teil der Sitzungs-ID festgelegt wird.
ms.assetid: 1B373496-1C1B-4D4B-8CAC-B572C58E43A2
title: Lastenausgleich mithilfe von SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce190d665f4cc41eb0615a2ddc83e0ee54798d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865728"
---
# <a name="load-balancing-using-schannel"></a>Lastenausgleich mithilfe von SChannel

Jeder Server kann einen machineID-Registrierungsschlüssel Wert in der Registrierung festlegen, der als fester Teil der Sitzungs-ID festgelegt wird. Der Registrierungsschlüssel machineID ist ein **reg \_ DWORD** -Werttyp. Der Load Balancer kann diesen Teil der Sitzungs-ID verwenden, um zu bestimmen, welcher Server die SSL-Sitzung generiert hat, und kann die Zuordnung zu diesem Server beibehalten. Die Sitzungs-ID ist Teil des SSL/TLS-Handshake, der über das Netzwerk gesendet wird. Der Load Balancer-Code sollte beim fortsetzen oder erneuten Herstellen der Verbindung mit dem Client das zweite **DWORD** in der Sitzungs-ID verwenden. Das zweite **DWORD** der von einem SChannel-Server generierten zufälligen Sitzungs-ID wird durch das in der Registrierung gespeicherte **DWORD** ersetzt. Der Registrierungs Wert für das **DWORD** darf nicht 0xFFFFFFFF lauten.

Der Wert des Registrierungsschlüssels lautet wie folgt.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            SecurityProviders
               SCHANNEL
                  MachineID<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

 

 



