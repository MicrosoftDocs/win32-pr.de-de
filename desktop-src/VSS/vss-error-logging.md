---
description: 'Die folgenden VSS-Fehler-und-Zustandsinformationen werden in das Anwendungs Ereignisprotokoll geschrieben:'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: VSS-Fehler Protokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129297"
---
# <a name="vss-error-logging"></a>VSS-Fehler Protokollierung

Die folgenden VSS-Fehler-und-Zustandsinformationen werden in das Anwendungs Ereignisprotokoll geschrieben:

-   Requestfehler, die mithilfe der [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Schnittstelle erzeugt wurden
-   Writer-Fehler, die in mithilfe der [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) -Klasse erzeugt werden
-   Vom Standardanbieter generierte Fehler
-   VSS-Dienst Fehler, die beim koordinieren der Anbieter-, Writer-und requestaktivität generiert wurden (z. b. die Generierung von Ereignissen)

Diese Fehler können eine Reihe von Gründen haben, einschließlich eines Programmierfehlers in Code von Drittanbietern oder von VSS-bezogenen Konfigurationsfehlern.

VSS-Treiber und Implementierungs Funktionen auf niedrigerer Ebene schreiben Fehler in das System Protokoll. Drittanbieter Software (requster, Anbieter, Writer) kann das Anwendungsprotokoll, das System Protokoll oder beides auswählen, um Fehlerprotokoll Einträge zu schreiben.

Es wird empfohlen, dass Anwendungen auf hoher Ebene (z. b. Code im Benutzermodus) das Anwendungsprotokoll verwenden. Anwendungen auf niedrigerer Ebene, z. b. Hardwareschnittstellen und Treiber, sollten das System Protokoll verwenden.

 

 



