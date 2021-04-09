---
description: Verwenden der Sicherungsfunktionen für Zertifikat Dienste zum Sichern einer Zertifikat Dienst Datenbank und der zugehörigen Dateien.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Sichern von Zertifikat Diensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1be929fcf3bd9b8b9655b48758a97d19af7abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868807"
---
# <a name="backing-up-certificate-services"></a>Sichern von Zertifikat Diensten

Im folgenden Szenario wird veranschaulicht, wie Sie die Sicherungsfunktionen der Zertifikat Dienste verwenden können, um eine Zertifikat Dienst-Datenbank und die zugehörigen Dateien zu sichern.

1.  Laden Sie die Certadm.dll Bibliothek in den Arbeitsspeicher (durch Aufrufen von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Rufen Sie die Adresse der einzelnen erforderlichen Funktionen in Certadm.dll (über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)) ab. Verwenden Sie diese Adressen, wenn Sie die Funktionen in den verbleibenden Schritten aufrufen.
3.  Wenden Sie [**cerzrvisserveronline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) an, um zu bestimmen, ob die Zertifikat Dienste online sind. Die Zertifikat Dienste müssen online sein, damit die Sicherungs Vorgänge erfolgreich ausgeführt werden.
4.  Nennen Sie [**cerzrvbackupprepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) , um eine Sicherungs Sitzung zu starten. Das resultierende Sicherungs Kontext Handle der Zertifikat Dienste wird von vielen der anderen Sicherungsfunktionen verwendet.
5.  Nennen Sie [**cerzrvrestoregetdatabaselocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) , um die Wiederherstellungs Zuordnung zu bestimmen. Die Restore Map enthält die Pfade, die beim Wiederherstellen der Sicherung verwendet werden sollen. Speichern Sie die von " **certsrvrestoregetdatabaselocations** " abgerufenen Informationen an einem anwendungsspezifischen Speicherort.
6.  Nennen Sie [**cerzrvbackupgetdatabasenames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) , um die Namen der zu sichernden Datenbankdateien zu bestimmen. Führen Sie für jede dieser Dateien die Schritte 7 bis 9 aus.
7.  Nennen Sie [**cerzrvbackupopenfile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) , um die Datei für die Sicherung zu öffnen.
8.  Rufen Sie [**cerzrvbackupread**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) auf, um einen Teil der Bytes aus der Datei zu lesen, und rufen Sie dann eine anwendungsspezifische Routine auf, um die Bytes auf einem Sicherungsmedium zu speichern. Wiederholen Sie diesen Schritt, bis alle Bytes in der Datei gesichert wurden.
9.  Nennen Sie [**cerzrvbackupclose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) , um die Datei zu schließen.
10. Nennen Sie [**cergs rvbackupgetbackuplogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) , um die Namen der zu sichernden Protokolldateien zu bestimmen. Führen Sie für jede dieser Dateien die Schritte 7 bis 9 aus.
11. Nennen Sie [**cergs rvbackuptrunkatelogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) , um die in den Schritten 6 und 10 gesicherten Protokolldateien abzuschneiden. Dieser Schritt ist optional. Allerdings wird **certrvbackuptrunerelogs** nur aufgerufen, wenn alle von [**certrvbackupgetdatabasenames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) und [**certrvbackupgetbackuplogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) zurückgegebenen Dateien gesichert wurden (andernfalls schlägt der Wiederherstellungs Vorgang fehl). Weitere Informationen finden Sie auf der Referenzseite zu **certrvbackuptruneurelogs** .
12. Nennen Sie [**cerzrvbackupgetdynamicfilelist**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) , um die Namen der zu sichernden nicht-Datenbankdateien zu bestimmen. Diese Dateien werden nur von der-Funktion identifiziert und müssen auf andere Weise gesichert werden.
13. Sichern Sie die in Schritt 12 identifizierten dynamischen Dateien mithilfe von Routinen, die von Certadm.dll getrennt sind.
14. Nennen Sie [**cerzrvbackupend**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) , um die Sicherungs Sitzung zu beenden.
15. Nennen Sie [**cerzrvbackupfree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) nach Bedarf, um Puffer freizugeben, die von bestimmten Sicherungsfunktionen für Zertifikat Dienste zugeordnet werden. Aufrufe von " [**cerzrvbackupgetbackuplogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)", " [**cerzrvbackupgetdatabasenames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)" und " [**cerzrvbackupgetdynamicfilelist**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) " weisen Puffer zu, die durch einen Aufruf von " **cerzrvbackupfree**" freigegeben werden können.
16. Geben Sie die Certadm.dll Ressourcen frei, indem Sie [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)aufrufen.

Informationen zu den Berechtigungen, die zum Sichern der Zertifikat Dienst Datenbank und der zugehörigen Dateien erforderlich sind, finden Sie unter [Festlegen der Sicherungs-und Wiederherstellungs Berechtigungen](setting-the-backup-and-restore-privileges.md).

 

 
