---
description: Beschreibt die Sicherheitsmodi (S-Modi) für ein Windows Gerät.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: WLDP_WINDOWS_LOCKDOWN_MODE -Enumeration (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 93a3ae8ef00c306d93995a3a97236fc9086185147144c4314726c507d8b52e57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911340"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>WLDP WINDOWS \_ \_ LOCKDOWN \_ MODE-Enumeration

Beschreibt die Sicherheitsmodi (S-Modi) für ein Windows Gerät. Wird hauptsächlich in [**WldpQueryWindowsLockdownMode verwendet.**](wldpquerywindowslockdownmode.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP WINDOWS \_ LOCKDOWN MODE UNLOCKED (WLDP-WINDOWS-SPERRMODUS \_ \_ \_ ENTSPERRT)**
</dt> <dd>

Entsperrt. Wird hauptsächlich für Windows ohne den S-Modus verwendet.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP \_ WINDOWS \_ LOCKDOWN \_ MODE \_ TRIAL**
</dt> <dd>

Probephase. Wird hauptsächlich für ein Windows 10-Testgerät mit dem S-Modus verwendet. Der Testmodus ist ein Sonderfall für Windows 10-Geräte mit dem S-Modus: Richtlinien werden erzwungen, es gibt jedoch keinen Antirollbackschutz für die Erzwingung der Richtlinie.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ WINDOWS \_ LOCKDOWN \_ MODE \_ LOCKED**
</dt> <dd>

Gesperrt. Wird hauptsächlich für ein Windows 10 mit dem S-Modus verwendet. Ein gesperrtes Gerät erzwingt die signierten Device Guard-Richtlinien, die mit dem Windows 10-Betriebssystemimage im S-Modus ausgeliefert werden.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP \_ WINDOWS \_ LOCKDOWN \_ MODE \_ MAX**
</dt> <dd>

Der maximale Enumerationswert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wldp.h</dt> </dl> |



 

 




