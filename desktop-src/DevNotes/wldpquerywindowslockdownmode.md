---
description: Ruft den aktuellen sicheren Windows ab. Windows kann sich im gesperrten Modus, im entsperrten normalen Modus oder im Testmodus befinden.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: WldpQueryWindowsLockdownMode-Funktion (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryWindowsLockdownMode
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 94dc1665dcfa98b27fc15f68a799792b57f428875fefb88c6d35de57bad71b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911290"
---
# <a name="wldpquerywindowslockdownmode-function"></a>WldpQueryWindowsLockdownMode-Funktion

Ruft den aktuellen sicheren Windows ab. Windows kann sich im gesperrten Modus, im entsperrten normalen Modus oder im Testmodus befinden.

## <a name="syntax"></a>Syntax


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lockdownMode* \[ out\]
</dt> <dd>

Bei Erfolg wird ein [**PWLDP \_ WINDOWS \_ \_ LOCKDOWN-MODUS**](wldp-windows-lockdown-mode.md) zurückgegeben, der den sicheren Modus für das aktuelle Windows 10 angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S \_ OK zurück,** wenn erfolgreich, andernfalls ein Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1803 desktop apps only (Nur \[ Desktop-Apps der Version 1803)\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




