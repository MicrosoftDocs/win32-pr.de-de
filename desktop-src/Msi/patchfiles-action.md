---
description: Die PatchFiles-Aktion fragt die Patchtabelle ab, um zu bestimmen, welche Patches angewendet werden sollen. Die PatchFiles-Aktion führt auch das byteweise Patchen der Dateien aus.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: PatchFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6186f150df1871e424b1dc6e4f466d148a1ce2ed51ffd9cd8170a1221e2f0b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082670"
---
# <a name="patchfiles-action"></a>PatchFiles-Aktion

Die PatchFiles-Aktion fragt die [Patchtabelle ab,](patch-table.md) um zu bestimmen, welche Patches angewendet werden sollen. Die PatchFiles-Aktion führt auch das byteweise Patchen der Dateien aus.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Wenn die datei, die gepatcht werden soll, nicht installiert ist, muss die PatchFiles-Aktion nach der [InstallFiles-Aktion,](installfiles-action.md) die die Datei installiert, angezeigt werden. Zuvor installierte Dateien können jederzeit in der Aktionssequenz gepatcht werden. Die [DuplicateFiles-Aktion](duplicatefiles-action.md) muss nach der PatchFiles-Aktion angezeigt werden, um zu verhindern, dass die ungepatchte Version der Datei dupliziert wird.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                    |
|-------|-----------------------------------------------|
| \[1\] | Bezeichner der gepatchten Datei.                   |
| \[2\] | Bezeichner des Verzeichnisses mit gepatchter Datei. |
| \[3\] | Patchgröße in Bytes.                       |



 

 

 



