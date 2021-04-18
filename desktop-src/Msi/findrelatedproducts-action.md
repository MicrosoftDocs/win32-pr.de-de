---
description: Die Aktion FindRelatedProducts wird nacheinander durch jeden Datensatz der upgradetabelle durchlaufen und vergleicht den UpgradeCode, die Produktversion und die Sprache in jeder Zeile mit den auf dem System installierten Produkten.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: FindRelatedProducts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347168"
---
# <a name="findrelatedproducts-action"></a>FindRelatedProducts-Aktion

Die Aktion FindRelatedProducts wird nacheinander durch jeden Datensatz der [upgradetabelle](upgrade-table.md) durchlaufen und vergleicht den UpgradeCode, die Produktversion und die Sprache in jeder Zeile mit den auf dem System installierten Produkten. Wenn "FindRelatedProducts" eine Übereinstimmung zwischen den Upgradeinformationen und einem installierten Produkt erkennt, fügt Sie den Produktcode an die Eigenschaft an, die in der Spalte "Aktions Eigenschaft" von "upgradetable" angegeben ist.

Die Aktion "FindRelatedProducts" wird nur bei der erstmaligen Installation des Produkts ausgeführt. Die Aktion "FindRelatedProducts" wird während des Wartungsmodus oder der nicht Installation nicht ausgeführt.

## <a name="database-tables-queried"></a>Abgefragte Datenbanktabellen

Mit dieser Aktion wird die folgende Tabelle abgefragt:

[Upgradetabelle](upgrade-table.md)

## <a name="properties-used"></a>Verwendete Eigenschaften

Die Aktion FindRelatedProducts verwendet die [**UpgradeCode**](upgradecode.md) -Eigenschaft und die in der upgradetabelle erstellten Versions-und Sprachinformationen, um installierte Produkte zu erkennen, die von dem ausstehenden Upgrade betroffen sind. Der Produktcode der erkannten Produkte wird an die Eigenschaft in der Spalte "Aktions Eigenschaft" von "upgradetable" angehängt.

FindRelatedProducts erkennt nur vorhandene Produkte, die mithilfe des Windows Installer mit einer MSI-Datei installiert wurden, die eine [**UpgradeCode**](upgradecode.md) -Eigenschaft definiert, eine [**ProductVersion**](productversion.md) -Eigenschaft und einen Wert für die [**productlanguage**](productlanguage.md) -Eigenschaft, die eine der in der [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft aufgelisteten Sprachen ist.

Beachten Sie, dass "FindRelatedProducts" die von " [**msigetproductinfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)" zurückgegebene Sprache verwendet. Damit FindRelatedProducts ordnungsgemäß funktioniert, muss der Paket Ersteller sicherstellen, dass die [**productlanguage**](productlanguage.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md) auf eine Sprache festgelegt ist, die auch in der [**Template-Übersichts**](template-summary.md) Eigenschaft aufgeführt ist. Weitere [wichtige Upgrades finden Sie unter Vorbereiten einer Anwendung](preparing-an-application-for-future-major-upgrades.md).

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

FindRelatedProducts muss in der Tabelle " [InstallUISequence](installuisequence-table.md) " und in [InstallExecuteSequence](installexecutesequence-table.md) -Tabellen erstellt werden. Das Installationsprogramm verhindert, dass findrelated-Produkte in InstallExecuteSequence ausgeführt werden, wenn die Aktion bereits in InstallUISequence ausgeführt wurde. Die FindRelatedProducts-Aktion muss vor der Aktion " [MigrateFeatureStates](migratefeaturestates-action.md) " und der [Aktion "RemoveExistingProducts](removeexistingproducts-action.md)" erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

FindRelatedProducts sendet eine Aktions Daten Nachricht für jedes zugehörige Produkt, das auf dem System erkannt wird.

 

 



