---
description: Der UpgradeCode wird hauptsächlich zur Unterstützung wichtiger Upgrades verwendet, obwohl kleine und kleinere Upgradepatches den UpgradeCode für die Produkt Validierung verwenden können.
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: Verwenden von UpgradeCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf32d40364653527b9f906e6dd42de64bb9f697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864380"
---
# <a name="using-an-upgradecode"></a>Verwenden von UpgradeCode

Der [**UpgradeCode**](upgradecode.md) wird hauptsächlich zur Unterstützung wichtiger Upgrades verwendet, obwohl kleine und kleinere **Upgradepatches den UpgradeCode** für die Produkt Validierung verwenden können. Bei größeren Upgrades erkennen, migrieren und entfernen frühere Versionen des Produkts durch die Aktionen " [FindRelatedProducts](findrelatedproducts-action.md)", " [MigrateFeatureStates](migratefeaturestates-action.md)" und " [RemoveExistingProducts](removeexistingproducts-action.md) ". Die Aktion "FindRelatedProducts" sucht nach Produkten anhand von Kriterien, die auf " **UpgradeCode**", " [**productlanguage**](productlanguage.md)" und " [**ProductVersion**](productversion.md)" basieren. Diese Kriterien werden in der [upgradetabelle](upgrade-table.md) angegeben.

Aufgrund der von der Aktion " [FindRelatedProducts](findrelatedproducts-action.md) " verwendeten Kriterien kann " [**UpgradeCode**](upgradecode.md) " für verschiedene Sprachen und Versionen eines einzelnen Produkts identisch sein. Dies liegt daran, dass die [upgradetabelle](upgrade-table.md) das unterscheiden zwischen Produkten und Versions-und sprach Zeilen ermöglicht.

In verschiedenen Versionen desselben Produkts müssen Sie den [**UpgradeCode**](upgradecode.md)möglicherweise nie ändern. Jedes eigenständige Produkt sollte über einen eigenen **UpgradeCode** verfügen. Eine Produktsuite sollte auch über einen eigenen **UpgradeCode** verfügen. Dies ermöglicht es der Suite, frühere Versionen der Suite oder eigenständigen Produkte zu aktualisieren, indem mehrere Zeilen in der [upgradetabelle](upgrade-table.md)verwendet werden.

Die folgenden beiden Szenarien veranschaulichen die Verwendung von [**UpgradeCode**](upgradecode.md).

-   Produkt a und Produkt B waren mit den gleichen [**productlanguage**](productlanguage.md), [**ProductVersion**](productversion.md)und [**UpgradeCode**](upgradecode.md)ausgeliefert. Produkt a und Produkt B verfügen über unterschiedliche [**productcodes**](productcode.md). Da den Produkten der gleiche **UpgradeCode** zugewiesen wurde, kann die [upgradetabelle](upgrade-table.md) nicht erstellt werden, um die ältere Version von Produkt a von der älteren Version von Produkt B zu unterscheiden. In diesem Fall ist es nicht möglich, eine Upgradeinstallation von Produkt a zu haben, bei der Produkt B ignoriert wird. Da es sich hierbei um unterschiedliche Produkte handelte, sollte jedem eine andere **UpgradeCode** zugewiesen werden.
-   Die englische und die französische Version von Produkt A wurden mit den gleichen [**ProductVersion**](productversion.md) und [**UpgradeCode**](upgradecode.md)ausgeliefert. Sowohl die englische als auch die französische Version von Product A haben unterschiedliche [**productlanguages**](productlanguage.md) und [**productcodes**](productcode.md). Obwohl die Sprachversionen Englisch und Französisch denselben **UpgradeCode** aufweisen, kann die [upgradetabelle](upgrade-table.md) so erstellt werden, dass nur die ältere englische Sprachversion erkannt und aktualisiert und die ältere französische Version ignoriert wird. Verschiedene Sprachversionen eines Produkts können denselben **UpgradeCode** verwenden.

 

 



