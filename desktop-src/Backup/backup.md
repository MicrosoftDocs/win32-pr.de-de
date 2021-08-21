---
title: Backup
description: Ermöglichen Sie es Sicherungsanwendungen, mit anderen Anwendungen und Diensten über Sicherungs- und Wiederherstellungsvorgänge zu kommunizieren. Führen Sie eine Bandsicherung durch, initialisieren Sie das Band, und rufen Sie Informationen zum Bandlaufwerk ab. Verwalten Sie doppelte Dateien mit dem Einzelinstanzspeicher (SINGLE Instance Store, SIS).
ms.assetid: 97c3e2c4-8214-4093-bd13-3c38c91e08bd
keywords:
- Sicherungssicherung
- backup backup , home
- Wiederherstellungsvorgänge Sichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efe2668df47c271aba5befc3ba380c313b7bc15c11162a29b8364be6eb3fead
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588890"
---
# <a name="backup"></a>Backup

Registrierungsschlüssel für die Sicherung und Wiederherstellung ermöglichen es Sicherungsanwendungen, mit anderen Anwendungen und Diensten über Sicherungs- und Wiederherstellungsvorgänge zu kommunizieren. Weitere Informationen finden Sie unter [Registrierungsschlüssel und -werte für Sicherung und Wiederherstellung.](registry-keys-for-backup-and-restore.md)

Mit der Bandsicherungs-API können Sicherungsanwendungen von einem Band lesen und auf ein Band schreiben, ein Band initialisieren und Band- oder Bandlaufwerkinformationen abrufen. Weitere Informationen finden Sie unter [Bandsicherung.](tape-backup.md)

Der Einzelinstanzspeicher (Single Instance Store, SIS) ist eine Architektur, die darauf ausgelegt ist, doppelte Dateien mit minimalem Mehraufwand zu verwalten. Die Sicherungsanwendung verwendet die SIS-Sicherungs-API für den Zugriff auf die SIS-Architektur. Weitere Informationen finden Sie unter [Einzelinstanz-Store und SIS-Sicherung.](single-instance-store-and-sis-backup.md)

Die Sicherung und Wiederherstellung verschlüsselter Dateien wird durch die unformatierte Verschlüsselungs-API aktiviert, die verschlüsselte Dateien liest und schreibt, während die Daten im verschlüsselten Format bleiben. Die API ermöglicht das Sichern und Wiederherstellen der verschlüsselten Daten in diesen Dateien, während gleichzeitig die Ziele der Aufrechterhaltung der Sicherheit der gesicherten Daten und der Verwendung durch eine Anwendung erreicht werden, die nicht über die Berechtigung zum Verwenden der Verschlüsselungsschlüssel für die Datei verfügt. Weitere Informationen finden Sie unter [Sichern und Wiederherstellen verschlüsselter Dateien.](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)

Mit dem Srdelayed-Tool können Anwendungen zur Wiederherstellung des Systemstatus den Kurznamen von Systemdateien verschieben, löschen und festlegen. Weitere Informationen finden Sie unter [Srdelayed.exe](srdelayed-exe.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherungsreferenz](backup-reference.md)
</dt> </dl>

 

 