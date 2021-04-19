---
description: Die MigrateFeatureStates-Aktion wird während des Upgrades und bei der Installation einer neuen Anwendung über eine verwandte Anwendung verwendet.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: MigrateFeatureStates-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e76edb5fa13506291cc85ebcf8c8824e4ee28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373214"
---
# <a name="migratefeaturestates-action"></a>MigrateFeatureStates-Aktion

Die MigrateFeatureStates-Aktion wird während des Upgrades und bei der Installation einer neuen Anwendung über eine verwandte Anwendung verwendet. MigrateFeatureStates liest die Funktions Zustände in der vorhandenen Anwendung und legt diese Funktions Zustände dann in der ausstehenden Installation fest. Die-Methode ist nur nützlich, wenn sich die neue Funktionsstruktur nicht wesentlich vom ursprünglichen geändert hat.

Die MigrateFeatureStates-Aktion wird nur bei der erstmaligen Installation des Produkts ausgeführt. Die Aktion "MigrateFeatureStates" wird während des Wartungsmodus oder der nicht Installation nicht ausgeführt.

Die MigrateFeatureStates-Aktion durchläuft jeden Datensatz der [upgradetabelle](upgrade-table.md) nacheinander und vergleicht den UpgradeCode, die Produktversion und die Sprache in jeder Zeile mit allen auf dem System installierten Produkten. Wenn MigrateFeatureStates Action eine Entsprechung erkennt und das msidbUpgradeAttributesMigrateFeatures-Bitflag in der Spalte Attribute der upgradetabelle festgelegt ist, fragt das Installationsprogramm die vorhandenen Funktions Zustände für das Produkt ab und legt diese Zustände für dieselben Features in der neuen Anwendung fest. Durch die Aktion werden nur die Funktions Zustände migriert, wenn die [**vorab ausgewählte**](preselected.md) Eigenschaft nicht festgelegt ist.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion "MigrateFeatureStates" sollte unmittelbar nach der [Aktion "costfinalize](costfinalize-action.md)" erfolgen. MigrateFeatureStates muss sowohl in der Tabelle [InstallUISequence](installuisequence-table.md) als auch in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)sequenziert werden. Der Installer verhindert, dass MigrateFeatureStates in InstallExecuteSequence ausgeführt wird, wenn die Aktion bereits in InstallUISequence ausgeführt wurde.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

MigrateFeatureSettings sendet eine Aktions Daten Nachricht für jedes Produkt.

## <a name="remarks"></a>Bemerkungen

Wenn mehr als ein installiertes Produkt eine Funktion gemeinsam nutzt, kann sich der Installationsstatus für diese Funktion zwischen den Produkten unterscheiden. MigrateFeatureState Action verwendet die folgende Rangfolge beim Migrieren von featureinstallationszuständen: lokal ausführen, aus Quelle ausführen, angekündigt und deinstalliert. Beispielsweise verfügt das installierte Produkt A möglicherweise über das Feature y als InstallState \_ local, und installiertes Produkt B hat möglicherweise die Funktion y als nicht \_ vorhanden. Wenn ein Upgrade das Produkt c installiert und den Installationsstatus von Feature y migriert, legt MigrateFeatureState den Installationsstatus von Feature y in Product C auf InstallState \_ local fest.

Weitere Informationen zur Verwendung der MigrateFeatureStates-Aktion für Produkt Upgrades finden Sie unter [Vorbereiten einer Anwendung für zukünftige größere Upgrades](preparing-an-application-for-future-major-upgrades.md).

 

 



