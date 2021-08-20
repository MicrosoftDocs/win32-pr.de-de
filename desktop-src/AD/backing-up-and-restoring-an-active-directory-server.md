---
title: Sichern und Wiederherstellen eines Active Directory-Servers
description: Active Directory Domain Services Funktionen zum Sichern und Wiederherstellen von Daten in der Verzeichnisdatenbank bereitstellen.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, Verwenden, Sichern und Wiederherstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1955c70daed8cfaed0f5afe6c498a599aebb30f5d7b1846442d22cf84e9634e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024157"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>Sichern und Wiederherstellen eines Active Directory-Servers

Active Directory Domain Services Funktionen zum Sichern und Wiederherstellen von Daten in der Verzeichnisdatenbank bereitstellen. In diesem Abschnitt wird beschrieben, wie Sie einen Active Directory-Server [sichern](backing-up-an-active-directory-server.md) und [wiederherstellen.](restoring-an-active-directory-server.md) Weitere Informationen zum Sichern eines Active Directory-Servers mithilfe der in Windows 2000 und Windows Server 2003 bereitgestellten Hilfsprogramme finden Sie im entsprechenden Resource Kit, das auf der Microsoft TechNet-Website verfügbar ist.

Die Sicherung eines Active Directory-Servers muss online erfolgen und bei der Installation der Active Directory Domain Services erfolgen. Active Directory Domain Services basieren auf einer speziellen Datenbank und exportieren eine Reihe von Sicherungsfunktionen, die die programmgesteuerte Sicherungsschnittstelle bereitstellen. Die Sicherung unterstützt keine inkrementellen Sicherungen. Eine Sicherungsanwendung wird an eine lokale clientseitige DLL gebunden, deren Einstiegspunkte in "Ntdsbcli.h" definiert sind.

Die Wiederherstellung eines Active Directory-Servers erfolgt immer offline.

Obwohl in den Themen in diesem Abschnitt nur beschrieben wird, wie ein Active Directory-Server gesichert und wiederhergestellt wird, sollten Sie beachten, dass Windows 2000 und die Betriebssysteme Windows Server 2003 über mehrere Komponenten für den "Systemzustand" verfügen, die zusammen gesichert und wiederhergestellt werden müssen. Diese Systemzustandskomponenten bestehen aus:

-   Startdateien wie ntldr, ntdetect, alle durch SFP geschützten Dateien und die Konfiguration des Leistungsindikators
-   Der Active Directory-Domäne Controller
-   SysVol (nur Domänencontroller)
-   Zertifikatserver (nur Zertifizierungsstelle)
-   Clusterdatenbank (nur Clusterknoten)
-   Registry
-   COM+-Klassenregistrierungsdatenbank

Der Systemstatus kann in beliebiger Reihenfolge gesichert werden, aber die Wiederherstellung des Systemzustands muss in der folgenden Reihenfolge erfolgen:

1.  Stellen Sie die Startdateien wieder her.
2.  Stellen Sie SysVol, Zertifikatserver, Clusterdatenbank und COM+-Klassenregistrierungsdatenbank nach Bedarf wieder her.
3.  Stellen Sie den Active Directory-Server wieder her.
4.  Stellen Sie die Registrierung wieder her.

Weitere Informationen zum Sichern und Wiederherstellen von Zertifikatdiensten finden Sie unter [Verwenden der Sicherungs- und Wiederherstellungsfunktionen von Zertifikatdiensten.](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions)

Weitere Informationen zum Sichern und Wiederherstellen Active Directory Domain Services finden Sie unter:

-   [Überlegungen zur Active Directory Domain Services Sicherung](considerations-for-active-directory-domain-services-backup.md)
-   [Sichern eines Active Directory-Servers](backing-up-an-active-directory-server.md)
-   [Wiederherstellen eines Active Directory-Servers](restoring-an-active-directory-server.md)
-   [Verzeichnissicherungsfunktionen](directory-backup-functions.md)

 

 