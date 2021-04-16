---
description: Es gibt zwei Möglichkeiten, die Windows Installer-Installations Datenbank zu erstellen, sodass eine Aktion nur beim Deinstallieren des Pakets aufgerufen wird.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Während des Entfernens auszuführende Aufbereitungs Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0e84f21b42f569744af9b8a7a46bb1e3df7a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528646"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Während des Entfernens auszuführende Aufbereitungs Aktionen

Es gibt zwei Möglichkeiten, die Installations Datenbank so zu erstellen, dass eine Aktion nur aufgerufen wird, wenn das Paket deinstalliert wird:

-   Wenn die Aktion nach der [InstallValidate-Aktion](installvalidate-action.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)sequenziert wird, kann der Paket Ersteller für die Aktion in der Spalte Bedingung die Bedingung Remove = "All" angeben. Beachten Sie, dass bei der Deinstallation nicht garantiert wird, dass die Eigenschaft [**Remove**](remove.md) auf all festgelegt ist, bevor der Installer die InstallValidate-Aktion ausführt. Beachten Sie, dass in diesem Fall die Anführungszeichen für den Wert alle erforderlich sind.
-   Wenn die Aktion nach der [Aktion "costfinalize](costfinalize-action.md) " und Aktionen, die den Funktionsstatus ändern können, wie z. b. " [MigrateFeatureStates Action](migratefeaturestates-action.md)", sequenziert werden, kann die Aktion auf den Zustand eines bestimmten Features oder einer bestimmten Komponente fest gebunden werden. Siehe [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md). Verwenden Sie diese Option, um eine Aktion während der Entfernung eines bestimmten Features oder einer Komponente aufzurufen, die möglicherweise außerhalb des kompletten Entfernens der Anwendung stattfindet.

Beachten Sie, dass die [**installierte**](installed.md) Eigenschaft in bedingten Ausdrücken verwendet werden kann, um zu bestimmen, ob ein Produkt pro Computer oder für den aktuellen Benutzer installiert ist. Überprüfen Sie die Eigenschaft [**productstate**](productstate.md) , um zu bestimmen, ob das Produkt für einen anderen Benutzer installiert ist.

Beachten Sie, dass ältere Versionen eines Produkts während eines Upgrades durch die Aktion " [RemoveExistingProducts](removeexistingproducts-action.md)" entfernt werden können. In der [upgradetabelle](upgrade-table.md) kann die [**Remove**](remove.md) -Eigenschaft in diesem Fall auch auf all festgelegt werden. Überprüfen Sie die [**upgradingproductcode**](upgradingproductcode.md) -Eigenschaft, um zu bestimmen, ob ein Produkt durch ein Upgrade entfernt wird. Das Installationsprogramm legt diese Eigenschaft fest, wenn RemoveExistingProducts das Produkt entfernt. Das Installationsprogramm legt die-Eigenschaft nicht während einer normalen Deinstallation fest, z. b. das Entfernen mit der Software.

 

 



