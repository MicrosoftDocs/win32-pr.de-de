---
description: Eine Aktion kapselt eine typische Funktion, die während der Installation oder Wartung einer Anwendung ausgeführt wird. Windows Das Installationsprogramm verfügt über viele integrierte Standardaktionen. Entwickler von Installationspaketen können auch eigene benutzerdefinierte Aktionen erstellen.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Standardaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e95c3ab95a7bddc1f23dd38108b2cb10978ad5316da60397e6f3ba019a415ac4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627620"
---
# <a name="standard-actions"></a>Standardaktionen

Eine Aktion kapselt eine typische Funktion, die während der Installation oder Wartung einer Anwendung ausgeführt wird. Windows Das Installationsprogramm verfügt über viele integrierte Standardaktionen. Entwickler von Installationspaketen können auch eigene benutzerdefinierte [Aktionen erstellen.](custom-actions.md)

Beispiele für Standardaktionen des Installationsprogramms sind:

-   [CreateShortcuts-Aktion:](createshortcuts-action.md)Verwaltet die Erstellung von Verknüpfungen zu Dateien, die mit der aktuellen Anwendung installiert wurden. Diese Aktion verwendet die [Verknüpfungstabelle](shortcut-table.md) für ihre Daten.
-   [InstallFiles-Aktion:](installfiles-action.md)Kopiert ausgewählte Dateien aus dem Quellverzeichnis in das Zielverzeichnis. Diese Aktion verwendet die [Dateitabelle](file-table.md) für ihre Daten.
-   [WriteRegistryValues-Aktion:](writeregistryvalues-action.md)Richtet Registrierungsinformationen ein, die die Anwendung in der Registrierung benötigt. Diese Aktion verwendet die [Registrierungstabelle](registry-table.md) für ihre Daten.

In den folgenden Abschnitten werden Standardaktionen erläutert.

-   [Informationen zu Standardaktionen](about-standard-actions.md)
-   [Verwenden von Standardaktionen](using-standard-actions.md)
-   [Referenz zu Standardaktionen](standard-actions-reference.md)

 

 



