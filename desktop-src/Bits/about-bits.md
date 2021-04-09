---
title: Informationen zu BITS
description: Verwenden Sie Background Intelligent Transfer Service (Bits), um Dateien asynchron zwischen einem Client und einem Server zu übertragen.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Background Intelligent Transfer Service, beschrieben
- Übertragungs Warteschlangen Bits
- Übertragungs Warteschlangen Bits, Drosselung
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b1ac0f587b496692ec1c2e62be06c0e64766a205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101719"
---
# <a name="about-bits"></a>Informationen zu BITS

Verwenden Sie Background Intelligent Transfer Service (Bits) zum Herunterladen von Dateien aus oder zum Hochladen von Dateien auf HTTP-Webserver oder SMB-Dateiserver. 

Bits überträgt weiterhin Dateien, nachdem eine Anwendung beendet wurde, solange der Benutzer, der die Übertragung initiiert hat, angemeldet bleibt und eine Netzwerkverbindung aufrechterhalten wird. Eine Netzwerkverbindung wird von Bits nicht erzwungen. Bits nimmt die Übertragungen wieder auf, nachdem eine Netzwerkverbindung, die verloren gegangen ist, wieder hergestellt wird oder nachdem ein Benutzer sich wieder angemeldet hat. Weitere Informationen finden Sie unter [Benutzer und Netzwerkverbindungen](users-and-network-connections.md).

Bits achtet auf die aktuellen Netzwerkkosten und-Überlastung, sodass ein Hintergrund Auftrag so wenig wie möglich mit der Vordergrund-Benutzererfahrung des Benutzers beeinträchtigt. Bits verwendet die [Netzwerkbandbreite](network-bandwidth.md) im Leerlauf, um die Dateien zu übertragen, und erhöht oder verringert die Rate, mit der Dateien übertragen werden, basierend auf der verfügbaren Netzwerkbandbreite im Leerlauf. Sobald von einer Netzwerkanwendung mehr Bandbreite genutzt wird, wird die Übertragungsrate von BITS verringert, sodass der Benutzer weiterhin interagieren kann. Bits verwendet von der APP angegebene [Übertragungs Richtlinien](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) , um zu verhindern, dass Dateien über bei Network-Verbindungen übertragen werden.

Bits berücksichtigt auch den Energieverbrauch. Beginnend mit dem Windows 10-Update von Mai 2019 überträgt Bits Dateien, wenn sich der Computer im [modernen](/windows-hardware/design/device-experiences/modern-standby) Standbymodus befindet und der Computer angeschlossen ist.

Die Bits-Anwendung kann die verschiedenen Bits- [Prioritätsstufen](/windows/desktop/api/Bits/ne-bits-bg_job_priority) verwenden, um Bits Intelligent auszuwählen, welche Übertragungs Aufträge ausgeführt werden. Aufträge mit höherer Priorität werden vor Aufträgen mit niedrigerer Priorität ausgeführt. Für Aufträge mit gleicher Prioritätsstufe wird die Übertragungszeit aufgeteilt, wodurch verhindert wird, dass ein großer Auftrag kleine Aufträge in der Übertragungswarteschlange blockiert. Aufträgen mit niedrigerer Priorität wird erst dann Übertragungszeit zugewiesen, wenn alle Aufträge mit höherer Priorität abgeschlossen wurden oder wenn bei diesen ein Fehler aufgetreten ist.

Bits verwendet Windows BranchCache für das Peer Caching. Weitere Informationen finden Sie unter [BranchCache: Übersicht](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

Universelle Windows-Plattform (UWP)-Entwickler sollten die [Windows. Networking. backgroundtransfer](/uwp/api/Windows.Networking.BackgroundTransfer) -API und nicht die Bits-API verwenden.

Es gibt drei Arten von [**Übertragungs Aufträgen**](/windows/desktop/api/Bits/ne-bits-bg_job_type). Bei einem Download Auftrag werden Dateien auf den Client heruntergeladen, bei einem Uploadauftrag wird eine Datei auf den Server hochgeladen, und bei einem Upload-Antwort-Auftrag wird eine Datei auf den Server hochgeladen und eine Antwortdatei von der Serveranwendung empfangen.

Die folgenden Themen enthalten ausführlichere Informationen zu Bits:

-   [Authentifizierung](authentication.md)
-   [Lebenszyklus eines Bits-Auftrags](life-cycle-of-a-bits-job.md)
-   [Benutzer und Netzwerkverbindungen](users-and-network-connections.md)
-   [Netzwerkbandbreite](network-bandwidth.md)
-   [Gruppenrichtlinien](group-policies.md)
-   [Dienst Konten und Bits](service-accounts-and-bits.md)
-   [Hilfstoken für Bits-Übertragungs Aufträge](helper-tokens-for-bits-transfer-jobs.md)
-   [Datei Übertragungs Konsistenz](file-transfer-consistency.md)
-   [HTTP-Anforderungen für Bits-Downloads](http-requirements-for-bits-downloads.md)
-   [IIS-Anforderungen für BITS-Uploads](iis-requirements-for-bits-uploads.md)
-   [Cleanup des virtuellen Verzeichnisses](virtual-directory-cleanup.md)
-   [Bits und System Wiederherstellung](bits-and-system-restore.md)
-   [Bits-Starttyp](bits-startup-type.md)
-   [Gemeinsame Nutzung der Internetverbindung](internet-connection-sharing.md)
-   [Peer Caching](peer-caching.md)
-   [Bits-Sicherheit,-Token und-Administrator Konten](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

Verwenden Sie die Bits- [Schnittstellen](bits-interfaces.md) zum Schreiben von Anwendungen, die Übertragungs Aufträge erstellen und überwachen. Ausführliche Informationen zur Verwendung der Bits-Schnittstellen finden Sie unter [Verwenden von Bits](using-bits.md).