---
description: Ab Windows Installer 3,0 können mehrere Patches in konstanter Reihenfolge auf ein Produkt angewendet werden, unabhängig von der Reihenfolge, in der die Patches dem System bereitgestellt werden.
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: Installieren mehrerer Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4edb8d085ede6aee81690bf67bd9c5e19780ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368170"
---
# <a name="installing-multiple-patches"></a>Installieren mehrerer Patches

Ab Windows Installer 3,0 können mehrere Patches in konstanter Reihenfolge auf ein Produkt angewendet werden, unabhängig von der Reihenfolge, in der die Patches dem System bereitgestellt werden.

**Windows Installer 2,0:** Nicht unterstützt. In Windows Installer Versionen vor Version 3,0 werden Patches immer in der Reihenfolge installiert, in der Sie dem System bereitgestellt werden.

**Windows Installer 3,0 und höher:** Das Installationsprogramm kann anhand der Informationen in der [msipatchsequence](msipatchsequence-table.md) -Tabelle bestimmen, welche Patches für das Windows Installer Paket anwendbar sind und in welcher Reihenfolge die Patches angewendet werden sollen. Anwendungen können die [**msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) -Funktion und die [**msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) -Funktion verwenden.

Die [**msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) -Funktion bestimmt, welche Patches auf das Windows Installer Paket und in welcher Reihenfolge angewendet werden. Die Funktion kann abgelösten oder veraltete Patches berücksichtigen. Diese Funktion berücksichtigt keine Produkte oder Patches, die auf dem System installiert sind, die nicht in der Gruppe angegeben sind.

Die [**msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) -Sequenz Funktion kann die beste Sequenz der Anwendung für die Patches für ein angegebenes installiertes Produkt bestimmen. Diese Funktion berücksichtigt Patches, die bereits auf das Produkt angewendet wurden, sowie Konten für veraltete und abgelösten Patches.

Wenn das Patchpaket nicht über eine [msipatchsequence](msipatchsequence-table.md) -Tabelle verfügt, wendet das Installationsprogramm die Patches immer in der Reihenfolge an, in der Sie dem System bereitgestellt werden.

Wenn das Patchpaket eine Mischung aus Patches mit Sequenz Informationen in der [msipatchsequence](msipatchsequence-table.md) -Tabelle und einigen Patches ohne diese Informationen enthält, sequenziert Windows Installer Version 3,0 die Patches in der Reihenfolge, die im folgenden Abschnitt beschrieben wird: [Sequenzieren von Patches](sequencing-patches.md).

Beim Installieren oder Aktualisieren einer Anwendung können von einem Windows Installer Paket nicht mehr als 127 Patches installiert werden. Wenn viele Updates erforderlich sind, sollten Sie kombiniert werden, und vorherige veraltete Patches sollten aus der Patchen-Sequenz entfernt werden.

Ein Patch, der nicht verwendet werden sollte, kann aus der Patchen-Sequenz entfernt werden. Dadurch wird verhindert, dass der Patch angewendet wird, wenn die Zielanwendung gepatcht wird. Dies unterscheidet sich von dem Entfernen eines Patches, der bereits auf eine Anwendung angewendet wurde. Weitere Informationen zum Entfernen von Patches aus der Patchen-Sequenz finden Sie unter [eliminieren von Patches](eliminating-patches.md). Weitere Informationen zum Entfernen von angewendeten Patches finden Sie unter [Entfernen von Patches](removing-patches.md).

Ein Beispiel dafür, wie Windows Installer mehrere Patches anwendet, wenn alle über [msipatchsequence](msipatchsequence-table.md) -Tabellen verfügen, finden Sie im Beispiel für das [mehrfache Patchen](multiple-patching-example.md).

 

 



