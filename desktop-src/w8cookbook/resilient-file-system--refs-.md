---
title: Robustes Dateisystem
description: Robustes Dateisystem
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2938f99e232f37d6f36f575c6c2a419adf3b6dbdc2a06bd9c8e243d6ba4884
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882680"
---
# <a name="resilient-file-system"></a>Robustes Dateisystem

## <a name="platform"></a>Plattform

**Server** – Windows Server 2012 

## <a name="description"></a>BESCHREIBUNG

Resilient File System (ReFS) ist ein neues lokales Dateisystem. Die Datenverfügbarkeit wird trotz Fehlern maximiert, die in der Vergangenheit zu Datenverlusten oder Ausfallzeiten führen würden. Die Datenintegrität stellt sicher, dass unternehmenskritische Daten vor Fehlern geschützt und bei Bedarf verfügbar sind. Die Architektur ist darauf ausgelegt, Skalierbarkeit und Leistung in einer Zeit mit ständig wachsenden Datenmengen und dynamischen Workloads bereitzustellen.

Die wichtigsten Features von ReFS sind:

-   **Integrität:** ReFS speichert Daten, sodass sie vor vielen häufigen Fehlern geschützt sind, die zu Datenverlusten führen können. Dateisystemmetadaten sind immer geschützt. Optional können Benutzerdaten pro Volume, pro Verzeichnis oder pro Datei geschützt werden. Wenn eine Beschädigung auftritt, kann ReFS die Beschädigung erkennen und bei der Konfiguration mit Speicherplätze automatisch korrigieren. Im Fall eines Systemfehlers ist ReFS so konzipiert, dass die Wiederherstellung nach diesem Fehler schnell ohne Verlust von Benutzerdaten erfolgt.
-   **Verfügbarkeit:** ReFS wurde entwickelt, um die Verfügbarkeit von Daten zu priorisieren. Wenn bei ReFS eine Beschädigung auftritt und sie nicht automatisch repariert werden kann, wird der Online-Wiederherstellungsprozess in den Bereich der Beschädigung lokalisiert, sodass kein Volumeausfall erforderlich ist. Kurz gesagt: Wenn eine Beschädigung auftritt, bleibt ReFS online.
-   **Skalierbarkeit:** ReFS ist für die Heutigen Und-Datentypen von heute und die Größen von Datasets von morgen konzipiert. Sie ist für hohe Skalierbarkeit optimiert.
-   **App-Kompatibilität:** Um AppCompat zu maximieren, unterstützt ReFS eine Teilmenge der NTFS-Features sowie Win32-APIs, die weit verbreitet sind.
-   **Proaktive Fehleridentifikation:** Die Integritätsfunktionen von ReFS werden von einem Datenintegritätsscanner (einem "Bereinigungsvorgang") genutzt, der regelmäßig das Volume überprüft, versucht, latente Beschädigungen zu identifizieren und dann proaktiv eine Reparatur dieser beschädigten Daten auslöst.

## <a name="resources"></a>Ressourcen

-   [Building Windows 8 Blog Post – Building the next generation file system for Windows: ReFS (Erstellen des Dateisystems der nächsten Generation für Windows: ReFS)](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [Anwendungskompatibilität und ReFS](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 