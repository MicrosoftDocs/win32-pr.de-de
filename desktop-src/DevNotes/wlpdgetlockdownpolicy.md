---
description: Ruft die Bibliothek auf, um den Sicherheitszustand relativ zum Host zu erhalten, und zu verwendetes Skript oder MSI.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Wldpgetlockdownpolicy-Funktion (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523464"
---
# <a name="wldpgetlockdownpolicy-function"></a>Wldpgetlockdownpolicy-Funktion

Ruft die Bibliothek auf, um den Sicherheitszustand relativ zum Host zu erhalten, und zu verwendetes Skript oder MSI. Die Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die LoadLibrary-Funktion und die GetProcAddress-Funktion verwenden, um dynamisch mit wldp.dll zu verknüpfen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hostinformationen* \[ in, optional\]
</dt> <dd>

Eine [**wldp- \_ Host \_ Informations**](wldp-host-information.md) Struktur, die den zu bewertenden Host und die zu bewertende Quelldatei identifiziert.

</dd> <dt>

*lockdownstate* \[ vorgenommen\]
</dt> <dd>

Stellt den resultierenden sicheren Richtlinien Wert bereit. Sei! WLDP_LOCKDOWN_IS_OFF, dann ist die Option "mehr CI" aktiviert. Sie können auch WLDP_LOCKDOWN_IS_AUDIT und WLDP_LOCKDOWN_IS_ENFORCE überprüfen, um festzustellen, ob eine Richtlinie im Überwachungs-oder Erzwingungs Modus ist.
</dd> <dt>

*LOCKDOWNFLAGS* \[ in\]
</dt> <dd>

Die folgenden Flagwerte sind definiert: wldp- \_ Flags \_ skipsignaturevalidation 0x00000100 – Wenn festgelegt, überspringen Sie die Überprüfung von SaferIdentifyLevel, wodurch ignoriert wird, ob ein Skript signiert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt \_ bei Erfolg S OK zurück oder andernfalls einen Fehlercode.

## <a name="remarks"></a>Hinweise

Beim Aufruf mit wldp- \_ Host \_ Informationen. szsource = NULL wird die generische Richtlinie für den Host zurückgegeben.

Beim Aufrufen mit wldp \_ \_ -Hostinformationen. dwhostid = wldp \_ Host- \_ ID \_ Global, wldp- \_ Host \_ Informationen. szsource muss NULL sein, und die Funktion gibt die globale System Richtlinie zurück.

Das dwFlag wldp-Flag \_ \_ skipsignaturevalidation kann verwendet werden, um die SaferIdentifyLevel ()-Überprüfung zu überspringen. Dadurch wird ignoriert, ob ein Skript signiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




