---
description: Die Registrierungsgruppe Windows Installer-Tabellen enthält Informationen zu Registrierungseinträgen.
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: Registrierungstabellengruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7ab4d3447ec727271d53fabe44fee11bf96663170c89a2210d80bb02bd8c7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128975"
---
# <a name="registry-tables-group"></a>Registrierungstabellengruppe

![Registrierungstabellengruppe](images/registry.png)

Weitere Informationen zu diesem Diagramm finden Sie in der Legende des [Entitätsbeziehungsdiagramms.](entity-relationship-diagram-legend.md)

Das Installationsprogramm verfügt über bestimmte Tabellen für die verschiedenen Typen von Registrierungseinträgen. Beim Auffüllen der Registrierungstabellengruppe ist es wichtig, die Anzahl der Einträge in der [Registrierungstabelle](registry-table.md) zu minimieren und die Verwendung der anderen, spezifischen Registrierungstabellen zu maximieren. Dies liegt daran, dass das Installationsprogramm nicht zwischen verschiedenen Typen von Registrierungseinträgen in der Registrierungstabelle unterscheiden kann und nicht die interne Logik verwenden kann, die erforderlich ist, um alle Installerfunktionen wie die [*Ankündigung*](a-gly.md)von in vollem Umfang zu nutzen. Das Erstellen von COM- und Shell-bezogenen Registrierungseinträgen auf diese Weise bietet auch eine logischere Organisation und kann dazu beitragen, fehlerhafte Registrierungen von COM-Serverinformationen zu minimieren.

Die Abbildung zeigt die Registrierungseintragsgruppe von Tabellen sowie die [Komponententabelle](component-table.md), [Featuretabelle](feature-table.md)und [Dateitabelle](file-table.md). Obwohl letztere nicht direkt an der Auffüllung der Registrierung beteiligt sind, sind sie in der Abbildung enthalten, da sie für die Logik der Registrierungseintragsgruppe wichtig sind.

Die Registrierungseintragsgruppe enthält die folgenden Tabellen mit bestimmten Registrierungseinträgen.

-   Die [Tabelle Erweiterung](extension-table.md) enthält alle Dateinamenerweiterungen, die Ihre Anwendung verwendet, sowie die zugehörigen Features und Komponenten.
-   Die [Verb-Tabelle](verb-table.md) ordnet Befehlsverbinformationen den dateinamenerweiterungen zu, die in der [Erweiterungstabelle](extension-table.md)aufgeführt sind. Dies stellt einen indirekten Link zwischen der Verb- und Featuretabelle bereit, die für die Featureankündigung erforderlich ist.
-   Die [Tabelle TypeLib](typelib-table.md) enthält Informationen, die das Installationsprogramm in der Registrierung für die Registrierung von Typbibliotheken platziert. Typbibliothekseinträge werden zum Zeitpunkt der Ankündigung nicht geschrieben. Das Installationsprogramm schreibt die Typbibliothekseinträge zum Zeitpunkt der Installation der der Bibliothek zugeordneten Komponenten.
-   Die [MIME-Tabelle](mime-table.md) ordnet einen MIME-Kontexttyp einer CLSID oder einer Dateinamenerweiterung zu. Dies stellt einen Pfad zwischen MIME und Featuretabelle bereit, der für die Featureankündigung erforderlich ist.
-   Die [Tabelle SelfReg](selfreg-table.md) enthält Informationen, die für die Selbstregistrierung von Modulen erforderlich sind. Die Selbstregistrierung wird vom Installationsprogramm nur aus Gründen der Abwärtskompatibilität bereitgestellt und wird nicht als Methode zum Auffüllen der Registrierung empfohlen. Wenn es jedoch Module in Ihrer Anwendung gibt, die sich selbst registrieren müssen, verwenden Sie die SelfReg-Tabelle.
-   Die [Tabelle Class](class-table.md) wird verwendet, um Klassen-IDs und andere Informationen für COM-Objekte zu registrieren. Diese Tabelle enthält comserverbezogene Informationen, die als Teil der Produktankündigung generiert werden müssen.
-   Die [Tabelle ProgId](progid-table.md) ordnet Programm-IDs Klassen-IDs zu.
-   Die [Tabelle AppId](appid-table.md) wird verwendet, um allgemeine Sicherheits- und Konfigurationseinstellungen für DCOM-Objekte zu registrieren.
-   Die [Umgebungstabelle](environment-table.md) wird verwendet, um die Werte von Umgebungsvariablen festzulegen, und in Windows 2000 schreibt die Umgebungstabelle ebenfalls in die Registrierung.
-   Die [Registrierungstabelle](registry-table.md) enthält alle anderen Informationen, die die Anwendung in die Systemregistrierung integrieren muss. Dies schließt Standardeinstellungen, Benutzerinformationen oder Daten oder die COM-Registrierung ein, die von den oben genannten Tabellen nicht unterstützt werden.
-   Die [Tabelle RemoveRegistry](removeregistry-table.md) enthält die Registrierungsinformationen, die die Anwendung zum Zeitpunkt der Installation aus der Systemregistrierung löschen muss.

 

 



