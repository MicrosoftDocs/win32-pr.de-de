---
description: Zeigt, wie die Sicherungsfunktionen der Zertifikat Dienste zum Wiederherstellen einer Zertifikat Dienst Datenbank und der zugehörigen Dateien verwendet werden können.
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: Zertifikat Dienste werden von der Sicherung wieder hergestellt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f5adf46d802194909397a3b70483b3cf43bb409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351516"
---
# <a name="restoring-certificate-services-from-backup"></a>Zertifikat Dienste werden von der Sicherung wieder hergestellt

Das folgende Szenario zeigt, wie die Sicherungsfunktionen der Zertifikat Dienste zum Wiederherstellen einer Zertifikat Dienst Datenbank und der zugehörigen Dateien verwendet werden können. Der Wiederherstellungs Vorgang umfasst das Schreiben der in einem Sicherungs Satz enthaltenen Dateien auf den Datenträger. Sie können mehrere Sicherungs Sätze wiederherstellen (eine vollständige Sicherung plus null oder mehr inkrementelle Sicherungen), aber alle Wiederherstellungen müssen vor Beginn des Wiederherstellungs Vorgangs vollständig ausgeführt werden. Der Wiederherstellungsprozess umfasst Zertifikat Dienste, die Protokolldateien wiedergeben, um die Konsistenz der Datenbank und der Protokolldateien sicherzustellen Das Szenario veranschaulicht die Funktionsaufrufe zum Wiederherstellen der Sicherungs Sätze und zum Benachrichtigen der Zertifikat Dienste der Wiederherstellungs Parameter.

Vor der Implementierung dieses Szenarios muss eine vorhandene vollständige Sicherung der Zertifikat Dienst Datenbank vorhanden sein.

