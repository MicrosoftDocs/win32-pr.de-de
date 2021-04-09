---
description: Die Registrierungs Gruppe Windows Installer Tabellen enthält Informationen zu Registrierungs Einträgen.
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: Registrierungs Tabellen Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba14bdc2bc5668ce2de3ec66172c75c176ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864836"
---
# <a name="registry-tables-group"></a>Registrierungs Tabellen Gruppe

![Registrierungs Tabellen Gruppe](images/registry.png)

Weitere Informationen zu diesem Diagramm finden Sie unter [Entity Relationship Diagram-Legende](entity-relationship-diagram-legend.md).

Das Installationsprogramm verfügt über bestimmte Tabellen für die verschiedenen Typen von Registrierungs Einträgen. Beim Auffüllen der Registrierungs Tabellen Gruppe ist es wichtig, die Anzahl der Einträge, die in der [Registrierungs Tabelle](registry-table.md) abgelegt werden, zu minimieren und die Verwendung der anderen, spezifischen Registrierungs Tabellen zu maximieren. Dies liegt daran, dass das Installationsprogramm nicht zwischen unterschiedlichen Typen von Registrierungs Einträgen in der Registrierungs Tabelle unterscheiden kann und nicht die interne Logik verwenden kann, die erforderlich ist, um alle Installer-Features, z. b. [*Werbung*](a-gly.md), voll auszuschöpfen. Das Erstellen von com-und shellbezogenen Registrierungs Einträgen auf diese Weise bietet auch eine logischere Organisation und kann helfen, die fehlerhafte Registrierung von com-Server Informationen zu minimieren.

Die Abbildung zeigt die Registrierungs Eintrags Gruppe von Tabellen sowie die [Komponenten Tabelle](component-table.md), die [Funktions Tabelle](feature-table.md)und die [Dateitabelle](file-table.md). Obwohl letztere nicht direkt am Auffüllen der Registrierung beteiligt sind, sind Sie in der Abbildung enthalten, da Sie für die Logik der Registrierungs Eintrags Gruppe unverzichtbar sind.

Die Gruppe Registrierungs Eintrag enthält die folgenden Tabellen spezifischer Registrierungseinträge.

-   Die [Erweiterungs Tabelle](extension-table.md) enthält alle Dateinamen Erweiterungen, die von der Anwendung verwendet werden, zusammen mit den zugehörigen Features und Komponenten.
-   Die [Verb Tabelle](verb-table.md) ordnet Befehls-Verb-Informationen den in der [Erweiterungs Tabelle](extension-table.md)aufgeführten Dateinamen Erweiterungen zu. Dadurch wird eine indirekte Verknüpfung zwischen dem Verb und der Funktions Tabelle bereitstellt, die für die featureankündigung erforderlich ist.
-   Die [typelib-Tabelle](typelib-table.md) enthält Informationen, die das Installationsprogramm für die Registrierung von Typbibliotheken in der Registrierung platziert. Typbibliotheks Einträge werden zum Zeitpunkt der Ankündigung nicht geschrieben. Das Installationsprogramm schreibt die Typbibliotheks Einträge zu dem Zeitpunkt, zu dem die der Bibliothek zugeordneten Komponenten installiert sind.
-   Die [MIME-Tabelle](mime-table.md) ordnet einen MIME-Kontexttyp einer CLSID oder einer Dateinamenerweiterung zu. Dadurch wird ein Pfad zwischen der MIME-und der Funktions Tabelle bereitstellt, die für die featureankündigung erforderlich ist.
-   Die [Tabelle selfreg](selfreg-table.md) enthält Informationen, die für die Selbstregistrierung von Modulen benötigt werden. Die Selbstregistrierung wird vom Installationsprogramm nur aus Gründen der Abwärtskompatibilität bereitgestellt und wird nicht als Methode zum Auffüllen der Registrierung empfohlen. Wenn jedoch Module in Ihrer Anwendung vorhanden sind, die sich selbst registrieren müssen, verwenden Sie die Tabelle selfreg.
-   Die [Klassen Tabelle](class-table.md) wird zum Registrieren von Klassen-IDs und anderen Informationen für COM-Objekte verwendet. Diese Tabelle enthält Informationen zu com-Servern, die als Teil der Produktankündigung generiert werden müssen.
-   Die [ProgID-Tabelle](progid-table.md) ordnet Programm-IDs Klassen-IDs zu.
-   Die [AppID-Tabelle](appid-table.md) wird verwendet, um allgemeine Sicherheits-und Konfigurationseinstellungen für DCOM-Objekte zu registrieren.
-   Die [Umgebungs Tabelle](environment-table.md) wird verwendet, um die Werte von Umgebungsvariablen festzulegen, und in Windows 2000 schreibt die Umgebungs Tabelle auch in die Registrierung.
-   Die [Registrierungs Tabelle](registry-table.md) enthält alle anderen Informationen, die von der Anwendung in die Systemregistrierung eingefügt werden müssen. Dies schließt Standardeinstellungen, Benutzerinformationen oder Daten oder com-Registrierung ein, die von den obigen Tabellen nicht unterstützt werden.
-   Die [Tabelle removeregistry](removeregistry-table.md) enthält die Registrierungsinformationen, die von der Anwendung zum Zeitpunkt der Installation aus der Systemregistrierung gelöscht werden müssen.

 

 



