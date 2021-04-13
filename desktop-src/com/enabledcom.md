---
title: EnableDCOM
description: Steuert die globalen Aktivierungs-und rufrichtlinien des Computers. Nur Administratoren und das System verfügen über Vollzugriff auf diesen Teil der Registrierung. Alle anderen Benutzer verfügen über schreibgeschützten Zugriff.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Registrierungs Wert für EnableDCOM com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388153"
---
# <a name="enabledcom"></a>EnableDCOM

Steuert die globalen Aktivierungs-und rufrichtlinien des Computers. Nur Administratoren und das System verfügen über Vollzugriff auf diesen Teil der Registrierung. Alle anderen Benutzer verfügen über schreibgeschützten Zugriff.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ SZ** -Wert.



| Wert    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (oder n) | Keine Remote Clients können Server starten oder eine Verbindung mit Objekten auf diesem Computer herstellen. Lokale Clients können nicht auf Remote-DCOM-Server zugreifen. der gesamte DCOM-Datenverkehr wird blockiert. Das lokale starten von Klassen Code und das Herstellen einer Verbindung mit Objekten ist auf Klassenbasis gemäß den Werten und Zugriffsberechtigungen des Registrierungs Werts " [**launchberechtigungs**](launchpermission.md) " der Klasse und des globalen [**defaultlaunchberechtigung**](defaultlaunchpermission.md) -Registrierungs Werts zulässig. |
| Y (oder y) | Das Starten von Servern und das Herstellen einer Verbindung mit Objekten durch Remote Clients ist auf Klassenbasis gemäß den Werten und Zugriffsberechtigungen des Registrierungs Werts " [**launchberechtigungs**](launchpermission.md) " der Klasse und des globalen [**defaultlaunchberechtigung**](defaultlaunchpermission.md) -Registrierungs Werts zulässig.                                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**Launchberechtigung**](launchpermission.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




