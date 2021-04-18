---
description: Ein Patch, der nicht mehr verwendet werden sollte, kann aus der Patchen-Sequenz entfernt werden.
ms.assetid: b1d499d9-4fd3-4996-84a1-c32acefbb98f
title: Entfernen von Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a705ce5919ffd36e6fc860403e11db56c6df1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345227"
---
# <a name="eliminating-patches"></a>Entfernen von Patches

Ein Patch, der nicht mehr verwendet werden sollte, kann aus der Patchen-Sequenz entfernt werden. Dadurch wird verhindert, dass der Patch angewendet wird, wenn die Zielanwendung gepatcht wird. Dies unterscheidet sich vom Entfernen eines Patches, der bereits auf eine Anwendung angewendet wurde. Weitere Informationen zum Entfernen von angewendeten Patches finden Sie unter [Entfernen von Patches](removing-patches.md).

* * Windows Installer 3,0 und höher: * *

Patches, die über die [msipatchsequence](msipatchsequence-table.md) -Tabelle verfügen, können diese Tabelle verwenden, um Patches aus der Patchen-Sequenz auszuschließen. Ein Patch kann Patches entfernen, die in der patchingsequenz vor ihm stehen, und die Informationen aus diesen Patches durch eigene Informationen ersetzen. Sowohl der Patch, der angibt, welche Patches gelöscht werden sollen, als auch die Patches, die entfernt werden, müssen über eine msipatchsequence-Tabelle verfügen, die Informationen

Wenn das Patchen der Patches und Ersetzung keine [msipatchsequence](msipatchsequence-table.md) -Tabellen hat, kann das Patchpaket eine Liste der Patches angeben, die aus der Patchen-Sequenz in der [**Revisionsnummer der Revisionsnummer**](revision-number-summary.md) entfernt werden sollen. In Windows Installer 3,0 wird diese Liste ignoriert, wenn die Patches oder Ersatz Patches eine msipatchsequence-Tabelle aufweisen.

Wenn das Patchpaket Patches mit Sequenz Informationen in der [msipatchsequence](msipatchsequence-table.md) -Tabelle und einige Patches ohne diese Informationen enthält, sequenziert Windows Installer 3,0 die Patches in der Reihenfolge, die im folgenden Abschnitt beschrieben wird: [Sequenzieren von Patches](sequencing-patches.md).

Patch1, Patch2 und Patch3 können z. b. drei Patches sein, die nicht die [msipatchsequence](msipatchsequence-table.md) -Tabelle aufweisen. Patch2 kann ein Patch sein, der nur anwendbar ist, wenn Patch1 bereits auf die Anwendung angewendet wurde. Patch3 kann ein späterer Patch sein, der alle Informationen in Patch1 enthält und auch Patch1 aus der Patchen-Sequenz entfernt. Dies bedeutet, dass Patch 2, wenn Patch3 angewendet wird, auch nicht mehr anwendbar ist, da hierfür Patch1 erforderlich ist. Alle Informationen in Patch2 allein werden nicht an die Anwendung übermittelt.

**Windows Installer 2,0:** Nicht unterstützt. Die einzige verfügbare Methode besteht darin, die Liste der Patches anzugeben, die aus der Patchen-Sequenz in der [**Revisionsnummer-Zusammenfassungs**](revision-number-summary.md) Eigenschaft gelöscht werden sollen.

> [!Note]  
> Patchautoren sollten die [**msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) -Funktion und die [**msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) -Funktion verwenden, um die Abfolge der Patches zu ermitteln, die tatsächlich auf das Produkt angewendet werden, da durch die Löschung einiger Patches andere Patches nicht anwendbar gerendert werden können.

 

 

 



