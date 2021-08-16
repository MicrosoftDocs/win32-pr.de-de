---
description: Zeigt, wie die Sicherungsfunktionen der Zertifikatdienste verwendet werden können, um eine Zertifikatdienst-Datenbank und die zugehörigen Dateien wiederherzustellen.
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: Wiederherstellen von Zertifikatdiensten aus einer Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665a1aed873cdf25f24dc5a7bc8b8466a5c3ae7a6c1aaf6bec07d2e8be336e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900523"
---
# <a name="restoring-certificate-services-from-backup"></a>Wiederherstellen von Zertifikatdiensten aus einer Sicherung

Das folgende Szenario zeigt, wie die Sicherungsfunktionen der Zertifikatdienste verwendet werden können, um eine Zertifikatdienst-Datenbank und die zugehörigen Dateien wiederherzustellen und wiederherzustellen. Der Wiederherstellungsvorgang umfasst das Schreiben der in einem Sicherungssatz enthaltenen Dateien auf den Datenträger. Sie können mehrere Sicherungssätze wiederherstellen (eine vollständige Sicherung plus null oder mehr inkrementelle Sicherungen), aber alle Wiederherstellungen müssen abgeschlossen sein, bevor Sie mit dem Wiederherstellungsprozess beginnen. Der Wiederherstellungsprozess umfasst die Wiedergabe von Protokolldateien durch die Zertifikatdienste, um die Datenbank- und Protokolldateikonsistenz sicherzustellen und so die Datenbankintegrität sicherzustellen. Das Szenario veranschaulicht die Funktionsaufrufe zum Wiederherstellen der Sicherungssätze und informieren die Zertifikatdienste über die Wiederherstellungsparameter.

Vor der Implementierung dieses Szenarios muss eine vollständige Sicherung der Zertifikatdienste-Datenbank vorhanden sein.

