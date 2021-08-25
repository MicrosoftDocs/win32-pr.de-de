---
description: Ein Patch, der nicht mehr verwendet werden soll, kann aus der Patchsequenz entfernt werden.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Entfernen von Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f025c6487293d07df7963514b79f551045398f8d86f51dd7ab98b589a605e762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913520"
---
# <a name="eliminating-patches"></a>Entfernen von Patches

Ein Patch, der nicht mehr verwendet werden soll, kann aus der Patchsequenz entfernt werden. Dadurch wird verhindert, dass der Patch angewendet wird, wenn die Zielanwendung gepatcht wird. Dies ist anders als das Entfernen eines Patches, der bereits auf eine Anwendung angewendet wird. Informationen zum Entfernen von angewendeten Patches finden Sie unter [Entfernen von Patches.](removing-patches.md)

**Windows Installer 3.0 und höher: **

Patches mit der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) können diese Tabelle verwenden, um Patches aus der Patchsequenz zu beseitigen. Ein Patch kann Patches beseitigen, die in der Patchsequenz vor ihm enthalten sind, und die Informationen aus diesen Patches durch eigene Informationen ersetzen. Sowohl der Patch, der angibt, welche Patches entfernt werden sollen, als auch die zu beseitigenden Patches müssen über eine MsiPatchSequence-Tabelle mit Informationen verfügen.

Wenn die entfernten Patches und der Ersatzpatch keine [MsiPatchSequence-Tabellen](msipatchsequence-table.md) enthalten, kann das Patchpaket eine Liste der Patches angeben, die aus der Patchsequenz entfernt werden sollen, in der Eigenschaft [**Zusammenfassung**](revision-number-summary.md) der Revisionsnummer. Windows Installer 3.0 ignoriert diese Liste, wenn entweder die entfernten patches oder Ersatzpatches über eine MsiPatchSequence-Tabelle verfügen.

Wenn das Patchpaket Patches mit Sequenzinformationen in der [Tabelle MsiPatchSequence](msipatchsequence-table.md) und einige Patches ohne diese Informationen enthält, sequenziert Windows Installer 3.0 die Patches in der im folgenden Abschnitt beschriebenen Reihenfolge: Sequenzieren von [Patches](sequencing-patches.md).

Beispielsweise können Patch1, Patch2 und Patch3 drei Patches sein, die nicht über die [Tabelle MsiPatchSequence](msipatchsequence-table.md) verfügen. Patch2 kann ein Patch sein, der nur anwendbar ist, wenn Patch1 bereits auf die Anwendung angewendet wurde. Patch3 kann ein späterer Patch sein, der alle Informationen in Patch1 enthält und Patch1 auch aus der Patchsequenz entfernt. Dies bedeutet, dass Patch 2 bei Anwendung von Patch3 ebenfalls nicht mehr angewendet werden kann, da patch1 erforderlich ist. Alle Informationen in Patch2 allein werden nicht an die Anwendung übermittelt.

**Windows Installer 2.0:** Nicht unterstützt. Die einzige verfügbare Methode besteht in der Angabe der Liste der Patches, die aus der Patchsequenz entfernt werden sollen, in der [**Eigenschaft Zusammenfassung der Revisionsnummer.**](revision-number-summary.md)

> [!Note]  
> Patchautoren sollten die [**Funktionen MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) und [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) verwenden, um die Sequenz von Patches zu bestimmen, die tatsächlich auf das Produkt angewendet werden, da die Entfernung einiger Patches andere Patches unanbrauchbar machen kann.

 

 

 



