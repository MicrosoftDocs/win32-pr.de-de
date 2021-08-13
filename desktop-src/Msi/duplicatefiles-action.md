---
description: Die DuplicateFiles-Aktion dupliziert Dateien, die von der InstallFiles-Aktion installiert wurden. Die duplizierten Dateien können in dasselbe Verzeichnis mit einem anderen Namen oder in ein anderes Verzeichnis mit dem ursprünglichen Namen kopiert werden.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: DuplicateFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7969440aed4361ad264baa0d30a9c1d16f0ca673c72a2a7c3c1326e5d393ffc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637712"
---
# <a name="duplicatefiles-action"></a>DuplicateFiles-Aktion

Die DuplicateFiles-Aktion dupliziert Dateien, die von der [InstallFiles-Aktion installiert](installfiles-action.md) wurden. Die duplizierten Dateien können in dasselbe Verzeichnis mit einem anderen Namen oder in ein anderes Verzeichnis mit dem ursprünglichen Namen kopiert werden.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die DuplicateFiles-Aktion muss nach der [InstallFiles-Aktion kommen.](installfiles-action.md) Die DuplicateFiles-Aktion muss auch nach der [PatchFiles-Aktion](patchfiles-action.md) angezeigt werden, um zu verhindern, dass die ungepatchte Version der Datei dupliziert wird.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                       |
|-------|--------------------------------------------------|
| \[1\] | Bezeichner der duplizierten Datei.                   |
| \[6\] | Größe der duplizierten Datei.                         |
| \[9\] | Bezeichner des Verzeichnisses, das eine duplizierte Datei enthält. |



 

## <a name="remarks"></a>Hinweise

Die DuplicateFiles-Aktion verarbeitet einen [DuplicateFile-Tabelleneintrag](duplicatefile-table.md) nur, wenn die mit diesem Eintrag verknüpfte Komponente lokal installiert wird. Weitere Informationen finden Sie in der [Komponententabelle](component-table.md).

Die Zeichenfolge im Feld DestFolder ist ein Eigenschaftsname, dessen Wert in einen vollqualifizierten Pfad aufzulösen ist. Diese Eigenschaft kann entweder einer der [](directory-table.md) Verzeichniseinträge in der Directory-Tabelle, eine vordefinierte Ordnereigenschaft (z. B.[**CommonFilesFolder)**](commonfilesfolder.md)oder eine Eigenschaft sein, die durch einen beliebigen Eintrag in der [AppSearch-Tabelle](appsearch-table.md) festgelegt wird. Wenn die **DestFolder-Eigenschaft** nicht zu einem gültigen Pfad ausgewertet wird, führt die DuplicateFiles-Aktion nichts für diesen Eintrag aus.

Wenn der Name der Zieldatei in der Spalte DestName der DuplicateFile-Tabelle leer gelassen wird, ist der Name der Zieldatei mit dem ursprünglichen Dateinamen identisch.

Dateien, die von der DuplicateFiles-Aktion installiert werden, werden gegebenenfalls durch die [RemoveDuplicateFiles-Aktion](removeduplicatefiles-action.md) entfernt.

 

 



