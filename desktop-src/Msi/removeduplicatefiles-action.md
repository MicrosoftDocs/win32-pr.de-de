---
description: Die RemoveDuplicateFiles-Aktion löscht Dateien, die von der DuplicateFiles-Aktion installiert wurden.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: RemoveDuplicateFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7527e7bd4dc66fe4d57f8c23654f1138e781a33064fc0a4a2694987c7ccdb66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074620"
---
# <a name="removeduplicatefiles-action"></a>RemoveDuplicateFiles-Aktion

Die RemoveDuplicateFiles-Aktion löscht Dateien, die von der [DuplicateFiles-Aktion](duplicatefiles-action.md) installiert wurden.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RemoveDuplicateFiles-Aktion muss nach der [InstallValidate-Aktion](installvalidate-action.md) und vor der [InstallFiles-Aktion](installfiles-action.md) erfolgen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                    |
|-------|-----------------------------------------------|
| \[1\] | Bezeichner der entfernten Datei.                   |
| \[9\] | Bezeichner des Verzeichnisses, das die entfernte Datei enthält. |



 

## <a name="remarks"></a>Hinweise

Zum Löschen einer Datei, die mit der [DuplicateFiles-Aktion](duplicatefiles-action.md) mithilfe der RemoveDuplicateFiles-Aktion dupliziert wurde, muss die Komponente, die dem Dateieintrag in der DuplicateFile-Tabelle zugeordnet ist, zum Entfernen ausgewählt werden.

Verwenden Sie die Spalte DestFolder der [DuplicateFile-Tabelle,](duplicatefile-table.md) um den Eigenschaftennamen anzugeben, dessen Wert den Zielordner identifiziert.

 

 



