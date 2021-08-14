---
description: Wie Sie die Sicherungsfunktionen der Zertifikatdienste verwenden können, um eine Zertifikatdienst-Datenbank und die zugehörigen Dateien zu sichern.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Sichern von Zertifikatdiensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeeb0881d517de538971d7eafb835ec48f3f33328e3a026b450e6719bfb23ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773086"
---
# <a name="backing-up-certificate-services"></a>Sichern von Zertifikatdiensten

Das folgende Szenario zeigt, wie Sie die Sicherungsfunktionen der Zertifikatdienste verwenden können, um eine Zertifikatdienste-Datenbank und die zugehörigen Dateien zu sichern.

1.  Laden Sie Certadm.dll Bibliothek in den Arbeitsspeicher (durch Aufrufen [**von LoadLibrary).**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
2.  Rufen Sie die Adresse jeder der erforderlichen Funktionen in Certadm.dll (mit [**getProcAddress) ab.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Verwenden Sie diese Adressen, wenn Sie die Funktionen in den verbleibenden Schritten aufrufen.
3.  Rufen [**Sie CertSrvIsServerOnline auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) um zu ermitteln, ob die Zertifikatdienste online sind. Zertifikatdienste müssen online sein, damit die Sicherungsvorgänge erfolgreich sind.
4.  Rufen [**Sie CertSrvBackupPrepare auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) um eine Sicherungssitzung zu starten. Das resultierende Zertifikatdienst-Sicherungskontexthand handle wird von vielen der anderen Sicherungsfunktionen verwendet.
5.  Rufen [**Sie CertSrvRestoreGetDatabaseLocations auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) um die Wiederherstellungszuordnung zu bestimmen. Die Wiederherstellungszuordnung enthält die Pfade, die beim Wiederherstellen der Sicherung verwendet werden sollen. Speichern Sie die von **CertSrvRestoreGetDatabaseLocations** abgerufenen Informationen an einem anwendungsspezifischen Speicherort.
6.  Rufen [**Sie CertSrvBackupGetDatabaseNames auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) um die Namen der zu sichernden Datenbankdateien zu bestimmen. Führen Sie für jede dieser Dateien die Schritte 7 bis 9 aus.
7.  Rufen [**Sie CertSrvBackupOpenFile auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) um die Datei für die Sicherung zu öffnen.
8.  Rufen [**Sie CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) auf, um einen Teil der Bytes aus der Datei zu lesen, und rufen Sie dann eine anwendungsspezifische Routine auf, um die Bytes auf einem Sicherungsmedium zu speichern. Wiederholen Sie diesen Schritt, bis alle Bytes in der Datei sichern.
9.  Rufen [**Sie CertSrvBackupClose auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) um die Datei zu schließen.
10. Rufen [**Sie CertSrvBackupGetBackupLogs auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) um die Namen der zu sichernden Protokolldateien zu bestimmen. Führen Sie für jede dieser Dateien die Schritte 7 bis 9 aus.
11. Rufen [**Sie CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) auf, um die Protokolldateien zu abschneiden, die in den Schritten 6 und 10 sichern wurden. Dieser Schritt ist optional. Rufen Sie **jedoch nur dann CertSrvBackupTruncateLogs** auf, wenn alle dateien, die von [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) und [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) zurückgegeben wurden, sicherungsgesichert wurden (andernfalls ist der Wiederherstellungsvorgang nicht durchgeführt). Weitere Informationen finden Sie auf der Referenzseite zu **CertSrvBackupTruncateLogs.**
12. Rufen [**Sie CertSrvBackupGetDynamicFileList auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) um die Namen der zu sichernden Nicht-Datenbankdateien zu bestimmen. Diese Dateien werden nur von der -Funktion identifiziert und müssen auf andere Wege sichern werden.
13. Sichern Sie die in Schritt 12 identifizierten dynamischen Dateien mithilfe von Routinen, die von den Certadm.dll.
14. Rufen [**Sie CertSrvBackupEnd auf,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) um die Sicherungssitzung zu beenden.
15. Rufen [**Sie bei Bedarf CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) auf, um Puffer frei zu geben, die von bestimmten Sicherungsfunktionen der Zertifikatdienste zugeordnet werden. Aufrufe von [**CertSrvBackupGetBackupLogs,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)und [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) weisen Puffer zu, die durch einen Aufruf von **CertSrvBackupFree** frei werden können.
16. Geben Sie die Certadm.dll ressourcen frei, indem [**Sie FreeLibrary aufrufen.**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)

Informationen zu den Berechtigungen, die zum Sichern der Zertifikatdienste-Datenbank und der zugehörigen Dateien erforderlich sind, finden Sie unter Festlegen der Sicherungs- [und Wiederherstellungsberechtigungen.](setting-the-backup-and-restore-privileges.md)

 

 
