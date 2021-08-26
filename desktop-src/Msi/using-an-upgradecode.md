---
description: UpgradeCode wird hauptsächlich zur Unterstützung wichtiger Upgrades verwendet, obwohl kleine und kleinere Upgradepatches den UpgradeCode für die Produktvalidierung verwenden können.
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: Verwenden eines UpgradeCodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482bdaa228bc57432ab730e59f265fc50352c3a63ed29f75ee0a63c65c201ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039090"
---
# <a name="using-an-upgradecode"></a>Verwenden eines UpgradeCodes

[**UpgradeCode wird hauptsächlich**](upgradecode.md) zur Unterstützung wichtiger Upgrades verwendet, obwohl kleine und kleinere Upgradepatches den **UpgradeCode** für die Produktvalidierung verwenden können. Während größerer Upgrades erkennen, migrieren und entfernen die Aktionen [FindRelatedProducts,](findrelatedproducts-action.md) [MigrateFeatureStates](migratefeaturestates-action.md)und [RemoveExistingProducts](removeexistingproducts-action.md) frühere Versionen des Produkts. Die Aktion FindRelatedProducts sucht nach Produkten, die Kriterien basierend auf **UpgradeCode,** [**ProductLanguage**](productlanguage.md)und [**ProductVersion verwenden.**](productversion.md) Diese Kriterien werden in der [Tabelle Upgrade](upgrade-table.md) angegeben.

Angesichts der Kriterien, die von der [Aktion FindRelatedProducts](findrelatedproducts-action.md) verwendet werden, kann [**UpgradeCode**](upgradecode.md) für verschiedene Sprachen und Versionen eines einzelnen Produkts identisch sein. Dies liegt daran, dass die [Upgradetabelle](upgrade-table.md) die Unterschiede zwischen Produkten über Versions- und Sprachzeilen zulässt.

In verschiedenen Versionen desselben Produkts müssen Sie möglicherweise nie [**UpgradeCode ändern.**](upgradecode.md) Jedes eigenständige Produkt sollte über einen eigenen **UpgradeCode verfügen.** Eine Produktsuite sollte auch über einen eigenen **UpgradeCode verfügen.** Auf diese Weise kann die Suite frühere Versionen der Suite oder eigenständige Produkte aktualisieren, indem mehrere Zeilen in der [Upgradetabelle verwendet werden.](upgrade-table.md)

Die folgenden beiden Szenarien veranschaulichen die Verwendung von [**UpgradeCode**](upgradecode.md).

-   Produkt A und Produkt B wurden mit dem gleichen [**ProductLanguage,**](productlanguage.md) [**ProductVersion und**](productversion.md) [**UpgradeCode ausgeliefert.**](upgradecode.md) Produkt A und Produkt B verfügen über unterschiedliche [**ProductCodes.**](productcode.md) Da den Produkten der gleiche **UpgradeCode** zugewiesen wurde, kann die [Upgradetabelle](upgrade-table.md) nicht so verfasst werden, dass die ältere Version von Produkt A von der älteren Version von Produkt B unterschieden wird. In diesem Fall ist keine Upgradeinstallation von Produkt A möglich, bei der Produkt B ignoriert wird. Da es sich um unterschiedliche Produkte handelt, sollte ihnen jeweils ein anderer **UpgradeCode zugewiesen worden sein.**
-   Die englische und die französische Version von Produkt A wurden mit der gleichen [**ProductVersion**](productversion.md) und [**upgradeCode ausgeliefert.**](upgradecode.md) Sowohl die englische als auch die französische Version von Produkt A verfügen über unterschiedliche [**ProductLanguages und**](productlanguage.md) [**ProductCodes.**](productcode.md) Obwohl sowohl die englische als auch die französische Sprachversion denselben **UpgradeCode** verwenden, ist es möglich, die [Upgradetabelle](upgrade-table.md) so zu erstellen, dass nur die ältere Englische Sprachversion erkannt und aktualisiert und die ältere französische Version ignoriert wird. Verschiedene Sprachversionen eines Produkts können denselben **UpgradeCode verwenden.**

 

 



