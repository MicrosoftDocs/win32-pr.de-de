---
description: Beschreibt die Modi der sicheren Modi für ein Windows-Gerät.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: WLDP_WINDOWS_LOCKDOWN_MODE-Enumeration (wldp. h)
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
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361466"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a>Wldp \_ Windows \_ Lockdown \_ Mode-Enumeration

Beschreibt die Modi der sicheren Modi für ein Windows-Gerät. Wird hauptsächlich in [**wldpquerywindowslockdownmode**](wldpquerywindowslockdownmode.md)verwendet.

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

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**wldp- \_ Windows- \_ \_ \_ Sperrmodus gesperrt**
</dt> <dd>

Geschaltet. Wird hauptsächlich für Windows-Geräte ohne den S-Modus verwendet.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**wldp- \_ Windows- \_ Sperrmodus- \_ \_ Testversion**
</dt> <dd>

Versuchten. Wird hauptsächlich für ein Windows 10-Testgerät mit dem S-Modus verwendet. Der Test Modus ist ein Sonderfall für Windows 10-Geräte mit dem S-Modus: Richtlinien werden erzwungen, aber es gibt keinen Schutz vor der Durchsetzung der Richtlinie.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**wldp- \_ Windows- \_ \_ \_ Sperrmodus gesperrt**
</dt> <dd>

Ene. Wird hauptsächlich für ein Windows 10-Gerät mit dem S-Modus verwendet. Ein gesperrtes Gerät erzwingt die signierten Device Guard-Richtlinien, die mit dem Windows 10-Betriebssystem Image im S-Modus ausgeliefert werden.

</dd> <dt>

<span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**wldp- \_ Windows- \_ \_ Sperrmodus ( \_ max)**
</dt> <dd>

Der maximale Enumerationswert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wldp. h</dt> </dl> |



 

 




