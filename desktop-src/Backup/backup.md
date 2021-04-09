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
# <a name="backup"></a>Backup

Mithilfe von Registrierungs Schlüsseln für die Sicherung und Wiederherstellung können Sicherungs Anwendungen mit anderen Anwendungen und Diensten zu Sicherungs-und Wiederherstellungs Vorgängen kommunizieren. Weitere Informationen finden Sie unter [Registrierungsschlüssel und-Werte für die Sicherung und Wiederherstellung](registry-keys-for-backup-and-restore.md).

Die Bandsicherungs-API ermöglicht es Sicherungs Anwendungen, von einem Band zu lesen und zu schreiben, ein Band zu initialisieren und Band-oder Bandlaufwerk Informationen abzurufen. Weitere Informationen finden Sie unter [Bandsicherung](tape-backup.md).

Single Instance Store (SIS) ist eine Architektur, die für die Verwaltung doppelter Dateien mit minimalem Verwaltungsaufwand konzipiert ist. Sicherungs Anwendung verwenden Sie die SIS-Sicherungs-API für den Zugriff auf die SIS-Architektur. Weitere Informationen finden Sie unter [Einzelinstanzspeicher und SIS-Sicherung](single-instance-store-and-sis-backup.md).

Die Sicherung und Wiederherstellung verschlüsselter Dateien wird durch die unformatierte Verschlüsselungs-API aktiviert, die verschlüsselte Dateien liest und schreibt, während die Daten verschlüsselt bleiben. Mit der API können die verschlüsselten Daten in diesen Dateien gesichert und wieder hergestellt werden. gleichzeitig werden die Ziele der Aufrechterhaltung der Sicherheit der gesicherten Daten erreicht und von einer Anwendung verwendet, die nicht über die Berechtigung zum Verwenden der Verschlüsselungsschlüssel für die Datei verfügt. Weitere Informationen finden Sie unter [Sichern und Wiederherstellen verschlüsselter Dateien](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).

Mit dem srverzögert-Tool können Systemstatus-Wiederherstellungs Anwendungen den Kurznamen von Systemdateien verschieben, löschen und festlegen. Weitere Informationen finden Sie unter [Srdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherungs Referenz](backup-reference.md)
</dt> </dl>

 

 