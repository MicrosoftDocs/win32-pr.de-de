---
description: Wenn der Windows Installer das Installationsskript für die Installation eines Produkts oder einer Anwendung verarbeitet, generiert es gleichzeitig ein Rollback-Skript und speichert eine Kopie jeder Datei, die während der Installation gelöscht wurde.
ms.assetid: 6c70e788-beb0-46db-94b0-1bbaac972acf
title: Rollback-Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc958c7d5e1dead2cd3e3e0b6081e7c71cd9af7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130665"
---
# <a name="rollback-installation"></a>Rollback-Installation

Wenn der Windows Installer das Installationsskript für die Installation eines Produkts oder einer Anwendung verarbeitet, generiert es gleichzeitig ein Rollback-Skript und speichert eine Kopie jeder Datei, die während der Installation gelöscht wurde. Diese Dateien werden in einem verborgenen System Verzeichnis gespeichert und automatisch gelöscht, sobald die Installation erfolgreich abgeschlossen wurde. Wenn die Installation jedoch nicht erfolgreich ist, führt das Installationsprogramm automatisch eine Rollback-Installation durch, bei der das System in seinen ursprünglichen Zustand zurückversetzt wird.

Das automatische Rollback einer nicht erfolgreichen Installation ist das Standardverhalten des Installers. Um das Rollback während einer Installation zu deaktivieren, verwenden Sie eine der folgenden Aktionen:

-   [**DISABLEROLLBACK (Eigenschaft)**](-disablerollback.md)
-   [**Promptrollbackcost (Eigenschaft)**](promptrollbackcost.md)
-   [DISABLEROLLBACK-Aktion](disablerollback-action.md)
-   [DISABLEROLLBACK](disablerollback.md)
-   [Enablerollback-ControlEvent](enablerollback-controlevent.md)

Wenn Rollback deaktiviert ist, legt das Installationsprogramm die [**rollbackdeaktiviert**](rollbackdisabled.md) -Eigenschaft fest.

Wenn eine Installation [benutzerdefinierte Aktionen](custom-actions.md)verwendet, ist eine zusätzliche Erstellung des Installationspakets erforderlich, um die Roll Back Funktion zu verwenden. Weitere Informationen finden Sie unter [Rollback für benutzerdefinierte Aktionen](rollback-custom-actions.md).

 

 



