---
description: Die Gruppe Locatortabellen wird verwendet, um Dateien und Anwendungen zu suchen.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Locator Tables Group
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0cf5b2d28d01b6e10cf796dc9653c82feb8ffb63adc57c7a7bc244e7ccfcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629167"
---
# <a name="locator-tables-group"></a>Locator Tables Group

Die Gruppe Locatortabellen wird verwendet, um Dateien und Anwendungen zu suchen. Um nach einer Datei zu suchen, bestimmen Sie zunächst die Dateisignatur, und suchen Sie dann nach der Datei. Die Locator-Tabellen werden verwendet, um die Registrierung, die Konfigurationsdaten des Installationsprogramms, die Verzeichnisstruktur oder .ini Dateien nach der eindeutigen Signatur einer Datei zu durchsuchen. Die Dateisignatur kann dann in der [Signaturtabelle](signature-table.md) überprüft werden, um sicherzustellen, dass es sich bei einer bestimmten Datei tatsächlich um die gesuchte Datei handelt und nicht um eine andere Datei mit dem gleichen Namen. Wenn ein Datensatz in einer Locatortabelle keinen Schlüssel in der Signaturtabelle enthält, bezieht sich der Datensatz auf ein Verzeichnis und nicht auf eine Datei.

Die Komponente, die eine Datei steuert, befindet sich in der [Dateitabelle](file-table.md) über den externen Schlüssel der [Komponententabelle](component-table.md). Das Installationsprogramm löst den Speicherort einer Datei über die Tabelle Komponente auf, da jede Datei zu einer Komponente gehört. Der Speicherort einer Komponente wird über einen externen Schlüssel in der Tabelle Komponente in der [Verzeichnistabelle](directory-table.md)gefunden.

Der Speicherort einer Anwendung wird gefunden, indem nach Dateien gesucht wird, aus denen die Anwendung besteht. Das Installationsprogramm stellt auch zwei Tabellen für die Suche nach früheren Versionen einer Anwendung bereit: die [Tabelle AppSearch](appsearch-table.md) und die [TABELLE CSVSearch](ccpsearch-table.md).

Die folgenden Tabellen bilden die Gruppe Locator-Tabellen und werden verwendet, um die Dateisignatur zu bestimmen.

-   Die [RegLocator-Tabelle](reglocator-table.md) enthält die Informationen, die für die Suche nach einer Datei oder einem Verzeichnis in der Registrierung erforderlich sind.
-   Die [Tabelle IniLocator](inilocator-table.md) enthält die Informationen, die für die Suche nach einer .ini-Datei erforderlich sind. Die .ini-Datei muss im Standardverzeichnis von Microsoft Windows vorhanden sein.
-   Die [Tabelle CompLocator](complocator-table.md) enthält die Informationen, die zum Suchen nach einer Datei oder einem Verzeichnis mithilfe der Konfigurationsdaten des Installationsprogramms erforderlich sind.
-   Die [DrLocator-Tabelle](drlocator-table.md) enthält die Informationen, die für die Suche nach einer Datei oder einem Verzeichnis in der Verzeichnisstruktur erforderlich sind.
-   Die [Tabelle AppSearch](appsearch-table.md) enthält die Eigenschaften, die auf das Suchergebnis einer entsprechenden Dateisignatur festgelegt werden müssen.
-   Die [TABELLE DOSSIERSearch](ccpsearch-table.md) enthält die Liste der Dateisignaturen, von denen mindestens eine auf dem Computer eines Benutzers für das Programm zur Konformitätsüberprüfung (COMPLIANCE Checking Program, DOSSIER) vorhanden sein muss.

 

 



