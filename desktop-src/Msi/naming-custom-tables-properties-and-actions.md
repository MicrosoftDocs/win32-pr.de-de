---
description: Paket Ersteller sollten sicherstellen, dass die Namen von benutzerdefinierten Tabellen, Eigenschaften oder Aktionen, die in Ihrem Paket definiert sind, nicht mit den Namen von Standard Tabellen,-Eigenschaften oder-Aktionen in Konflikt stehen, die für die Windows Installer System eigen sind.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864083"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen

Paket Ersteller sollten sicherstellen, dass die Namen von benutzerdefinierten Tabellen, Eigenschaften oder Aktionen, die in Ihrem Paket definiert sind, nicht mit den Namen von Standard Tabellen,-Eigenschaften oder-Aktionen in Konflikt stehen, die für die Windows Installer System eigen sind.

Paket Autoren sollten die folgenden Richtlinien für benutzerdefinierte Tabellen-, Eigenschafts-oder Aktions Namen einhalten.

-   Geben Sie Namen für benutzerdefinierte Tabellen, Eigenschaften oder Aktionen mit einem Präfix an, das Ihre Anwendung identifiziert.
-   Verwenden Sie niemals einen Namen mit MSI als Präfix. Ab Windows Installer 2,0 werden allen neuen systemeigenen Windows Installer Eigenschaften, Aktionen und Tabellennamen mit dem Präfix MSI zugewiesen. Bei diesem Präfix wird die Groß-/Kleinschreibung nicht beachtet, z.b. msinewinternaltable. Da die Groß-/Kleinschreibung nicht beachtet wird, sollten Autoren alle Fälle des MSI-Präfixes vermeiden.

Weitere Informationen finden Sie unter [Tabellennamen](table-names.md).

 

 



