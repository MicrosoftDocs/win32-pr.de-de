---
description: Hier wird überprüft, ob das Online Benutzerprofil geladen wurde.
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: Onprofileloaded-Funktion (lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756433"
---
# <a name="onprofileloaded-function"></a>Onprofileloaded-Funktion

Hier wird überprüft, ob das Online Benutzerprofil geladen wurde.

## <a name="syntax"></a>Syntax


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProviderHandle* \[ in\]
</dt> <dd>

Das Anbieter handle.

</dd> <dt>

*UserToken* \[ in\]
</dt> <dd>

Token des Benutzers, dessen Profil geladen oder entladen wird.

</dd> <dt>

*Geladen* \[ in\]
</dt> <dd>

**True** , wenn das Profil geladen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion Status \_ Erfolg zurück.

Wenn die Funktion fehlschlägt, gibt die Funktion einen Fehlercode ungleich 0 (null) zurück, bei dem es sich um einen anbieterspezifischen Fehler für Diagnosezwecke handelt.

## <a name="remarks"></a>Bemerkungen

Diese Funktion wird jedes Mal aufgerufen, wenn die [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) -Funktion aufgerufen wird. Sie ist nicht mit **LoadUserProfile** synchronisiert. Das heißt, **LoadUserProfile** hat möglicherweise zurückgegeben, und das Profil wurde möglicherweise bis zum Zeitpunkt des Aufrufs der Funktion entladen. Diese Funktion kann mehrmals aufgerufen werden, auch wenn das Profil geladen wurde. Der Identitäts Anbieter darf nicht davon ausgehen, dass ein Aufrufvorgang *mit "* *geladen* " gleich "true" durch einen-Befehl gefolgt von "false" gefolgt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Lsaidprov. h</dt> </dl> |



 

 
