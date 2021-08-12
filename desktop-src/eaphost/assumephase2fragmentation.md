---
title: AssumePhase2Fragmentation
description: Der Registrierungsschlüssel AssumePhase2Fragmentation bestimmt, ob der Server und der Client die Fragmentierung der Phase 2 annehmen.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caee785b0c89b92aaf4b01c590425c451b9a977664e915874e7eb5ad1edf46aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275837"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

Der Registrierungsschlüssel AssumePhase2Fragmentation bestimmt, ob der Server und der Client die Fragmentierung der Phase 2 annehmen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **\_ REG-DWORD-Wert.**



| Wert   | Beschreibung                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | Server und Client gehen davon aus, dass die andere Partei während der PEAP-Authentifizierung nicht in der Lage ist, die Phase 2 zu fragmentieren. |
| Nonzero | Server und Client gehen davon aus, dass die andere Partei in der Lage ist, die Phase 2-Fragmentierung während der PEAP-Authentifizierung zu erstellen.     |



 

Wenn dieser Registrierungswert nicht vorhanden ist, gehen server und client davon aus, dass die andere Partei während der PEAP-Authentifizierung in der Lage ist, die Phase 2 zu fragmentieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




