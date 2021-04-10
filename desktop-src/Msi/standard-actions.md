---
description: Eine Aktion kapselt eine typische Funktion, die während der Installation oder Wartung einer Anwendung ausgeführt wird. Windows Installer verfügt über viele integrierte Standard Aktionen. Entwickler von Installationspaketen können auch eigene benutzerdefinierte Aktionen erstellen.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Standard Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215562"
---
# <a name="standard-actions"></a>Standard Aktionen

Eine Aktion kapselt eine typische Funktion, die während der Installation oder Wartung einer Anwendung ausgeführt wird. Windows Installer verfügt über viele integrierte Standard Aktionen. Entwickler von Installationspaketen können auch eigene [benutzerdefinierte Aktionen](custom-actions.md)erstellen.

Beispiele für Standard Aktionen für den Installer sind:

-   [Aktion "kreateshortcuts](createshortcuts-action.md)": verwaltet die Erstellung von Verknüpfungen zu Dateien, die mit der aktuellen Anwendung installiert wurden. Diese Aktion verwendet die Verknüpfungs [Tabelle](shortcut-table.md) für Ihre Daten.
-   [InstallFiles-Aktion](installfiles-action.md): Kopiert ausgewählte Dateien aus dem Quellverzeichnis in das Zielverzeichnis. Bei dieser Aktion wird die [Dateitabelle](file-table.md) für die Daten verwendet.
-   [Aktion "schreiteregistryvalues](writeregistryvalues-action.md)": richtet Registrierungsinformationen ein, die die Anwendung in der Registrierung erfordert. Diese Aktion verwendet die- [Registrierungs Tabelle](registry-table.md) für Ihre Daten.

In den folgenden Abschnitten werden Standard Aktionen behandelt.

-   [Informationen zu Standard Aktionen](about-standard-actions.md)
-   [Verwenden von Standard Aktionen](using-standard-actions.md)
-   [Referenz zu Standard Aktionen](standard-actions-reference.md)

 

 



