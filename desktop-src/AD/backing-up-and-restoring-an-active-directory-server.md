---
title: Sichern und Wiederherstellen eines Active Directory Servers
description: Active Directory Domain Services Funktionen zum Sichern und Wiederherstellen von Daten in der Verzeichnis Datenbank bereitstellen.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, verwenden, sichern und Wiederherstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724649"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a>Sichern und Wiederherstellen eines Active Directory Servers

Active Directory Domain Services Funktionen zum Sichern und Wiederherstellen von Daten in der Verzeichnis Datenbank bereitstellen. In diesem Abschnitt wird beschrieben, wie ein Active Directory Server [gesichert](backing-up-an-active-directory-server.md) und [wieder hergestellt](restoring-an-active-directory-server.md) wird. Weitere Informationen zum Sichern eines Active Directory Servers mithilfe der Hilfsprogramme in den Betriebssystemen Windows 2000 und Windows Server 2003 finden Sie im entsprechenden Ressourcenkit, das auf der Microsoft TechNet-Website verfügbar ist.

Die Sicherung eines Active Directory Servers muss online durchgeführt werden und muss bei der Installation der Active Directory Domain Services ausgeführt werden. Active Directory Domain Services werden auf einer speziellen Datenbank erstellt und exportieren eine Reihe von Sicherungsfunktionen, die die programmgesteuerte Sicherungs Schnittstelle bereitstellen. Die Sicherung unterstützt keine inkrementellen Sicherungen. Eine Sicherungs Anwendung bindet an eine lokale Client seitige dll mit in ntdsbcli. h definierten Einstiegspunkten.

Die Wiederherstellung eines Active Directory Servers erfolgt immer offline.

Obwohl in den Themen in diesem Abschnitt nur das Sichern und Wiederherstellen eines Active Directory Servers beschrieben wird, beachten Sie, dass die Betriebssysteme Windows 2000 und Windows Server 2003 mehrere Systemstatus Komponenten aufweisen, die gleichzeitig gesichert und wieder hergestellt werden müssen. Diese Systemstatus Komponenten bestehen aus folgenden Komponenten:

-   Startdateien wie NTLDR, ntdetect, alle durch SFP geschützten Dateien und die Konfiguration des Leistungs Zählers
-   Der Active Directory-Domäne Controller
-   SYSVOL (nur Domänen Controller)
-   Zertifikat Server (nur ca)
-   Cluster Datenbank (nur Cluster Knoten)
-   Registrierung
-   Com+-Klassen Registrierungsdatenbank

Der Systemstatus kann in beliebiger Reihenfolge gesichert werden, aber die Wiederherstellung des Systemstatus muss in der folgenden Reihenfolge erfolgen:

1.  Stellen Sie die Startdateien wieder her.
2.  Stellen Sie SYSVOL, den Zertifikat Server, die Cluster Datenbank und die com+-Klassen Registrierungsdatenbank ggf. wieder her.
3.  Stellen Sie den Active Directory Server wieder her.
4.  Stellen Sie die Registrierung wieder her.

Weitere Informationen zum Sichern und Wiederherstellen von Zertifikat Diensten finden [Sie unter Verwenden der Funktionen zum Sichern und Wiederherstellen von Zertifikat Diensten](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).

Weitere Informationen zum Sichern und Wiederherstellen von Active Directory Domain Services finden Sie unter:

-   [Überlegungen zur Active Directory Domain Services Sicherung](considerations-for-active-directory-domain-services-backup.md)
-   [Sichern eines Active Directory Servers](backing-up-an-active-directory-server.md)
-   [Wiederherstellen eines Active Directory Servers](restoring-an-active-directory-server.md)
-   [Verzeichnis Sicherungsfunktionen](directory-backup-functions.md)

 

 