1.  Laden Sie die Certadm.dll-Bibliothek in den Arbeitsspeicher (durch Aufrufen von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Rufen Sie die Adresse jeder der erforderlichen Funktionen in Certadm.dll ab (über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Verwenden Sie diese Adressen, wenn Sie die Funktionen in den verbleibenden Schritten aufrufen.
3.  Rufen Sie [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) auf, um zu bestimmen, ob die Zertifikatdienste online sind. Wenn Die Zertifikatdienste ausgeführt werden, fahren Sie sie herunter, bevor Sie fortfahren. Zertifikatdienste dürfen nicht online sein, damit die Wiederherstellungsvorgänge erfolgreich sind.
4.  Rufen Sie [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) auf, um eine Wiederherstellungssitzung zu starten. Das resultierende Sicherungskontexthandle der Zertifikatdienste wird von mehreren anderen Funktionen verwendet.
5.  Bestimmen Sie den Pfad für den Datenbankspeicherort. Während eines Sicherungsszenarios wäre dieser Wert über einen Aufruf von [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw)verfügbar gewesen. Dieser Wert sollte als Teil der Sicherung gespeichert worden sein.
6.  Erstellen Sie eine Wiederherstellungszuordnung, die den Namen der wiederhergestellten Datenbank angibt. Eine Wiederherstellungszuordnungsstruktur für die Zertifikatdienste-Datenbank (CSEDB \_ RSTMAPW) wird verwendet, um eine Wiederherstellungszuordnung anzugeben. Legen Sie das \_ **PwszDatabaseName-Element** des CSEDB RSTMAPW und das \_ **pwszNewDatabaseName-Element** des CSEDB RSTMAPW auf den in Schritt 5 ermittelten Datenbankspeicherort fest. Wenn die wiederhergestellte Datenbank einen anderen Namen als die Sicherungsdatenbank haben soll, legen Sie optional das \_ **PwszNewDatabaseName-Element** des CSEDB RSTMAPW auf den neuen Datenbanknamen fest.
7.  Wenn Sie sicherstellen möchten, dass Änderungen an der Datenbank, die nach der Sicherung vorgenommen wurden, nach Abschluss der Datenbankwiederherstellung nicht erneut angewendet werden (im Rahmen der Datenbankwiederherstellung, die beim nächsten Start der Zertifikatdienste durchgeführt wird), löschen Sie Dateien aus den aktiven Datenbank- und Protokollverzeichnissen des Zielservers.
8.  Kopieren Sie die in der vollständigen Sicherung enthaltenen Dateien in die aktiven Datenbank- und Protokollverzeichnisse des Zielservers.
9.  Rufen Sie [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) auf, um einen Wiederherstellungsvorgang für die vollständige Sicherung zu registrieren. **CertSrvRestoreRegister** verwendet die in Schritt 6 angegebene Wiederherstellungszuordnung. **CertSrvRestoreRegister** gibt auch den Speicherort der Sicherungsdatenbank und der Protokolle an. Der Aufruf von **CertSrvRestoreRegister** zwingt die Zertifikatdienste, beim nächsten Start einen Wiederherstellungsvorgang zu versuchen. Außerdem wird verhindert, dass Zertifikatanforderungen von Zertifikatdiensten verarbeitet werden, bis die Wiederherstellung abgeschlossen ist.
10. Rufen Sie [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)auf, und beenden Sie dadurch die Registrierungsaktivität, die in Schritt 8 gestartet wurde. Beachten Sie, dass die Registrierung eines Wiederherstellungsvorgangs eine Anweisung für Zertifikatdienste ist, die beim Starten befolgt werden soll. Die tatsächliche Wiederherstellung erfolgt erst, nachdem die Zertifikatdienste gestartet wurden.
11. Kopieren Sie für jede wiederherzustellende inkrementelle Sicherung die in der inkrementellen Sicherung enthaltenen Dateien in das aktive Protokollverzeichnis des Zielservers, und rufen Sie dann [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)auf, gefolgt von einem Aufruf von [**CertSrvRestoreRegisterComplete.**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete) Die Registrierung der inkrementellen Sicherungen für die Wiederherstellung kann in beliebiger Reihenfolge erfolgen, aber nur der Satz von Dateien für eine inkrementelle Sicherung sollte vor jedem Aufruf von **CertSrvRestoreRegister** auf den Server kopiert werden.
12. Kopieren Sie die dynamischen Zertifikatdienste-Dateien auf den Zielserver. Die dynamischen Dateien wurden während der Sicherung identifiziert, als [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) aufgerufen wurde. Möglicherweise muss der World Wide Web-Veröffentlichungsdienst beendet werden, um das Überschreiben der dynamischen Dateien zu ermöglichen.
13. Rufen Sie [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) auf, um die Wiederherstellungssitzung zu beenden.
14. Starten Sie die Zertifikatdienste-Anwendung manuell (oder warten Sie bis zum nächsten Neustart, bis sie automatisch gestartet wird). Beim Start der Zertifikatdienste wird ermittelt, ob ein Wiederherstellungsvorgang registriert wurde. Wenn ein Wiederherstellungsvorgang registriert wurde, wird die Wiederherstellung von den Zertifikatdiensten gestartet. Zertifikatdienste verarbeiten keine Zertifikatanforderungen, bis der Wiederherstellungsvorgang abgeschlossen ist.

> [!Note]  
> Wenn eine Wiederherstellung abgeschlossen ist, ist es wichtig, dass Sie eine neue vollständige Sicherung der Zertifikatdienste-Datenbank erstellen. Dies ist erforderlich, um die wiederhergestellten Protokolldateien abzuschneiden und einen Basissicherungssatz für zukünftige Wiederherstellungen einzurichten. Sicherungen, die nach einer Wiederherstellung ausgeführt werden, können nicht mit Sicherungen (vollständig oder inkrementell) kombiniert werden, die vor der Wiederherstellung erstellt wurden. Das heißt, nachdem eine Zertifikatdienstdatenbank wiederhergestellt wurde und in einen nachfolgenden Zustand übergegangen ist, können Sie die Sicherungen vor der Wiederherstellung nicht verwenden, um die Datenbank in diesem nachfolgenden Zustand wiederherzustellen.

 

 

 
