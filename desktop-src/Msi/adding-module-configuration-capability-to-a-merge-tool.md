---
description: Windows Installer Entwickler können Tools erstellen, die es Endbenutzern ermöglichen, konfigurierbare Mergemodule zu verwenden.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Hinzufügen von Modul Konfigurationsfunktionen zu einem Mergetool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756253"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>Hinzufügen von Modul Konfigurationsfunktionen zu einem Mergetool

Damit Endbenutzer konfigurierbare Mergemodule verwenden können, können Sie Merge-und Konfigurationstools erstellen, um folgende Aufgaben durchzuführen:

-   Merge-Tools sollten die Funktionen in Mergemod.dll Version 2,0 zum Zusammenführen des Moduls aufruft. Frühere Versionen von Mergemod.dll können nicht zum Konfigurieren von Mergemodulen verwendet werden.
-   Client Konfigurations Anwendungen sollten mit dem mergemodulbenutzer interagieren, um die Benutzer Auswahl für konfigurierbare Elemente zu erfassen.
-   Die Merge-Tools sollten Konfigurationsinformationen, die im Mergemodul erstellt wurden, für die Client Anwendung verfügbar machen, damit der Client diese Informationen verwenden kann, um den Benutzer abzufragen.
-   Wenn ein Zusammenführungstool während einer Zusammenführung auf ein konfigurierbares Element stößt, sollte es das Client Konfigurationstool für Anpassungs Informationen abrufen, die vom Benutzer abgerufen wurden. Das Merge-Tool sollte die angegebenen Änderungen am Mergemodul vornehmen.
-   Konfigurations Anwendungen sollten es dem Benutzer ermöglichen, Optionen für konfigurierbare Elemente bereitzustellen, aber alle möglichen Optionen müssen für den Benutzer nicht offengelegt werden. Das Mergetool kann Standardwerte für konfigurierbare Elemente verwenden, die der Benutzer nicht ausgewählt hat.
-   Wenn ein Benutzer keine Anpassungs Informationen bereitstellt, sollten die mergetools die im Mergemodul angegebenen Standard Konfigurationswerte verwenden.
-   Nachdem ein Benutzer eine bestimmte Auswahl für das Konfigurationstool erteilt hat, ruft das Merge-Tool Mergemod.dll auf, um den Merge auszuführen.

 

 



