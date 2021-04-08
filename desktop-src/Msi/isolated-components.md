---
description: Autoren von Installationspaketen können angeben, dass das Installationsprogramm die freigegebenen Dateien (häufig freigegebene DLLs) einer Anwendung in den Ordner der Anwendung und nicht in einen freigegebenen Speicherort kopiert.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Isolierte Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f29f614dfd819e093c5729a9a97a076247d281d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750120"
---
# <a name="isolated-components"></a>Isolierte Komponenten

Autoren von Installationspaketen können angeben, dass das Installationsprogramm die freigegebenen Dateien (häufig freigegebene DLLs) einer Anwendung in den Ordner der Anwendung und nicht in einen freigegebenen Speicherort kopiert. Dieser private Satz von Dateien (DLLs) wird dann nur von der Anwendung verwendet. Wenn Sie die Anwendung auf diese Weise mit den freigegebenen Komponenten isolieren, haben Sie folgende Vorteile:

-   Die Anwendung verwendet immer die Versionen der freigegebenen Dateien, mit denen Sie bereitgestellt wurde.
-   Beim Installieren der Anwendung werden andere Versionen der freigegebenen Dateien von anderen Anwendungen nicht überschrieben.
-   Bei nachfolgenden Installationen anderer Anwendungen, die unterschiedliche Versionen der freigegebenen Dateien verwenden, können die von dieser Anwendung verwendeten Dateien nicht überschrieben werden.

Da die aktuelle Implementierung von com einen einzelnen vollständigen Pfad in der Registrierung für jedes CLSID/Kontext-paar beibehält, zwingt Sie alle Anwendungen, dieselbe Version einer freigegebenen DLL zu verwenden. Damit eine Anwendung eine private Kopie eines COM-Servers beibehalten kann, prüft das System Lade Modul in Windows 2000, ob ein vorhanden ist. Lokale Datei im Ordner der Anwendung. , Wenn das System Lade Modul eine erkennt. Lokale Datei ändert Ihre Suchlogik so, dass DLLs bevorzugt werden, die sich im selben Ordner wie die Anwendung befinden.

Wenn Windows Installer die [isolatecomponents-Aktion](isolatecomponents-action.md) ausführt, kopieren Sie die Dateien der Komponente (in der Regel eine freigegebene DLL), die in der frei \_ gegebenen Komponenten Spalte der [isolatedcomponent-Tabelle](isolatedcomponent-table.md) angegeben ist, in denselben Ordner wie die Komponente (in der Regel eine exe-Datei), die in der Spalte Komponenten Anwendung angegeben ist \_ . Das Installationsprogramm erstellt eine Datei in diesem Verzeichnis, eine Länge von 0 (null) Bytes, wobei der kurze Dateiname der Schlüsseldatei für die Komponenten \_ Anwendung (in der Regel der Name ist identisch mit der exe-Datei der Anwendung) ist, der angefügt wird. Nah. Das Installationsprogramm verwendet die Registrierung für die Komponente am freigegebenen Speicherort und schreibt keine Registrierungsinformationen für die Kopie der Komponente am privaten Speicherort.

Weitere Informationen finden Sie unter

-   [Installation isolierter Komponenten](installation-of-isolated-components.md)
-   [Neuinstallation isolierter Komponenten](reinstallation-of-isolated-components.md)
-   [Entfernen isolierter Komponenten](removal-of-isolated-components.md)
-   [Verwenden isolierter Komponenten](using-isolated-components.md)

 

 



