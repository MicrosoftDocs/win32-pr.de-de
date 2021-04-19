---
description: Die Gruppe Locator Tables dient zum Suchen von Dateien und Anwendungen.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Locator-Tabellen Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 300a869a912c06b2112476f50bcda021833cfbe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349499"
---
# <a name="locator-tables-group"></a>Locator-Tabellen Gruppe

Die Gruppe Locator Tables dient zum Suchen von Dateien und Anwendungen. Um nach einer Datei zu suchen, bestimmen Sie zuerst die Datei Signatur, und suchen Sie dann die Datei. Die Locator-Tabellen werden zum Durchsuchen der Registrierung, der installerkonfigurationsdaten, der Verzeichnisstruktur oder der INI-Dateien für die eindeutige Signatur einer Datei verwendet. Die Datei Signatur kann dann in der [Signatur Tabelle](signature-table.md) eingeglichen werden, um zu überprüfen, ob es sich bei einer bestimmten Datei wirklich um die gesuchte Datei handelt, und nicht um eine andere Datei mit demselben Namen. Wenn ein Datensatz in einer Serverlocatorpunkt-Tabelle keinen Schlüssel in der Signatur Tabelle enthält, verweist der Datensatz auf ein Verzeichnis und nicht auf eine Datei.

Die Komponente, die eine Datei steuert, befindet sich in der [Dateitabelle](file-table.md) durch den externen Schlüssel der [Komponenten Tabelle](component-table.md). Das Installationsprogramm löst den Speicherort einer Datei durch die Komponenten Tabelle auf, da jede Datei zu einer Komponente gehört. Der Speicherort einer Komponente wird durch einen externen Schlüssel in der Komponenten Tabelle der [Verzeichnis Tabelle](directory-table.md)gefunden.

Der Speicherort einer Anwendung wird gefunden, indem nach Dateien gesucht wird, aus denen die Anwendung besteht. Das Installationsprogramm bietet auch zwei Tabellen für die Suche nach früheren Anwendungsversionen: der [AppSearch-Tabelle](appsearch-table.md) und der [ccpsearch-Tabelle](ccpsearch-table.md).

Die folgenden Tabellen bilden die Gruppe Locator Tables und dienen zum Bestimmen der Datei Signatur.

-   Die [reglocator-Tabelle](reglocator-table.md) enthält die Informationen, die erforderlich sind, um nach einer Datei oder einem Verzeichnis in der Registrierung zu suchen.
-   Die [inilocator-Tabelle](inilocator-table.md) enthält die Informationen, die erforderlich sind, um nach einer INI-Datei zu suchen. Die INI-Datei muss im Microsoft Windows-Standardverzeichnis vorhanden sein.
-   Die [complocator-Tabelle](complocator-table.md) enthält die Informationen, die erforderlich sind, um mithilfe der Konfigurationsdaten des Installers nach einer Datei oder einem Verzeichnis zu suchen.
-   Die [drlocator-Tabelle](drlocator-table.md) enthält die Informationen, die erforderlich sind, um in der Verzeichnisstruktur nach einer Datei oder einem Verzeichnis zu suchen.
-   Die [AppSearch-Tabelle](appsearch-table.md) enthält die Eigenschaften, die auf das Suchergebnis einer entsprechenden Datei Signatur festgelegt werden müssen.
-   Die [ccpsearch-Tabelle](ccpsearch-table.md) enthält die Liste der Datei Signaturen, von denen mindestens eine auf dem Computer eines Benutzers für das Konformitäts Überprüfungs Programm (CCP) vorhanden sein muss.

 

 



