---
title: Robustes Dateisystem
description: Robustes Dateisystem
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba011dcdd3cd39280e0a79d0b325f9e75d6b64
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104039785"
---
# <a name="resilient-file-system"></a>Robustes Dateisystem

## <a name="platform"></a>Plattform

**Server** – Windows Server 2012 

## <a name="description"></a>BESCHREIBUNG

Resilientes Dateisystem (Refs) ist ein neues lokales Dateisystem. Es maximiert die Datenverfügbarkeit, trotz der Fehler, die in der Vergangenheit zu Datenverlust oder Ausfallzeiten führen würden. Mit der Datenintegrität wird sichergestellt, dass geschäftskritische Daten vor Fehlern geschützt werden und bei Bedarf verfügbar sind. Die Architektur ist so konzipiert, dass Sie Skalierbarkeit und Leistung in einem Zeitraum von ständig wachsenden DataSet-Größen und dynamischen Workloads bietet.

Die wichtigsten Features von refs sind:

-   **Integrität**: Refs speichert Daten so, dass Sie vor vielen häufigen Fehlern geschützt werden, die zu Datenverlusten führen können. Dateisystem Metadaten sind immer geschützt. Optional können Benutzerdaten auf Volumen-, Verzeichnis-oder Datei Basis geschützt werden. Wenn eine Beschädigung auftritt, können Refs die Beschädigung erkennen und bei der Konfiguration mit Speicherplätzen automatisch korrigieren. Im Falle eines Systemfehlers ist Refs so konzipiert, dass dieser Fehler schnell wieder hergestellt werden kann, ohne dass Benutzerdaten verloren gehen.
-   **Verfügbarkeit**: Refs wurde entwickelt, um die Verfügbarkeit von Daten zu priorisieren. Wenn bei Refs eine Beschädigung auftritt und Sie nicht automatisch repariert werden kann, wird der Prozess der Online Rettung in den Bereich der Beschädigung lokalisiert, sodass keine Ausfallzeit des Volumes erforderlich ist. Kurz gesagt, wenn eine Beschädigung auftritt, bleiben Refs online.
-   **Skalierbarkeit**: Refs ist für die DataSet-Größen von heute und die DataSet-Größen von Morgen vorgesehen. Es ist für eine hohe Skalierbarkeit optimiert.
-   **APP-Kompatibilität**: um AppCompat zu maximieren, unterstützt Refs eine Teilmenge der NTFS-Features und Win32-APIs, die weitgehend übernommen werden.
-   **Proaktive Fehler Identifikation**: die Integritäts Funktionen von refs werden von einem Daten Integritäts Scanner ("Scrubber") genutzt, der regelmäßig das Volume scannt, versucht, eine latente Beschädigung zu erkennen, und löst dann proaktiv eine Reparatur dieser beschädigten Daten aus.

## <a name="resources"></a>Ressourcen

-   [Blog Beitrag zum Entwickeln von Windows 8 – entwickeln der nächsten Generation des Dateisystems für Windows: Refs](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [Anwendungs Kompatibilität und Refs](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 