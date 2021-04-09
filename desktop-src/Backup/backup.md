---
title: Backup
description: Ermöglicht es Sicherungs Anwendungen, mit anderen Anwendungen und Diensten über Sicherungs-und Wiederherstellungs Vorgänge zu kommunizieren. Ausführen der Bandsicherung, Initialisieren des Bands und Abrufen von Informationen zum Bandlaufwerk. Warten Sie doppelte Dateien mit Single Instance Store (SIS).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- Sicherungs Sicherung
- Sicherungs Sicherung, Startseite
- Wiederherstellungs Vorgänge sichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 689a5a4613bdf029b270947b523727ea00a6e05d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101995"
---
# <a name="backup"></a><span data-ttu-id="748b8-108">Backup</span><span class="sxs-lookup"><span data-stu-id="748b8-108">Backup</span></span>

<span data-ttu-id="748b8-109">Mithilfe von Registrierungs Schlüsseln für die Sicherung und Wiederherstellung können Sicherungs Anwendungen mit anderen Anwendungen und Diensten zu Sicherungs-und Wiederherstellungs Vorgängen kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="748b8-109">Registry keys for backup and restore allow backup applications to communicate with other applications and services about backup and restore operations.</span></span> <span data-ttu-id="748b8-110">Weitere Informationen finden Sie unter [Registrierungsschlüssel und-Werte für die Sicherung und Wiederherstellung](registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="748b8-110">For more information, see [Registry Keys and Values for Backup and Restore](registry-keys-for-backup-and-restore.md).</span></span>

<span data-ttu-id="748b8-111">Die Bandsicherungs-API ermöglicht es Sicherungs Anwendungen, von einem Band zu lesen und zu schreiben, ein Band zu initialisieren und Band-oder Bandlaufwerk Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="748b8-111">The tape backup API enables backup applications to read from and write to a tape, initialize a tape, and retrieve tape or tape drive information.</span></span> <span data-ttu-id="748b8-112">Weitere Informationen finden Sie unter [Bandsicherung](tape-backup.md).</span><span class="sxs-lookup"><span data-stu-id="748b8-112">For more information, see [Tape Backup](tape-backup.md).</span></span>

<span data-ttu-id="748b8-113">Single Instance Store (SIS) ist eine Architektur, die für die Verwaltung doppelter Dateien mit minimalem Verwaltungsaufwand konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="748b8-113">Single-instance store (SIS) is an architecture designed to maintain duplicate files with a minimum of overhead.</span></span> <span data-ttu-id="748b8-114">Sicherungs Anwendung verwenden Sie die SIS-Sicherungs-API für den Zugriff auf die SIS-Architektur.</span><span class="sxs-lookup"><span data-stu-id="748b8-114">Backup application use the SIS backup API to access the SIS architecture.</span></span> <span data-ttu-id="748b8-115">Weitere Informationen finden Sie unter [Einzelinstanzspeicher und SIS-Sicherung](single-instance-store-and-sis-backup.md).</span><span class="sxs-lookup"><span data-stu-id="748b8-115">For more information, see [Single-Instance Store and SIS Backup](single-instance-store-and-sis-backup.md).</span></span>

<span data-ttu-id="748b8-116">Die Sicherung und Wiederherstellung verschlüsselter Dateien wird durch die unformatierte Verschlüsselungs-API aktiviert, die verschlüsselte Dateien liest und schreibt, während die Daten verschlüsselt bleiben.</span><span class="sxs-lookup"><span data-stu-id="748b8-116">Backup and restore of encrypted files is enabled by the raw encryption API, which reads and writes encrypted files while keeping the data in encrypted format.</span></span> <span data-ttu-id="748b8-117">Mit der API können die verschlüsselten Daten in diesen Dateien gesichert und wieder hergestellt werden. gleichzeitig werden die Ziele der Aufrechterhaltung der Sicherheit der gesicherten Daten erreicht und von einer Anwendung verwendet, die nicht über die Berechtigung zum Verwenden der Verschlüsselungsschlüssel für die Datei verfügt.</span><span class="sxs-lookup"><span data-stu-id="748b8-117">The API allows the encrypted data in these files to be backed up and restored, while meeting the goals of maintaining the security of the backed up data, and being usable by an application that lacks permission to use the encryption keys on the file.</span></span> <span data-ttu-id="748b8-118">Weitere Informationen finden Sie unter [Sichern und Wiederherstellen verschlüsselter Dateien](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span><span class="sxs-lookup"><span data-stu-id="748b8-118">For more information, see [Backup and Restore of Encrypted Files](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span></span>

<span data-ttu-id="748b8-119">Mit dem srverzögert-Tool können Systemstatus-Wiederherstellungs Anwendungen den Kurznamen von Systemdateien verschieben, löschen und festlegen.</span><span class="sxs-lookup"><span data-stu-id="748b8-119">The Srdelayed tool can enable system state recovery applications to move, delete, and set the short name of system files.</span></span> <span data-ttu-id="748b8-120">Weitere Informationen finden Sie unter [Srdelayed.exe](srdelayed-exe.md).</span><span class="sxs-lookup"><span data-stu-id="748b8-120">For more information, see [Srdelayed.exe](srdelayed-exe.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="748b8-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="748b8-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="748b8-122">Sicherungs Referenz</span><span class="sxs-lookup"><span data-stu-id="748b8-122">Backup Reference</span></span>](backup-reference.md)
</dt> </dl>

 

 