---
title: Informationen zu BITS
description: Verwenden Sie Background Intelligent Transfer Service (BITS), um Dateien asynchron zwischen einem Client und einem Server zu übertragen.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Background Intelligent Transfer Service beschrieben
- BITS der Übertragungswarteschlange
- Übertragungswarteschlange BITS , Drosselung
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 53693b7087d647e8d6e89a8c81e09895dc3866b964642475466bbf8f52ddbae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529280"
---
# <a name="about-bits"></a>Informationen zu BITS

Verwenden Sie Background Intelligent Transfer Service (BITS), um Dateien von HTTP-Webservern oder SMB-Dateiservern herunterzuladen oder auf diese hochzuladen. 

BITS überträgt dateien weiterhin, nachdem eine Anwendung beendet wurde, solange der Benutzer, der die Übertragung initiiert hat, angemeldet bleibt und eine Netzwerkverbindung beibehalten wird. Bits erzwingen keine Netzwerkverbindung. BITS setzt Übertragungen fort, nachdem eine verloren gegangene Netzwerkverbindung wiederhergestellt wurde oder nachdem sich ein Benutzer, der sich abgemeldet hat, wieder angemeldet hat. Weitere Informationen finden Sie unter [Benutzer und Netzwerkverbindungen.](users-and-network-connections.md)

BITS beachtet die aktuellen Netzwerkkosten und Überlastungen, sodass ein Hintergrundauftrag die Vordergrunderfahrung des Benutzers so wenig wie möglich beeinträchtigt. BITS verwendet [die Netzwerkbandbreite](network-bandwidth.md) im Leerlauf, um die Dateien zu übertragen, und erhöht oder verringert die Rate, mit der Dateien basierend auf der verfügbaren Netzwerkbandbreite im Leerlauf übertragen werden. Sobald von einer Netzwerkanwendung mehr Bandbreite genutzt wird, wird die Übertragungsrate von BITS verringert, sodass der Benutzer weiterhin interagieren kann. BITS verwendet von der App angegebene [Übertragungsrichtlinien,](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) um zu verhindern, dass Dateien auf kostenintensive Netzwerkverbindungen übertragen werden.

BITS ist auch auf die Energieverbrauchsnutzung achten. Ab dem Windows 10 May 2019 Update überträgt BITS Dateien, wenn sich der Computer im [modernen Standbymodus](/windows-hardware/design/device-experiences/modern-standby) befindet und der Computer angeschlossen ist.

Die BITS-Anwendung kann die verschiedenen [BITS-Prioritätsebenen](/windows/desktop/api/Bits/ne-bits-bg_job_priority) verwenden, damit BITS intelligent auswählen kann, welche Übertragungsaufträge ausgeführt werden sollen. Aufträge mit höherer Priorität werden vor Aufträgen mit niedrigerer Priorität ausgeführt. Für Aufträge mit gleicher Prioritätsstufe wird die Übertragungszeit aufgeteilt, wodurch verhindert wird, dass ein großer Auftrag kleine Aufträge in der Übertragungswarteschlange blockiert. Aufträgen mit niedrigerer Priorität wird erst dann Übertragungszeit zugewiesen, wenn alle Aufträge mit höherer Priorität abgeschlossen wurden oder wenn bei diesen ein Fehler aufgetreten ist.

BITS verwendet Windows BranchCache für die Peerzwischenspeicherung. Weitere Informationen finden Sie in der [BranchCache-Übersicht.](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10))

UWP-Entwickler (Universal Windows Platform) sollten die [Windows verwenden. Networking.BackgroundTransfer-API](/uwp/api/Windows.Networking.BackgroundTransfer) und nicht die BITS-API.

Es gibt drei Arten von [**Übertragungsaufträgen.**](/windows/desktop/api/Bits/ne-bits-bg_job_type) Ein Downloadauftrag lädt Dateien auf den Client herunter, ein Uploadauftrag lädt eine Datei auf den Server hoch, und ein Upload-Antwort-Auftrag lädt eine Datei auf den Server hoch und empfängt eine Antwortdatei von der Serveranwendung.

Die folgenden Themen enthalten ausführlichere Informationen zu BITS:

-   [Authentifizierung](authentication.md)
-   [Lebenszyklus eines BITS-Auftrags](life-cycle-of-a-bits-job.md)
-   [Benutzer und Netzwerkverbindungen](users-and-network-connections.md)
-   [Netzwerkbandbreite](network-bandwidth.md)
-   [Gruppenrichtlinien](group-policies.md)
-   [Dienstkonten und BITS](service-accounts-and-bits.md)
-   [Hilfstoken für BITS-Übertragungsaufträge](helper-tokens-for-bits-transfer-jobs.md)
-   [Dateiübertragungskonsistenz](file-transfer-consistency.md)
-   [HTTP-Anforderungen für BITS-Downloads](http-requirements-for-bits-downloads.md)
-   [IIS-Anforderungen für BITS-Uploads](iis-requirements-for-bits-uploads.md)
-   [Bereinigung virtueller Verzeichnisse](virtual-directory-cleanup.md)
-   [BITS und Systemwiederherstellung](bits-and-system-restore.md)
-   [BITS-Starttyp](bits-startup-type.md)
-   [Gemeinsame Nutzung der Internetverbindung](internet-connection-sharing.md)
-   [Peerzwischenspeicherung](peer-caching.md)
-   [BITS-Sicherheit, Token und Administratorkonten](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

Verwenden Sie die [BITS-Schnittstellen,](bits-interfaces.md) um Anwendungen zu schreiben, die Übertragungsaufträge erstellen und überwachen. Ausführliche Informationen zur Verwendung der BITS-Schnittstellen finden Sie unter [Verwenden von BITS.](using-bits.md)