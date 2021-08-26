---
description: Ab Windows Installer 3.0 können mehrere Patches in konstanter Reihenfolge auf ein Produkt angewendet werden, unabhängig von der Reihenfolge, in der die Patches für das System bereitgestellt werden.
ms.assetid: 10af1857-d59f-490d-9b50-49619b1e892c
title: Installieren mehrerer Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dc6b65997bd6bcb2b9f4c8da5022adda9a38b0b93401dc507397421799d260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893850"
---
# <a name="installing-multiple-patches"></a>Installieren mehrerer Patches

Ab Windows Installer 3.0 können mehrere Patches in konstanter Reihenfolge auf ein Produkt angewendet werden, unabhängig von der Reihenfolge, in der die Patches für das System bereitgestellt werden.

**Windows Installer 2.0:** Nicht unterstützt. Windows Installationsprogrammversionen vor Version 3.0 installieren Patches immer in der Reihenfolge, in der sie für das System bereitgestellt werden.

**Windows Installer 3.0 und höher:** Das Installationsprogramm kann die Informationen in der [Tabelle MsiPatchSequence](msipatchsequence-table.md) verwenden, um zu bestimmen, welche Patches auf das Windows Installer-Paket anwendbar sind und in welcher Reihenfolge die Patches angewendet werden sollen. Anwendungen können die [**Funktionen MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) und [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) verwenden.

Die [**MsiDetermineApplicablePatches-Funktion**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) bestimmt, welche Patches für das Paket Windows Installer gelten und in welcher Reihenfolge. Die Funktion kann ersetzte oder veraltete Patches berücksichtigen. Diese Funktion berücksichtigt keine Produkte oder Patches, die auf dem System installiert sind und nicht in der Gruppe angegeben sind.

Die [**MsiDeterminePatchSequence Sequence-Funktion**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) kann die beste Sequenz der Anwendung für die Patches für ein angegebenes installiertes Produkt bestimmen. Diese Funktion ermöglicht Patches, die bereits auf das Produkt angewendet wurden, sowie veraltete und ersetzte Patches.

Wenn das Patchpaket nicht über eine [MsiPatchSequence-Tabelle](msipatchsequence-table.md) verfügt, wendet das Installationsprogramm die Patches immer in der Reihenfolge an, in der sie für das System bereitgestellt werden.

Wenn das Patchpaket eine Mischung aus Patches mit Sequenzinformationen in der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) und einigen Patches ohne diese Informationen enthält, sequenziert Windows Installer Version 3.0 die Patches in der im folgenden Abschnitt beschriebenen Reihenfolge: [Sequenzierungspatches](sequencing-patches.md).

Ein Windows Installer-Paket kann beim Installieren oder Aktualisieren einer Anwendung nicht mehr als 127 Patches installieren. Wenn viele Updates erforderlich sind, sollten sie kombiniert und vorherige veraltete Patches aus der Patchsequenz entfernt werden.

Ein Patch, der nicht verwendet werden sollte, kann aus der Patchsequenz entfernt werden. Dadurch wird verhindert, dass der Patch angewendet wird, wenn die Zielanwendung gepatcht wird. Dies ist anders als das Entfernen eines Patches, der bereits auf eine Anwendung angewendet wurde. Weitere Informationen zum Entfernen von Patches aus der Patchsequenz finden Sie unter [Entfernen von Patches](eliminating-patches.md). Informationen zum Entfernen von angewendeten Patches finden Sie unter [Entfernen von Patches.](removing-patches.md)

Ein Beispiel dafür, wie Windows Installer mehrere Patches wendet, wenn alle [MsiPatchSequence-Tabellen](msipatchsequence-table.md) enthalten, finden Sie im [Beispiel für mehrere Patches.](multiple-patching-example.md)

 

 



