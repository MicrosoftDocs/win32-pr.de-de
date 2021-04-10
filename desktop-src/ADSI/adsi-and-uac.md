---
title: ADSI und Benutzerkontensteuerung
description: Windows und Windows Server verfügen über die Benutzerkontensteuerung, die Auswirkungen auf Anwendungen hat, die Active Directory Service Interfaces (ADSI) verwenden.
ms.assetid: 0b286252-8c24-4a18-9dc6-063ca158a8ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36fc88169a8710228a3bf70283aaccd4b4ac42e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039602"
---
# <a name="adsi-and-user-account-control"></a>ADSI und Benutzerkontensteuerung

Windows und Windows Server verfügen über die [Benutzerkontensteuerung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc709691(v=ws.10)), die Auswirkungen auf Anwendungen hat, die [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI) verwenden. Diese Schnittstellen wurden speziell so konzipiert, dass Sie von einem Benutzerkonto mit Administratorrechten auf dem lokalen Computer ausgeführt werden.

**Problem**

Jedes Mal, wenn eine Anwendung eine Verbindung mit dem Verzeichnis herstellt und versucht, ein ADSI-Objekt zu erstellen, wird das [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) auf Änderungen geprüft. Wenn Sie sich seit der letzten Verbindung geändert hat, wird das Schema heruntergeladen und in einem Cache auf dem lokalen Computer gespeichert. In Windows-Versionen vor Windows Vista war der Standard Speicherort für diesen Cache.

`%systemroot%\SchCache\`

Anwendungen, die standardmäßig ausgeführt werden (d. h. nicht-Administrator Konten), haben keinen Zugriff auf dieses Verzeichnis. Folglich können Anwendungen, die ADSI-Schnittstellen verwenden, die in diesem Modus ausgeführt werden, das Schema bei jeder Verbindung herunterladen, was sich auf den Durchsatz und die Leistung auswirkt.

**Lösungen**

*Einzelner Benutzer* : um dieses Problem zu beheben, gibt es neue Registrierungs Steuerungs Schlüssel für ADSI-Anbieter, mit denen die Registrierungs Speicherorte und Dateispeicher Orte für zwischengespeicherte [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) Objekte bestimmt werden. Wenn der Registrierungsschlüssel

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

wird auf 0 (null) festgelegt, und jeder Benutzer erhält einen anderen Speicherort für ADSI. Registrierungsschlüssel werden in gespeichert.

`HKEY_CURRENT_USER\Software\Microsoft\ADs\Providers\LDAP\`

und Cache Dateien werden in gespeichert.

`%LOCALAPPDATA%\Microsoft\Windows\SchCache`

Diese Einstellungen sind die Standardeinstellungen auf Computern, auf denen Windows Server 2008 oder Windows Vista ausgeführt wird.

*Mehr Benutzer* : Wenn Sie ADSI-Anwendungen auf einem Computer mit vielen Benutzerkonten (z. b. einem Webserver) ausführen, ist es vorzuziehen, nicht viele Kopien des [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) Caches zu verwenden, die große Mengen an Speicherplatz aufweisen. Festlegen des Registrierungsschlüssels

`HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\adsi\Cache\PerMachine`

auf 1 (eins) wird ADSI auf das vorherige Verhalten zurückgesetzt. alle [Active Directory Schema](/windows/desktop/ADSchema/active-directory-schema) Objekte werden an Ihren vorherigen Speicherorten gespeichert. der Registrierungsschlüssel wird in

`HKEY_LOCAL_MACHINE\Software\Microsoft\ADs\Providers\LDAP`

die Cachedatei wird in

`%systemroot%\SchCache`

In diesem Fall sollte die Anwendung von Administrator Konten ausgeführt werden. Dadurch wird die Schema Datei im globalen Speicherort für die zukünftige Verwendung durch die Benutzer mit weniger Berechtigungen zwischengespeichert.

 

 