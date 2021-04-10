---
description: Zum Anwenden eines größeren Upgrades mithilfe von Windows Installer muss das ursprüngliche Produkt Installationspaket eine UpgradeCode-Eigenschaft angeben, die unter Vorbereiten einer Anwendung für zukünftige größere Upgrades beschrieben wird, und das Upgradepaket muss eine upgradetabelle aufweisen.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Aktualisieren der upgradetabelle für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131196"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Aktualisieren der upgradetabelle für ein Upgrade

Zum Anwenden eines größeren Upgrades mithilfe von Windows Installer muss das ursprüngliche Produkt Installationspaket eine UpgradeCode-Eigenschaft angeben, die unter [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md)beschrieben wird, und das [**Upgradepaket muss eine upgradetabelle**](upgradecode.md) aufweisen. [](upgrade-table.md)

Weitere Informationen zu größeren Upgrades finden Sie unter [wichtige Upgrades](major-upgrades.md) bei [Patching und Upgrades](patching-and-upgrades.md).

Dem Installationspaket MNP2000.msi wurde eine [**UpgradeCode**](upgradecode.md) -Eigenschaft zugewiesen, wie im Abschnitt Angeben von [Eigenschaften](specifying-properties.md)beschrieben.

Windows Installer wendet das Upgrade an, wenn der Benutzer bereits die Versionen 1,0 bis 1,4 (einschließlich) der englischen Sprache MNP2000 installiert hat. Windows Installer migriert alle Funktionseinstellungen des ursprünglichen Produkts zum aktualisierten Produkt. Das Installationsprogramm entfernt die Dateien, die zu den ursprünglichen Produkten gehören, die nicht von der Aktualisierung des Produkts verwendet werden.

Wenn Ihre Kopie von MNP2001.msi keine [upgradetabelle](upgrade-table.md)enthält, verwenden Sie "Orca" oder einen anderen Tabellen-Editor, um eine leere upgradetabelle aus Schema.msi in die-Datenbank zu importieren. Das SDK stellt eine Kopie Schema.msi bereit. Öffnen Sie MNP2001.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die leere upgradetabelle ein.



| UpgradeCode auch                            | Versionmin | Versionmax | Sprache | Attribute | Entfernen | Aktions Eigenschaft |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908e378a-9551-4772-BF1D-5cfaf6fd9cb4} | 01.00.0000 | 01.40.0000 | 1033     | 769        |        | Oldappfound    |



 

[Fortsetzen](updating-properties-for-an-upgrade.md)

 

 



