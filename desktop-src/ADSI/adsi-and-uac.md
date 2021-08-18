---
title: ADSI und Benutzerkontensteuerung
description: Windows und Windows Server verfügen über die Benutzerkontensteuerung, die auswirkungen auf Anwendungen hat, die Active Directory-Dienstschnittstellen (ADSI) verwenden.
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1d0163348356f83b64522c9b05607d0d094ceb8f0ad530a798e546021433ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023968"
---
# <a name="adsi-and-user-account-control"></a>ADSI und Benutzerkontensteuerung

Windows und Windows Server verfügen [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10))über die Benutzerkontensteuerung, die auswirkungen auf Anwendungen hat, die [Active Directory-Dienstschnittstellen](active-directory-service-interfaces-adsi.md) (ADSI) verwenden. Insbesondere wurden diese Schnittstellen so konzipiert, dass sie von einem Benutzerkonto mit Administratorrechten auf dem lokalen Computer ausgeführt werden.

**Problem**

Jedes Mal, wenn eine Anwendung eine Verbindung mit dem Verzeichnis herstellt und versucht, ein ADSI-Objekt zu erstellen, wird das [Active Directory-Schema](/windows/desktop/ADSchema/active-directory-schema) auf Änderungen überprüft. Wenn es sich seit der letzten Verbindung geändert hat, wird das Schema heruntergeladen und in einem Cache auf dem lokalen Computer gespeichert. In Versionen von Windows vor Windows Vista war der Standardspeicherort für diesen Cache.

`%systemroot%\SchCache\`

Anwendungen, die über Standardkonten (d. h. Konten ohne Administratorrechte) ausgeführt werden, haben jedoch keinen Zugriff auf dieses Verzeichnis, und daher laden Anwendungen, die ADSI-Schnittstellen verwenden, die in diesem Modus ausgeführt werden, das Schema für jede Verbindung herunter, was sich auf Durchsatz und Leistung auswirken wird.

**Lösungen**

*Einzelner Benutzer:* Um dieses Problem zu beheben, gibt es neue Registrierungsschlüssel des ADSI-Anbieters, die die Registrierungs- und Dateispeicherorte für zwischengespeicherte [Active Directory-Schemaobjekte](/windows/desktop/ADSchema/active-directory-schema) bestimmen. Wenn der Registrierungsschlüssel

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

ist auf 0 (null) festgelegt. Jeder Benutzer hat einen anderen Speicherort für ADSI. Registrierungsschlüssel werden in gespeichert.

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

und Cachedateien werden in gespeichert.

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

Diese Einstellungen sind die Standardeinstellungen auf Computern, auf denen Windows Server 2008 oder Windows Vista ausgeführt wird.

Mehrere Benutzer: Wenn Sie *ADSI-Anwendungen* auf einem Computer mit vielen Benutzerkonten (z. B. einem Webserver) ausführen, ist es vorzuziehen, nicht über viele Kopien des [Active Directory-Schemacaches](/windows/desktop/ADSchema/active-directory-schema) zu verfügen, die große Mengen an Speicherplatz auf dem Datenträger nutzen. Festlegen des Registrierungsschlüssels

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

bei 1 (eins) wird ADSI auf das vorherige Verhalten zurückverwendet. alle [Active Directory-Schemaobjekte](/windows/desktop/ADSchema/active-directory-schema) werden an ihren vorherigen Speicherorten gespeichert. der Registrierungsschlüssel in

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

und die Cachedatei in

`%systemroot%\SchCache`

In diesem Fall sollten Administratorkonten die Anwendung ausführen, wodurch die Schemadatei zur zukünftigen Verwendung durch die Benutzer mit geringeren Berechtigungen am globalen Speicherort zwischengespeichert wird.

 

 