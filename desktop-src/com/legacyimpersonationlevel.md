---
title: Legacyidentitäts ationlevel
description: Legt die Standard Ebene des Identitäts Wechsels für Anwendungen fest, die CoInitializeSecurity nicht aufzurufen.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Registrierungs Wert "legacyidentitäts ationlevel" com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337791"
---
# <a name="legacyimpersonationlevel"></a>Legacyidentitäts ationlevel

Legt die Standard Ebene des Identitäts Wechsels für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen.

> [!Caution]  
> Es wird nicht empfohlen, diesen Wert zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren. Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern. Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ Word** -Wert, der den Konstanten der RPC- \_ C- \_ IMP- \_ Ebene entspricht.



| Wert | Konstante                        |
|-------|---------------------------------|
| 1     | RPC- \_ C- \_ IMP- \_ Ebene \_ Anonym   |
| 2     | RPC- \_ C- \_ IMP- \_ Stufe \_ identifizieren    |
| 3     | Identitätswechsel auf RPC- \_ C- \_ \_ Ebene \_ |
| 4     | RPC- \_ C- \_ IMP- \_ Stufen \_ Delegat    |



 

Wenn dieser Registrierungs Wert nicht vorhanden ist, ist die Standard Ebene des Identitäts Wechsels, die vom System festgelegt wird, 2 (RPC- \_ C- \_ Ebene- \_ Ebene \_ identifizieren).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren von com-Servern](registering-com-servers.md)
</dt> <dt>

[Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md)
</dt> </dl>

 

 




