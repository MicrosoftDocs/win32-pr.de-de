---
description: Ab Windows Installer 3,0 können Autoren der patchpaketdatenbank in der msipatchsequence-Tabelle patchsequenzierungs Informationen hinzufügen.
ms.assetid: 9cdcb25f-2c3d-411e-9aae-bdd52df38a97
title: Sequenzieren von Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9cbd9aead596abfaeb50d972915bf4d618440d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218676"
---
# <a name="sequencing-patches"></a>Sequenzieren von Patches

Ab Windows Installer 3,0 können Autoren der patchpaketdatenbank in der [msipatchsequence](msipatchsequence-table.md) -Tabelle patchsequenzierungs Informationen hinzufügen. Das Installationsprogramm kann anhand dieser Informationen bestimmen, welche Patches auf ein Installationspaket anwendbar sind, um die beste patchsequenz zu ermitteln und Patches in konstanter Reihenfolge zu installieren, unabhängig von der Reihenfolge, in der Sie dem System bereitgestellt werden.

**Windows Installer 2,0:** Nicht unterstützt. In Windows Installer Versionen vor Windows Installer 3,0 werden Patches in der Reihenfolge installiert, in der Sie dem System bereitgestellt werden, unabhängig davon, ob Sie eine [msipatchsequence](msipatchsequence-table.md) -Tabelle enthalten.

Folgendes ist erforderlich, um die Funktion für die Patchsequenzierung zu verwenden.

-   [Patchpakete](patch-packages.md) (MSP-Dateien) müssen über eine [msipatchsequence](msipatchsequence-table.md) -Tabelle mit Sequenzierungs Informationen verfügen. Der Installer installiert Patches ohne msipatchsequence-Tabelle in der Reihenfolge, in der Sie dem System bereitgestellt werden.
-   Patches werden mithilfe von Windows Installer 3,0 oder höher installiert.

Windows Installer Version 3,0 verfügt über die folgenden Funktionen, die Anwendungen verwenden können, um die beste patchsequenz zu ermitteln.

-   Die [**msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) -Funktion nimmt eine Liste von Patches vor und bestimmt, in welcher Reihenfolge Sie auf ein installiertes Produkt angewendet werden können. Mit dieser Funktion werden alle Patches oder Produkte berücksichtigt, die bereits auf dem System installiert wurden.
-   Die [**msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) -Funktion nimmt eine Liste von Patches vor und bestimmt, in welcher Reihenfolge Sie auf ein installiertes Produkt angewendet werden können. Diese Funktion berücksichtigt keine Patches oder Produkte, die bereits auf dem System installiert wurden.

Windows Installer Version 3,0 kann mehrere Patches auf ein Produkt in einer einzelnen Patchinstallation anwenden. Die Gruppe der Patches kann Patches enthalten, die das Patchen von Sequenz Informationen (eine [msipatchsequence](msipatchsequence-table.md) -Tabelle) und Patches enthalten, die dies nicht tun. In der Windows Installer werden die Patchpakete ohne diese Tabelle in der Reihenfolge installiert, in der Sie dem System bereitgestellt werden. Das Installationsprogramm ist für Patchpakete vorgesehen, die nicht über eine msipatchsequence-Tabelle verfügen, aber durch die im folgenden Abschnitt beschriebene Methode als veraltete oder abgelösten Patches gekennzeichnet wurden.

Wenn in Windows Installer Version 3,0 mehrere Patches installiert werden, werden die folgenden Schritte ausgeführt, um die Reihenfolge zu bestimmen, in der die einzelnen Patches auf das Produkt angewendet werden:

1.  Installierte Patches ohne [msipatchsequence](msipatchsequence-table.md) -Tabelle werden in der Reihenfolge in der Reihenfolge abgelegt, in der Sie auf das Produkt angewendet wurden. Der erste angewendete Patch wird zuerst in der Sequenz platziert.
2.  Neue Patches ohne [msipatchsequence-Tabelle](msipatchsequence-table.md) werden in die Sequenz eingefügt. Diese Patches werden von der aktuellen Patchen-Installation angewendet. Sie werden in der Reihenfolge abgelegt, in der Sie dem System bereitgestellt werden, und werden nach allen Patches in Schritt 1 platziert.
3.  Veraltete Patches werden aus der Sequenz von Patches entfernt.
    > [!Note]  
    > In der [**Zusammenfassungs Eigenschaft der Revisionsnummer**](revision-number-summary.md) kann ein Patchpaket eine explizite Liste veralteter Patches angeben, die vom Patch entfernt werden sollen. Diese Liste ist für die Verwendung durch Windows Installer Versionen vor Version 3,0 vorgesehen. Windows Installer Version 3,0 entfernt die Patches, die als veraltet markiert sind, aus der Sequenz, nur wenn die Patches nicht über die [msipatchsequence-Tabelle](msipatchsequence-table.md)verfügen.

     

