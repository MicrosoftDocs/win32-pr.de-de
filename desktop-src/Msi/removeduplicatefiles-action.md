---
description: Durch die Aktion RemoveDuplicateFiles werden Dateien gelöscht, die von der duplicatefiles-Aktion installiert wurden.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: RemoveDuplicateFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751121"
---
# <a name="removeduplicatefiles-action"></a>RemoveDuplicateFiles-Aktion

Durch die Aktion RemoveDuplicateFiles werden Dateien gelöscht, die von der [duplicatefiles](duplicatefiles-action.md) -Aktion installiert wurden.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion RemoveDuplicateFiles muss nach der [InstallValidate](installvalidate-action.md) -Aktion und vor der [InstallFiles](installfiles-action.md) -Aktion erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                    |
|-------|-----------------------------------------------|
| \[1\] | Bezeichner der entfernten Datei.                   |
| \[9\] | Der Bezeichner des Verzeichnisses, das die entfernte Datei enthält. |



 

## <a name="remarks"></a>Bemerkungen

Zum Löschen einer Datei, die mit der [Aktion "duplicatefiles](duplicatefiles-action.md) " mithilfe der Aktion "RemoveDuplicateFiles" dupliziert wurde, muss die Komponente, die dem Eintrag der Datei in der duplicatefile-Tabelle zugeordnet ist, zum Entfernen ausgewählt werden.

Verwenden Sie die Spalte destfolder der [duplicatefile-Tabelle](duplicatefile-table.md) , um den Eigenschaftsnamen anzugeben, dessen Wert den Zielordner angibt.

 

 



