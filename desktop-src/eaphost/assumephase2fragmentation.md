---
title: AssumePhase2Fragmentation
description: Der Registrierungsschlüssel AssumePhase2Fragmentation bestimmt, ob der Server und der Client die Fragmentierung der Phase 2 annehmen.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389636"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

Der Registrierungsschlüssel AssumePhase2Fragmentation bestimmt, ob der Server und der Client die Fragmentierung der Phase 2 annehmen.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert   | BESCHREIBUNG                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | Server und Client gehen davon aus, dass die andere Partei während der Peer-Authentifizierung keine Fragmentierung in Phase 2 durchsetzen kann. |
| ungleich NULL | Server und Client gehen davon aus, dass die andere Partei während der Peer-Authentifizierung die Fragmentierung der Phase 2 unterstützt.     |



 

Wenn dieser Registrierungs Wert nicht vorhanden ist, gehen Server und Client davon aus, dass die andere Partei während der Peer-Authentifizierung die Fragmentierung der Phase 2 unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Registrierungs Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