4.  Das Installationsprogramm durchläuft die Patchen-Sequenz und bestimmt, welche Patches in der angegebenen Sequenz anwendbar sind. Wenn mehrere Patches auf ein Produkt angewendet werden, transformiert jeder Patch in der Sequenz auch die Installations Datenbank des Produkts (MSI-Datei). Ein Patch ist nur in einer bestimmten Sequenz anwendbar, wenn seine Daten Bank Transformation in der Lage ist, den [Produktcode](product-codes.md), die [**Version**](productversion.md), die [**Sprache**](productlanguage.md)und den [**UpgradeCode auch**](upgradecode.md) zu verwenden, der sich aus der Anwendung der Transformationen aller vorangehenden [Patchpakete](patch-packages.md) auf die Produktdatenbank ergibt. Das Installationsprogramm entfernt alle anwendbaren Patches aus der Sequenz.
5.  Das Installationsprogramm beginnt mit dem Platzieren von Patches mit Sequenz Informationen in der [msipatchsequence](msipatchsequence-table.md) -Tabelle. [Kleinere Upgradepatches](minor-upgrades.md) , die die msipatchsequence-Tabelle aufweisen, werden nach den in den vorherigen Schritten sequenzierten Patches und in der Reihenfolge ihrer niedrigsten zu höchsten Produktversionen nach dem Upgrade in die Sequenz eingefügt. Windows Installer entfernt dann alle geringfügigen Upgradepatches, die in dieser Sequenz nicht anwendbar sind.
6.  [Kleine](small-updates.md) Updatepatches, die auf [kleinere Upgrades](minor-upgrades.md) abzielen, die über eine [msipatchsequence](msipatchsequence-table.md) -Tabelle verfügen, werden der höchsten Version des geringfügigen Upgradepatches in der Sequenz zugewiesen.
7.  Alle [kleinen](small-updates.md) Updatepatches, die nach den vorherigen Schritten nicht zugewiesen wurden und die die [msipatchsequence](msipatchsequence-table.md) -Tabelle aufweisen, werden vor dem ersten [kleinen Upgrade](minor-upgrades.md) , das die msipatchsequence-Tabelle enthält, und nach der MSI-Installations Datenbank und allen Patches ohne die msipatchsequence-Tabelle in die Sequenz eingefügt. Windows Installer entfernt dann alle kleinen Updatepatches, die in dieser Sequenz nicht zutreffend sind.
8.  Windows Installer Version 3,0 entfernt ersetzte Patches aus der Sequenz. Wenn ein Patch die Patches ablöst, die zuvor in der patchsequenz auftreten, enthält der Patch alle Korrekturen in den vorherigen Patches. Die früheren Patches sind nicht mehr erforderlich. Der Windows Installer erfordert, dass die Informationen in der [msipatchsequence](msipatchsequence-table.md) -Tabelle abgelösten Patches ausschließen.
    > [!Note]  
    > Patches, die als Ersatz für eine frühere Gruppe von Patches dienen, müssen erstellt werden, um die früheren Patches in allen patchfamilien zu ersetzen. [Kleine](small-updates.md) Updatepatches können nur kleine Updates ablösen. [Kleinere Upgrades](minor-upgrades.md) können sowohl bei kleinen Updates als auch bei anderen geringfügigen Upgrades abgelöst werden.

     

9.  [Kleine](small-updates.md) Updatepatches, die [msipatchsequence](msipatchsequence-table.md) -Tabellen enthalten, werden in Produktversionen entsprechend den Sequenzierungs Informationen in ihren msipatchsequence-Tabellen sequenziert. Dies bestimmt die abschließende Patchen-Sequenz.

Ein Patch, der nicht mehr verwendet werden sollte, kann aus der Patchen-Sequenz entfernt werden. Weitere Informationen zum Ausschließen von Patches aus der Patchen-Sequenz finden Sie unter [eliminieren von Patches](eliminating-patches.md).

Ein Beispiel dafür, wie die [msipatchsequence](msipatchsequence-table.md) -Tabelle zum Anwenden von Patches in der Reihenfolge verwendet werden kann, in der Sie erstellt werden, finden Sie im Beispiel für das [mehrfache Patchen](multiple-patching-example.md).

 

 