1.  Laden Sie die Certadm.dll Bibliothek in den Arbeitsspeicher (durch Aufrufen von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Rufen Sie die Adresse der einzelnen erforderlichen Funktionen in Certadm.dll (über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)) ab. Verwenden Sie diese Adressen, wenn Sie die Funktionen in den verbleibenden Schritten aufrufen.
3.  Wenden Sie [**cerzrvisserveronline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) an, um zu bestimmen, ob die Zertifikat Dienste online sind. Wenn die Zertifikat Dienste ausgeführt werden, fahren Sie Sie herunter, bevor Sie fortfahren. Die Zertifikat Dienste dürfen nicht online sein, damit die Wiederherstellungs Vorgänge erfolgreich ausgeführt werden.
4.  Nennen Sie [**cerzrvrestoreprepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) , um eine Wiederherstellungs Sitzung zu starten. Das resultierende Sicherungs Kontext Handle der Zertifikat Dienste wird von mehreren der anderen Funktionen verwendet.
5.  Bestimmen Sie den Pfad für den Speicherort der Datenbank. Während eines Sicherungs Szenarios wäre dieser Wert über einen Befehl von " [**cerzrvrestoregetdatabaselocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw)" verfügbar. Dieser Wert sollte als Teil der Sicherung gespeichert worden sein.
6.  Erstellen Sie eine Wiederherstellungs Zuordnung, die den Namen der wiederhergestellten Datenbank angibt. Eine mapremap-Struktur für die Daten Bank Wiederherstellung ( \_ ccrstmapw) für Zertifikat Dienste wird zum Angeben einer Wiederherstellungs Zuordnung verwendet. Legen \_ Sie das **pwszdatabasename** -Element von csedb rstmapw und das \_ **pwsznewdatabasename** -Element von csedb rstmapw auf den Daten Bank Speicherort fest, der in Schritt 5 festgelegt wurde. Wenn die wiederhergestellte Datenbank einen anderen Namen als die Sicherungs Datenbank aufweisen soll, legen \_ Sie den **pwsznewdatabasename** -Member der csedb-rstmapw auf den neuen Datenbanknamen fest.
7.  Wenn Sie sicherstellen möchten, dass Änderungen, die nach dem Durchführen der Sicherung an der Datenbank vorgenommen wurden, nicht erneut angewendet werden, nachdem die Daten Bank Wiederherstellung durchgeführt wurde (als Teil der Daten Bank Wiederherstellung beim nächsten Starten der Zertifikat Dienste), löschen Sie Dateien aus der aktiven Datenbank und dem Protokoll Verzeichnis des Zielservers.
8.  Kopieren Sie die Dateien, die in der vollständigen Sicherung enthalten sind, in die aktive Datenbank und die Protokoll Verzeichnisse des Zielservers.
9.  Nennen Sie [**cerzrvrestoreregister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) , um einen Wiederherstellungs Vorgang für die vollständige Sicherung zu registrieren. **Cerzrvrestoreregiester** verwendet die in Schritt 6 angegebene Wiederherstellungs Zuordnung. **Certsrvrestoreregiester** gibt auch den Speicherort der Sicherungs Datenbank und der Protokolle an. Durch das Aufrufen von " **certrvrestoreregiester** " wird erzwungen, dass Zertifikat Dienste beim nächsten Start einen Wiederherstellungs Vorgang versuchen. Außerdem wird verhindert, dass Zertifikat Dienste Zertifikat Anforderungen verarbeiten, bis die Wiederherstellung beendet ist.
10. Nennen Sie [**cerzrvrestoreregistercomplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete), wodurch die in Schritt 8 gestartete Registrierungs Aktivität abgeschlossen wird. Beachten Sie, dass die Registrierung eines Wiederherstellungs Vorgangs eine Anweisung für die Zertifikat Dienste ist, die beim Start befolgt werden sollen. die tatsächliche Wiederherstellung wird erst ausgeführt, nachdem die Zertifikat Dienste gestartet wurden.
11. Kopieren Sie für jede wieder herzustellende inkrementelle Sicherung die Dateien, die in der inkrementellen Sicherung enthalten sind, in das aktive Protokoll Verzeichnis des Zielservers, und klicken Sie dann auf [](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete) [**cerzrvrestoreregistercomplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw). Die Registrierung der inkrementellen Sicherungen für die Wiederherstellung kann in beliebiger Reihenfolge erfolgen, aber nur der Satz von Dateien für eine inkrementelle Sicherung muss vor jedem Rückruf von **certsrvrestoreregiester** auf den Server kopiert werden.
12. Kopieren Sie die dynamischen Dateien der Zertifikat Dienste auf den Zielserver. Die dynamischen Dateien wurden während der Sicherung identifiziert, als " [**certrvbackupgetdynamicfilelist**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) " aufgerufen wurde. Möglicherweise ist es erforderlich, den World Wide Web Publishing-Dienstanbieter anzuhalten, damit die dynamischen Dateien überschrieben werden können.
13. Nennen Sie [**cerzrvrestoreend**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) , um die Wiederherstellungs Sitzung zu beenden.
14. Starten Sie die Zertifikat Dienst Anwendung manuell (oder warten Sie bis zum nächsten Neustart, damit Sie automatisch gestartet wird). Wenn die Zertifikat Dienste gestartet werden, wird festgestellt, ob ein Wiederherstellungs Vorgang registriert wurde. Wenn ein Wiederherstellungs Vorgang registriert wurde, wird die Wiederherstellung der Zertifikat Dienste gestartet. Zertifikat Dienste verarbeiten keine Zertifikat Anforderungen, bis der Wiederherstellungs Vorgang abgeschlossen ist.

> [!Note]  
> Wenn eine Wiederherstellung vollständig ist, ist es wichtig, dass Sie eine neue vollständige Sicherung der Zertifikat Dienst Datenbank erstellen. Dies ist erforderlich, um die wiederhergestellten Protokolldateien abzuschneiden und einen Basis Sicherungs Satz für zukünftige Wiederherstellungen einzurichten. Sicherungen, die nach einer Wiederherstellung ausgeführt werden, können nicht mit Sicherungen (vollständig oder inkrementell) gemischt werden Das heißt, nachdem eine Zertifikat Dienst Datenbank wieder hergestellt wurde und sich in einem nachfolgenden Zustand befindet, können Sie mit den Sicherungen vor der Wiederherstellung die Datenbank in diesem nachfolgenden Zustand wiederherstellen.

 

 

 
