---
description: Die Aktion FindRelatedProducts durchläuft jeden Datensatz der Upgradetabelle nacheinander und vergleicht den Upgradecode, die Produktversion und die Sprache in jeder Zeile mit produkten, die auf dem System installiert sind.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Aktion "FindRelatedProducts"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8201a2e86f9dec09931b17cd4dd594c45e4bf78de32ba438b8824a6f540563fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142879"
---
# <a name="findrelatedproducts-action"></a>Aktion "FindRelatedProducts"

Die Aktion FindRelatedProducts durchläuft jeden Datensatz der [Upgradetabelle](upgrade-table.md) nacheinander und vergleicht den Upgradecode, die Produktversion und die Sprache in jeder Zeile mit produkten, die auf dem System installiert sind. Wenn FindRelatedProducts eine Entsprechung zwischen den Upgradeinformationen und einem installierten Produkt erkennt, wird der Produktcode an die Eigenschaft angefügt, die in der Spalte ActionProperty der UpgradeTable angegeben ist.

Die Aktion FindRelatedProducts wird nur bei der ersten Installation des Produkts ausgeführt. Die Aktion FindRelatedProducts wird nicht während des Wartungsmodus oder der Deinstallation ausgeführt.

## <a name="database-tables-queried"></a>Abgefragte Datenbanktabellen

Diese Aktion fragt die folgende Tabelle ab:

[Upgradetabelle](upgrade-table.md)

## <a name="properties-used"></a>Verwendete Eigenschaften

Die Aktion FindRelatedProducts verwendet die [**UpgradeCode-Eigenschaft**](upgradecode.md) und die Versions- und Sprachinformationen, die in der Upgradetabelle erfasst wurden, um installierte Produkte zu erkennen, die vom ausstehenden Upgrade betroffen sind. Er fügt den Produktcode der erkannten Produkte an die -Eigenschaft in der ActionProperty -Spalte der UpgradeTable an.

FindRelatedProducts erkennt nur vorhandene Produkte, die mit dem Windows Installer installiert wurden, mit einem .msi, der eine [**UpgradeCode-Eigenschaft,**](upgradecode.md) eine [**ProductVersion-Eigenschaft**](productversion.md) und einen [](template-summary.md) Wert für die [**ProductLanguage-Eigenschaft**](productlanguage.md) definiert, die eine der in der Eigenschaft "Vorlagenzusammenfassung" aufgeführten Sprachen ist.

Beachten Sie, dass FindRelatedProducts die von [**MsiGetProductInfo zurückgegebene Sprache verwendet.**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) Damit FindRelatedProducts ordnungsgemäß funktioniert, muss der Paketautor sicherstellen, dass die [**ProductLanguage-Eigenschaft**](productlanguage.md) in der [Property](property-table.md) -Tabelle auf eine Sprache festgelegt ist, die auch in der Eigenschaft für die Vorlagenzusammenfassung [**aufgeführt**](template-summary.md) ist. Weitere Informationen finden Sie unter Preparing an Application for Future Major Upgrades (Vorbereiten einer Anwendung [für zukünftige Hauptupgrades).](preparing-an-application-for-future-major-upgrades.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

FindRelatedProducts sollte in die [Tabellen InstallUISequence](installuisequence-table.md) und [InstallExecuteSequence erstellt](installexecutesequence-table.md) werden. Das Installationsprogramm verhindert die Ausführung von FindRelated Products in InstallExecuteSequence, wenn die Aktion bereits in InstallUISequence ausgeführt wurde. Die Aktion FindRelatedProducts muss vor der [MigrateFeatureStates-Aktion](migratefeaturestates-action.md) und der [RemoveExistingProducts-Aktion kommen.](removeexistingproducts-action.md)

## <a name="actiondata-messages"></a>ActionData-Meldungen

FindRelatedProducts sendet eine Aktionsdatenmeldung für jedes zugehörige Produkt, das im System erkannt wird.

 

 



