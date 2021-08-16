---
description: Halten Sie sich an die folgenden Richtlinien, wenn Sie einen Patch für ein kleines update Windows Installer erstellen.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Erstellen eines kleinen Updatepatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2c3dffac099358b924914b5dbd86871ba370241c42a2e3fd5caef2d8f12ff4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379395"
---
# <a name="creating-a-small-update-patch"></a>Erstellen eines kleinen Updatepatches

Beim Erstellen eines Patches [für kleine Updates](small-updates.md)sollten Autoren die folgenden Richtlinien einhalten:

-   Kleine Updatepatches müssen für eine einzelne Zielinstallation entworfen werden.
-   Für kleine Updatepatches sollte die früheste Version als Zielinstallation verwendet werden.
-   Ein kleiner Updatepatch sollte alle früheren kleinen Updatepatches ersetzen und veraltet machen.

Das folgende Szenario veranschaulicht, wann ein kleiner Updatepatch am besten ist.

Ihr Unternehmen liefert Version 1.0 der Myproduct.msi. Kurz darauf versenden Sie einen kleinen [Updatepatch](small-updates.md) für Myproduct.msi QFE1. Dadurch wird weder die [**ProductCode-Eigenschaft**](productcode.md) noch die [**ProductVersion-Eigenschaft**](productversion.md) geändert.

Später erstellen Sie einen zweiten kleinen [Updatepatch](small-updates.md) für Myproduct.msi QFE2. Dieser zweite Patch muss auf Myproduct.msi 1.0. Dieser zweite Patch darf nicht sowohl auf Myproduct.msi 1.0 als auch auf Myproduct.msi 1.0 + QFE1. Wenn QFE2 angewendet wird, sollte QFE1 entfernt werden.

 

 



