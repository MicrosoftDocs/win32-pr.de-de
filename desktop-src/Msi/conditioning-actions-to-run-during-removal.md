---
description: Es gibt zwei Möglichkeiten, die Installationsdatenbank Windows Installer so zu erstellen, dass eine Aktion nur aufgerufen wird, wenn das Paket deinstalliert wird.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Durchführen von Aktionen, die während des Entfernens ausgeführt werden sollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fa9596dd6868b105f87c795ad70b6edc5ebac96381ffcc2b8b951947c87568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144323"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Durchführen von Aktionen, die während des Entfernens ausgeführt werden sollen

Es gibt zwei Möglichkeiten, die Installationsdatenbank so zu erstellen, dass eine Aktion nur aufgerufen wird, wenn das Paket deinstalliert wird:

-   Wenn die Aktion nach der [InstallValidate-Aktion](installvalidate-action.md) in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md)sequenziert wird, kann der Paketautor die Bedingung REMOVE="ALL" für die Aktion in der Spalte Bedingung angeben. Beachten Sie, dass die [**REMOVE-Eigenschaft**](remove.md) während einer Deinstallation nicht garantiert auf ALL festgelegt wird, bevor das Installationsprogramm die InstallValidate-Aktion ausführt. Beachten Sie, dass die Anführungszeichen um den Wert ALL in diesem Fall erforderlich sind.
-   Wenn die Aktion nach der [CostFinalize-Aktion](costfinalize-action.md) und allen Aktionen sequenziert wird, die den Featurezustand ändern könnten, z. B. [die MigrateFeatureStates-Aktion,](migratefeaturestates-action.md)kann die Aktion auf den Zustand eines bestimmten Features oder einer bestimmten Komponente bedingte werden. Weitere Informationen finden Sie unter [Syntax der bedingten Anweisung.](conditional-statement-syntax.md) Verwenden Sie diese Option, um während des Entfernens einer bestimmten Funktion oder Komponente eine Aktion aufzurufen, die außerhalb des vollständigen Entfernens der Anwendung auftreten kann.

Beachten Sie, dass die Eigenschaft Installiert in [**bedingten**](installed.md) Ausdrücken verwendet werden kann, um zu bestimmen, ob ein Produkt pro Computer oder für den aktuellen Benutzer installiert ist. Überprüfen Sie die [**ProductState-Eigenschaft,**](productstate.md) um zu bestimmen, ob das Produkt für einen anderen Benutzer installiert ist.

Beachten Sie, dass ältere Versionen eines Produkts während eines Upgrades durch die [Aktion RemoveExistingProducts](removeexistingproducts-action.md)entfernt werden können. Die [Tabelle Upgrade](upgrade-table.md) kann in diesem Fall auch die [**REMOVE-Eigenschaft**](remove.md) auf ALL festlegen. Überprüfen Sie die [**UPGRADINGPRODUCTCODE-Eigenschaft,**](upgradingproductcode.md) um zu ermitteln, ob ein Produkt durch ein Upgrade entfernt wird. Das Installationsprogramm legt diese Eigenschaft nur fest, wenn RemoveExistingProducts das Produkt entfernt. Das Installationsprogramm legt die -Eigenschaft während einer normalen Deinstallation nicht fest, z. B. beim Entfernen mit Programmen zum Hinzufügen/Entfernen.

 

 



