---
title: EnableDCOM
description: Steuert die globale Aktivierungs- und Aufrufrichtlinien des Computers. Nur Administratoren und das System haben Vollzugriff auf diesen Teil der Registrierung. Alle anderen Benutzer haben schreibgeschützten Zugriff.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- EnableDCOM-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74aea79cf600aad4407b96b5c4a10e8f44633a1c928f8b7e376c192b108cb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793599"
---
# <a name="enabledcom"></a>EnableDCOM

Steuert die globale Aktivierungs- und Aufrufrichtlinien des Computers. Nur Administratoren und das System haben Vollzugriff auf diesen Teil der Registrierung. Alle anderen Benutzer haben schreibgeschützten Zugriff.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ SZ-Wert.**



| Wert    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (oder n) | Keine Remoteclients dürfen Server starten oder eine Verbindung mit Objekten auf diesem Computer herstellen. Lokale Clients können nicht auf DCOM-Remoteserver zugreifen. Der ganze DCOM-Datenverkehr wird blockiert. Der lokale Start von Klassencode und das Herstellen einer Verbindung mit Objekten sind pro Klasse zulässig, je nach Wert und Zugriffsberechtigungen des [**LaunchPermission-Registrierungswerts**](launchpermission.md) der Klasse und des globalen [**Registrierungswerts DefaultLaunchPermission.**](defaultlaunchpermission.md) |
| Y (oder y) | Das Starten von Servern und das Herstellen einer Verbindung mit Objekten durch Remoteclients ist pro Klasse gemäß dem Wert und den Zugriffsberechtigungen des [**LaunchPermission-Registrierungswerts**](launchpermission.md) der Klasse und des globalen [**Registrierungswerts DefaultLaunchPermission**](defaultlaunchpermission.md) zulässig.                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 




