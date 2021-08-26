---
description: Paketautoren sollten sicherstellen, dass die Namen von benutzerdefinierten Tabellen, Eigenschaften oder Aktionen, die in ihrem Paket definiert sind, nicht mit den Namen von Standardtabellen, Eigenschaften oder Aktionen in Konflikt stehen, die für den Windows Installer nativ sind.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd26ab08bcada936bdcb9c87d10cb060c697689cec8978a1eae0d25ac5c0a2d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105080"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Benennen von benutzerdefinierten Tabellen, Eigenschaften und Aktionen

Paketautoren sollten sicherstellen, dass die Namen von benutzerdefinierten Tabellen, Eigenschaften oder Aktionen, die in ihrem Paket definiert sind, nicht mit den Namen von Standardtabellen, Eigenschaften oder Aktionen in Konflikt stehen, die für den Windows Installer nativ sind.

Paketautoren sollten die folgenden Richtlinien für benutzerdefinierte Tabellen-, Eigenschafts- oder Aktionsnamen einhalten.

-   Erstellen Sie Namen für benutzerdefinierte Tabellen, Eigenschaften oder Aktionen, die über ein Präfix verfügen, das Ihre Anwendung identifiziert.
-   Verwenden Sie niemals einen Namen mit Msi als Präfix. Ab Windows Installer 2.0 erhalten alle neuen nativen Windows Eigenschaften, Aktionen und Tabellen des Installationsprogramms Namen mit dem Präfix Msi. Bei diesem Präfix wird die Groß-/Kleinschreibung nicht beachtet, z. B. MsiNewInternalTable. Da beim Präfix die Groß-/Kleinschreibung nicht beachtet wird, sollten Autoren alle Fälle des Msi-Präfixes vermeiden.

Weitere Informationen finden Sie unter [Tabellennamen.](table-names.md)

 

 



