---
description: Autoren von Installationspaketen können angeben, dass das Installationsprogramm die freigegebenen Dateien (häufig freigegebene DLLs) einer Anwendung in den Ordner dieser Anwendung anstatt an einen freigegebenen Speicherort kopiert.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Isolierte Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08095e72862a94474b7096950ac5ed3b331e806456e72982ee9d7374ab9511b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013178"
---
# <a name="isolated-components"></a>Isolierte Komponenten

Autoren von Installationspaketen können angeben, dass das Installationsprogramm die freigegebenen Dateien (häufig freigegebene DLLs) einer Anwendung in den Ordner dieser Anwendung anstatt an einen freigegebenen Speicherort kopiert. Dieser private Satz von Dateien (DLLs) wird dann nur von der Anwendung verwendet. Das Isolieren der Anwendung zusammen mit den freigegebenen Komponenten auf diese Weise hat die folgenden Vorteile:

-   Die Anwendung verwendet immer die Versionen der freigegebenen Dateien, mit denen sie bereitgestellt wurde.
-   Durch die Installation der Anwendung werden keine anderen Versionen der freigegebenen Dateien von anderen Anwendungen überschrieben.
-   Nachfolgende Installationen anderer Anwendungen, die verschiedene Versionen der freigegebenen Dateien verwenden, können die von dieser Anwendung verwendeten Dateien nicht überschreiben.

Da die aktuelle Implementierung von COM einen einzelnen vollständigen Pfad in der Registrierung für jedes CLSID-/Kontextpaar bei sich behält, erzwingt dies, dass alle Anwendungen die gleiche Version einer freigegebenen DLL verwenden. Damit eine Anwendung eine private Kopie eines COM-Servers behalten kann, überprüft das Systemlader in Windows 2000, ob eine -Datei vor ort ist. LOCAL-Datei im Ordner der Anwendung. Wenn das Systemlader eine erkennt. LOKALE Datei ändert die Suchlogik so, dass DLLs bevorzugt werden, die sich im gleichen Ordner wie die Anwendung befinden.

Wenn Windows Installer die [Aktion IsolateComponents](isolatecomponents-action.md) ausgeführt, kopieren sie die Dateien der Komponente (häufig eine freigegebene DLL), die in der Spalte Freigegebene Komponenten der \_ [Tabelle IsolatedComponent](isolatedcomponent-table.md) angegeben ist, in den gleichen Ordner wie die Komponente (im Allgemeinen eine .exe-Datei), die in der Spalte Komponentenanwendung angegeben \_ ist. Das Installationsprogramm erstellt in diesem Verzeichnis eine Datei mit einer Länge von 0 Bytes, an die der kurze Dateiname der Schlüsseldatei für die Komponentenanwendung angefügt ist (in der Regel entspricht der Name dem .exe der \_ Anwendung). lokal. Das Installationsprogramm verwendet die Registrierung für die Komponente am freigegebenen Speicherort und schreibt keine Registrierungsinformationen für die Kopie der Komponente am privaten Speicherort.

Weitere Informationen finden Sie unter

-   [Installation isolierter Komponenten](installation-of-isolated-components.md)
-   [Neuinstallation isolierter Komponenten](reinstallation-of-isolated-components.md)
-   [Entfernen isolierter Komponenten](removal-of-isolated-components.md)
-   [Verwenden isolierter Komponenten](using-isolated-components.md)

 

 



