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
# <a name="backing-up-and-restoring-an-active-directory-server"></a><span data-ttu-id="8816e-104">Sichern und Wiederherstellen eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="8816e-104">Backing Up and Restoring an Active Directory Server</span></span>

<span data-ttu-id="8816e-105">Active Directory Domain Services Funktionen zum Sichern und Wiederherstellen von Daten in der Verzeichnis Datenbank bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8816e-105">Active Directory Domain Services provide functions for backing up and restoring data in the directory database.</span></span> <span data-ttu-id="8816e-106">In diesem Abschnitt wird beschrieben, wie ein Active Directory Server [gesichert](backing-up-an-active-directory-server.md) und [wieder hergestellt](restoring-an-active-directory-server.md) wird.</span><span class="sxs-lookup"><span data-stu-id="8816e-106">This section describes how to [back up](backing-up-an-active-directory-server.md) and [restore](restoring-an-active-directory-server.md) an Active Directory server.</span></span> <span data-ttu-id="8816e-107">Weitere Informationen zum Sichern eines Active Directory Servers mithilfe der Hilfsprogramme in den Betriebssystemen Windows 2000 und Windows Server 2003 finden Sie im entsprechenden Ressourcenkit, das auf der Microsoft TechNet-Website verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8816e-107">For more information about backing up an Active Directory server using the utilities provided in Windows 2000 and Windows Server 2003 operating systems, see the applicable Resource Kit, available on the Microsoft TechNet website.</span></span>

<span data-ttu-id="8816e-108">Die Sicherung eines Active Directory Servers muss online durchgeführt werden und muss bei der Installation der Active Directory Domain Services ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8816e-108">Backup of an Active Directory server must be performed online and must be performed when the Active Directory Domain Services are installed.</span></span> <span data-ttu-id="8816e-109">Active Directory Domain Services werden auf einer speziellen Datenbank erstellt und exportieren eine Reihe von Sicherungsfunktionen, die die programmgesteuerte Sicherungs Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8816e-109">Active Directory Domain Services are built on a special database and export a set of backup functions that provide the programmatic backup interface.</span></span> <span data-ttu-id="8816e-110">Die Sicherung unterstützt keine inkrementellen Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="8816e-110">The backup does not support incremental backups.</span></span> <span data-ttu-id="8816e-111">Eine Sicherungs Anwendung bindet an eine lokale Client seitige dll mit in ntdsbcli. h definierten Einstiegspunkten.</span><span class="sxs-lookup"><span data-stu-id="8816e-111">A backup application binds to a local client-side DLL with entry points defined in Ntdsbcli.h.</span></span>

<span data-ttu-id="8816e-112">Die Wiederherstellung eines Active Directory Servers erfolgt immer offline.</span><span class="sxs-lookup"><span data-stu-id="8816e-112">Restoration of an Active Directory server is always performed offline.</span></span>

<span data-ttu-id="8816e-113">Obwohl in den Themen in diesem Abschnitt nur das Sichern und Wiederherstellen eines Active Directory Servers beschrieben wird, beachten Sie, dass die Betriebssysteme Windows 2000 und Windows Server 2003 mehrere Systemstatus Komponenten aufweisen, die gleichzeitig gesichert und wieder hergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8816e-113">Although the topics in this section describe only how to back up and restore an Active Directory server, be aware that Windows 2000 and the Windows Server 2003 operating systems have several "system state" components that must be backed up and restored together.</span></span> <span data-ttu-id="8816e-114">Diese Systemstatus Komponenten bestehen aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="8816e-114">These system state components consist of:</span></span>

-   <span data-ttu-id="8816e-115">Startdateien wie NTLDR, ntdetect, alle durch SFP geschützten Dateien und die Konfiguration des Leistungs Zählers</span><span class="sxs-lookup"><span data-stu-id="8816e-115">Boot files such as ntldr, ntdetect, all files protected by SFP, and performance counter configuration</span></span>
-   <span data-ttu-id="8816e-116">Der Active Directory-Domäne Controller</span><span class="sxs-lookup"><span data-stu-id="8816e-116">The Active Directory Domain Controller</span></span>
-   <span data-ttu-id="8816e-117">SYSVOL (nur Domänen Controller)</span><span class="sxs-lookup"><span data-stu-id="8816e-117">SysVol (domain controller only)</span></span>
-   <span data-ttu-id="8816e-118">Zertifikat Server (nur ca)</span><span class="sxs-lookup"><span data-stu-id="8816e-118">Certificate Server (CA only)</span></span>
-   <span data-ttu-id="8816e-119">Cluster Datenbank (nur Cluster Knoten)</span><span class="sxs-lookup"><span data-stu-id="8816e-119">Cluster database (cluster node only)</span></span>
-   <span data-ttu-id="8816e-120">Registrierung</span><span class="sxs-lookup"><span data-stu-id="8816e-120">Registry</span></span>
-   <span data-ttu-id="8816e-121">Com+-Klassen Registrierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="8816e-121">COM+ class registration database</span></span>

<span data-ttu-id="8816e-122">Der Systemstatus kann in beliebiger Reihenfolge gesichert werden, aber die Wiederherstellung des Systemstatus muss in der folgenden Reihenfolge erfolgen:</span><span class="sxs-lookup"><span data-stu-id="8816e-122">The system state can be backed up in any order, but restoration of the system state must occur in the following order:</span></span>

1.  <span data-ttu-id="8816e-123">Stellen Sie die Startdateien wieder her.</span><span class="sxs-lookup"><span data-stu-id="8816e-123">Restore the boot files.</span></span>
2.  <span data-ttu-id="8816e-124">Stellen Sie SYSVOL, den Zertifikat Server, die Cluster Datenbank und die com+-Klassen Registrierungsdatenbank ggf. wieder her.</span><span class="sxs-lookup"><span data-stu-id="8816e-124">Restore SysVol, Certificate Server, Cluster database and COM+ class registration database, as applicable.</span></span>
3.  <span data-ttu-id="8816e-125">Stellen Sie den Active Directory Server wieder her.</span><span class="sxs-lookup"><span data-stu-id="8816e-125">Restore the Active Directory server.</span></span>
4.  <span data-ttu-id="8816e-126">Stellen Sie die Registrierung wieder her.</span><span class="sxs-lookup"><span data-stu-id="8816e-126">Restore the registry.</span></span>

<span data-ttu-id="8816e-127">Weitere Informationen zum Sichern und Wiederherstellen von Zertifikat Diensten finden [Sie unter Verwenden der Funktionen zum Sichern und Wiederherstellen von Zertifikat Diensten](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span><span class="sxs-lookup"><span data-stu-id="8816e-127">For more information about backing up and restoring Certificate Services, see [Using the Certificate Services Backup and Restore Functions](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span></span>

<span data-ttu-id="8816e-128">Weitere Informationen zum Sichern und Wiederherstellen von Active Directory Domain Services finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="8816e-128">For more information about backing up and restoring Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="8816e-129">Überlegungen zur Active Directory Domain Services Sicherung</span><span class="sxs-lookup"><span data-stu-id="8816e-129">Considerations for Active Directory Domain Services Backup</span></span>](considerations-for-active-directory-domain-services-backup.md)
-   [<span data-ttu-id="8816e-130">Sichern eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="8816e-130">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
-   [<span data-ttu-id="8816e-131">Wiederherstellen eines Active Directory Servers</span><span class="sxs-lookup"><span data-stu-id="8816e-131">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
-   [<span data-ttu-id="8816e-132">Verzeichnis Sicherungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="8816e-132">Directory Backup Functions</span></span>](directory-backup-functions.md)

 

 