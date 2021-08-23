---
description: 'Die folgenden VSS-Fehler- und -Statusinformationen werden in das Anwendungsereignisprotokoll geschrieben:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: VSS-Fehlerprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c2743fc6c23458a1059287a7731777e92447e3cd57ebf52e40baf7619c5658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056228"
---
# <a name="vss-error-logging"></a>VSS-Fehlerprotokollierung

Die folgenden VSS-Fehler- und -Statusinformationen werden in das Anwendungsereignisprotokoll geschrieben:

-   Fehler der Anfordernden, die mithilfe der [**IVssBackupComponents-Schnittstelle erzeugt**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) wurden
-   Schreiben von Fehlern, die in mithilfe der [**CVssWriter-Klasse**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) erzeugt werden, einschließlich überschreibende Methoden
-   Vom Standardanbieter generierte Fehler
-   VSS-Dienstfehler, die bei der Koordination von Anbieter-, Writer- und Anforderungsaktivität generiert werden (z. B. die Generierung von Ereignissen)

Diese Fehler können eine Reihe von Ursachen haben, z. B. einen Programmierfehler in Drittanbietercode oder VSS-bezogene Konfigurationsfehler.

VSS-Treiber und Implementierungsfunktionen auf niedrigerer Ebene schreiben Fehler in das Systemprotokoll. Drittanbietersoftware (Anfordernde, Anbieter, Writer) kann das Anwendungsprotokoll, das Systemprotokoll oder beides auswählen, um Fehlerprotokolleinträge zu schreiben.

Es wird empfohlen, dass Anwendungen auf hoher Ebene (z. B. Benutzermoduscode) das Anwendungsprotokoll verwenden. Anwendungen auf niedrigerer Ebene, z. B. Hardwareschnittstellen und Treiber, sollten das Systemprotokoll verwenden.

 

 



