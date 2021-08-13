---
description: Die Gruppe Locator tables (Locatortabellen) wird verwendet, um Dateien und Anwendungen zu suchen.
ms.assetid: 44ab770b-1a7f-4590-9681-8f6bd343bf86
title: Gruppe "Locatortabellen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0cf5b2d28d01b6e10cf796dc9653c82feb8ffb63adc57c7a7bc244e7ccfcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629167"
---
# <a name="locator-tables-group"></a>Gruppe "Locatortabellen"

Die Gruppe Locator tables (Locatortabellen) wird verwendet, um Dateien und Anwendungen zu suchen. Um nach einer Datei zu suchen, bestimmen Sie zuerst die Dateisignatur, und suchen Sie dann die Datei. Die Locator-Tabellen werden verwendet, um die Registrierung, die Konfigurationsdaten des Installationsprogramms, die Verzeichnisstruktur oder .ini dateien nach der eindeutigen Signatur einer Datei zu durchsuchen. Die Dateisignatur kann dann in [](signature-table.md) der Signaturtabelle überprüft werden, um sicherzustellen, dass es sich bei einer bestimmten Datei tatsächlich um die gesuchte Datei und nicht um eine andere Datei mit dem gleichen Namen handelt. Wenn ein Datensatz in einer Locatortabelle keinen Schlüssel in der Signaturtabelle enthält, verweist der Datensatz auf ein Verzeichnis und nicht auf eine Datei.

Die Komponente, die eine Datei steuert, befindet sich in der [Tabelle File über](file-table.md) den externen Schlüssel der [Component-Tabelle.](component-table.md) Das Installationsprogramm löst den Speicherort einer Datei über die Component-Tabelle auf, da jede Datei zu einer Komponente gehört. Der Speicherort einer Komponente wird durch einen externen Schlüssel in der Component -Tabelle in der [Directory-Tabelle gefunden.](directory-table.md)

Der Speicherort einer Anwendung wird durch Suchen nach Dateien gefunden, aus denen die Anwendung besteht. Das Installationsprogramm stellt auch zwei Tabellen für die Suche nach früheren Versionen einer Anwendung zur Verfügung: die [AppSearch-Tabelle](appsearch-table.md) und die [TABELLE DESTSearch-Tabellen.](ccpsearch-table.md)

Die folgenden Tabellen machen die Gruppe Locator-Tabellen aus und werden verwendet, um die Dateisignatur zu bestimmen.

-   Die [RegLocator-Tabelle](reglocator-table.md) enthält die Informationen, die zum Suchen nach einer Datei oder einem Verzeichnis in der Registrierung erforderlich sind.
-   Die [IniLocator-Tabelle](inilocator-table.md) enthält die Informationen, die zum Suchen nach einer .ini erforderlich sind. Die .ini-Datei muss im Microsoft-Standardverzeichnis Windows sein.
-   Die [Tabelle CompLocator enthält](complocator-table.md) die Informationen, die für die Suche nach einer Datei oder einem Verzeichnis mithilfe der Konfigurationsdaten des Installationsprogramms erforderlich sind.
-   Die [DrLocator-Tabelle](drlocator-table.md) enthält die Informationen, die für die Suche nach einer Datei oder einem Verzeichnis in der Verzeichnisstruktur erforderlich sind.
-   Die [AppSearch-Tabelle](appsearch-table.md) enthält die Eigenschaften, die auf das Suchergebnis einer entsprechenden Dateisignatur festgelegt werden müssen.
-   Die [TABELLE ANTIVIRUSSearch](ccpsearch-table.md) enthält die Liste der Dateisignaturen, von denen mindestens eines auf dem Computer eines Benutzers für das Compliance Checking Program (ANTIVIRUS) vorhanden sein muss.

 

 



