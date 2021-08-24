---
description: Die MigrateFeatureStates-Aktion wird während des Upgrades und bei der Installation einer neuen Anwendung über eine zugehörige Anwendung verwendet.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: MigrateFeatureStates-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac96a3b2babf5f92ae8078ecc703875c09a0e2f61155fd565985919b5a6393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745170"
---
# <a name="migratefeaturestates-action"></a>MigrateFeatureStates-Aktion

Die MigrateFeatureStates-Aktion wird während des Upgrades und bei der Installation einer neuen Anwendung über eine zugehörige Anwendung verwendet. MigrateFeatureStates liest die Featurezustände in der vorhandenen Anwendung und legt diese Featurezustände dann in der ausstehenden Installation fest. Die -Methode ist nur nützlich, wenn sich die neue Featurestruktur nicht stark von der ursprünglichen geändert hat.

Die MigrateFeatureStates-Aktion wird nur bei der ersten Installation des Produkts ausgeführt. Die MigrateFeatureStates-Aktion wird nicht während des Wartungsmodus oder der Deinstallation ausgeführt.

Die MigrateFeatureStates-Aktion durchläuft jeden Datensatz der [Upgradetabelle](upgrade-table.md) nacheinander und vergleicht den Upgradecode, die Produktversion und die Sprache in jeder Zeile mit allen auf dem System installierten Produkten. Wenn die MigrateFeatureStates-Aktion eine Entsprechung erkennt und das Bitflag msidbUpgradeAttributesMigrateFeatures in der Spalte Attribute der Upgradetabelle festgelegt ist, fragt das Installationsprogramm die vorhandenen Featurezustände für das Produkt ab und legt diese Zustände für die gleichen Features in der neuen Anwendung fest. Die Aktion migriert die Featurezustände nur, wenn die [**Eigenschaft Vorab ausgewählt**](preselected.md) nicht festgelegt ist.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die MigrateFeatureStates-Aktion sollte unmittelbar nach der [CostFinalize-Aktion beginnen.](costfinalize-action.md) MigrateFeatureStates muss sowohl in der [InstallUISequence-Tabelle](installuisequence-table.md) als auch in der [InstallExecuteSequence-Tabelle sequenziert werden.](installexecutesequence-table.md) Das Installationsprogramm verhindert die Ausführung von MigrateFeatureStates in InstallExecuteSequence, wenn die Aktion bereits in InstallUISequence ausgeführt wurde.

## <a name="actiondata-messages"></a>ActionData-Meldungen

MigrateFeatureSettings sendet eine Aktionsdatennachricht für jedes Produkt.

## <a name="remarks"></a>Hinweise

Wenn mehrere installierte Produkte ein Feature verwenden, kann sich der Installationsstatus für dieses Feature von Produkt zu Produkt unterscheiden. Die MigrateFeatureState-Aktion verwendet beim Migrieren von Featureinstallationszuständen die folgende Rangfolge: Lokale Ausführung, Ausführung aus der Quelle, Ankündigung und Deinstallation. Beispielsweise kann das installierte Produkt A das Feature Y als INSTALLSTATE LOCAL und das installierte Produkt B das Feature Y als \_ INSTALLSTATE \_ ABSENT haben. Wenn ein Upgrade Produkt C installiert und den Installationsstatus des Features Y migriert, legt MigrateFeatureState den Installationsstatus von Feature Y in Produkt C auf INSTALLSTATE \_ LOCAL fest.

Weitere Informationen zur Verwendung der MigrateFeatureStates-Aktion für Produktupgrades finden Sie unter [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).

 

 



