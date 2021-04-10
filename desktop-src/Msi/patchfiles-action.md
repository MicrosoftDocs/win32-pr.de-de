---
description: Mit der Aktion PATCHFILES wird die patchtabelle abgefragt, um zu bestimmen, welche Patches angewendet werden sollen. Die Aktion "PATCHFILES" führt auch das Byte Weise Patchen der Dateien aus.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Aktion "PATCHFILES"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865212"
---
# <a name="patchfiles-action"></a>Aktion "PATCHFILES"

Mit der Aktion PATCHFILES wird die [patchtabelle](patch-table.md) abgefragt, um zu bestimmen, welche Patches angewendet werden sollen. Die Aktion "PATCHFILES" führt auch das Byte Weise Patchen der Dateien aus.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Wenn die Datei, die gepatcht werden soll, nicht installiert ist, muss die PATCHFILES-Aktion nach der [InstallFiles-Aktion](installfiles-action.md) erfolgen, mit der die Datei installiert wird. Zuvor installierte Dateien können an einem beliebigen Punkt in der Aktions Sequenz gepatcht werden. Die [duplicatefiles-Aktion](duplicatefiles-action.md) muss nach der PATCHFILES-Aktion erfolgen, um zu verhindern, dass die nicht gepatchte Version der Datei duplizieren.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                    |
|-------|-----------------------------------------------|
| \[1\] | Bezeichner der gepatchten Datei.                   |
| \[2\] | Der Bezeichner des Verzeichnisses mit gepatchten Datei. |
| \[3\] | Größe des Patches in Bytes.                       |



 

 

 



