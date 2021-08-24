---
description: Um ein größeres Upgrade mit Windows Installer anzuwenden, muss das ursprüngliche Produktinstallationspaket eine UpgradeCode-Eigenschaft angeben, die unter Vorbereiten einer Anwendung für zukünftige größere Upgrades beschrieben wird, und das Upgradepaket muss über eine Upgradetabelle verfügen.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Aktualisieren der Upgradetabelle für ein Upgrade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba65db43019c09e27824c54265244c65b900e4f3c94dacd24405e7fac2e0272a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809750"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Aktualisieren der Upgradetabelle für ein Upgrade

Um ein größeres Upgrade mit Windows Installer anzuwenden, muss das ursprüngliche Produktinstallationspaket eine [**UpgradeCode-Eigenschaft**](upgradecode.md) angeben, die unter [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md)beschrieben wird, und das Upgradepaket muss über eine [Upgradetabelle verfügen.](upgrade-table.md)

Weitere Informationen zu größeren Upgrades finden Sie unter [Hauptupgrades](major-upgrades.md) unter [Patchen und Upgrades.](patching-and-upgrades.md)

Dem Installationspaket von MNP2000.msi wurde eine [**UpgradeCode-Eigenschaft**](upgradecode.md) zugewiesen, wie im Abschnitt [Angeben von Eigenschaften](specifying-properties.md)beschrieben.

Windows Das Installationsprogramm wendet das Upgrade an, wenn der Benutzer bereits die Versionen 1.0 bis 1.4 (einschließlich) der englischen Sprache MNP2000 installiert hat. Windows Das Installationsprogramm migriert alle Featureeinstellungen des ursprünglichen Produkts zum aktualisierten Produkt. Das Installationsprogramm entfernt die Dateien, die zu den ursprünglichen Produkten gehören, die vom Upgrade des Produkts nicht verwendet werden.

Wenn Ihre Kopie von MNP2001.msi keine [Upgradetabelle](upgrade-table.md)enthält, verwenden Sie Orca oder einen anderen Tabellen-Editor, um eine leere Upgradetabelle aus Schema.msi in die Datenbank zu importieren. Das SDK stellt eine Kopie der Schema.msi bereit. Verwenden Sie den Datenbank-Editor, um MNP2001.msi zu öffnen und die folgenden Daten in die leere Upgradetabelle einzugeben.



| Upgradecode                            | VersionMin | VersionMax | Sprache | Attribute | Entfernen | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 1033     | 769        |        | OLDAPPFOUND    |



 

[Fortsetzen](updating-properties-for-an-upgrade.md)

 

 



