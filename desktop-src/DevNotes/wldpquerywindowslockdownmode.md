---
description: Ruft den aktuellen sicheren Windows-Modus ab. Fenster können sich im gesperrten Modus befinden, nicht im normalen Modus oder im Testmodus.
ms.assetid: FD280818-C6DE-4CEA-A772-E239A8DB891F
title: Wldpquerywindowslockdownmode-Funktion (wldp. h)
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
ms.openlocfilehash: fc746270a0634525154417cfba7e1529bee7edfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214242"
---
# <a name="wldpquerywindowslockdownmode-function"></a>Wldpquerywindowslockdownmode-Funktion

Ruft den aktuellen sicheren Windows-Modus ab. Fenster können sich im gesperrten Modus befinden, nicht im normalen Modus oder im Testmodus.

## <a name="syntax"></a>Syntax


```C++
 WINAPI WldpQueryWindowsLockdownMode(
  _Out_ PWLDP_WINDOWS_LOCKDOWN_MODE lockdownMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lockdownmode* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg wird der [**Modus "pwldp \_ Windows \_ Lockdown \_**](wldp-windows-lockdown-mode.md) " zurückgegeben, der den sicheren Modus für das aktuelle Windows 10-Gerät angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1803, \[ nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




