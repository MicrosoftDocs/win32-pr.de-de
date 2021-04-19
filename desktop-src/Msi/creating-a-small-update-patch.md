---
description: Befolgen Sie die folgenden Richtlinien, wenn Sie einen Patch für ein Windows Installer kleines Update erstellen.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Erstellen eines kleinen Update-Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359544"
---
# <a name="creating-a-small-update-patch"></a>Erstellen eines kleinen Update-Patches

Beim Erstellen eines Patches für [kleine Updates](small-updates.md)sollten Autoren die folgenden Richtlinien befolgen:

-   Kleine Updatepatches müssen für eine einzelne Ziel Installation entworfen werden.
-   Für kleine Updatepatches sollte die früheste Version als Ziel Installation verwendet werden.
-   Ein kleiner Update Patch sollte alle früheren kleinen Updatepatches ersetzen und veraltete Dateien als veraltet festlegen.

Im folgenden Szenario wird veranschaulicht, wann ein kleines Update Patch am besten geeignet ist.

Ihr Unternehmen wird in Version 1,0 von Myproduct.msi ausgeliefert. Kurz danach liefern Sie einen [kleinen Update](small-updates.md) Patch für Myproduct.msi mit dem Namen QFE1. Dadurch wird die [**ProductCode**](productcode.md) -Eigenschaft oder die [**ProductVersion**](productversion.md) -Eigenschaft nicht geändert.

Später erstellen Sie einen zweiten [kleinen Update](small-updates.md) Patch für Myproduct.msi mit dem Namen QFE2. Dieser zweite Patch muss auf Myproduct.msi Version 1,0 ausgerichtet sein. Dieser zweite Patch darf nicht sowohl Myproduct.msi Version 1,0 als auch Myproduct.msi Version 1,0 + QFE1 als Ziel haben. Wenn QFE2 angewendet wird, sollte QFE1 entfernt werden.

 

 



