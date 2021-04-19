---
description: Die duplicatefiles-Aktion dupliziert Dateien, die von der InstallFiles-Aktion installiert wurden. Die doppelten Dateien können in dasselbe Verzeichnis mit einem anderen Namen oder in ein anderes Verzeichnis mit dem ursprünglichen Namen kopiert werden.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Duplicatefiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360604"
---
# <a name="duplicatefiles-action"></a>Duplicatefiles-Aktion

Die duplicatefiles-Aktion dupliziert Dateien, die von der [InstallFiles](installfiles-action.md) -Aktion installiert wurden. Die doppelten Dateien können in dasselbe Verzeichnis mit einem anderen Namen oder in ein anderes Verzeichnis mit dem ursprünglichen Namen kopiert werden.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion "duplicatefiles" muss nach der [Aktion "InstallFiles](installfiles-action.md)" erfolgen. Die duplicatefiles-Aktion muss auch nach der [PATCHFILES-Aktion](patchfiles-action.md) erfolgen, um zu verhindern, dass die nicht gepatchte Version der Datei duplizieren.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                       |
|-------|--------------------------------------------------|
| \[1\] | Bezeichner der duplizierten Datei.                   |
| \[6\] | Größe der duplizierten Datei.                         |
| \[9\] | Der Bezeichner des Verzeichnisses, das die doppelte Datei enthält. |



 

## <a name="remarks"></a>Bemerkungen

Die duplicatefiles-Aktion verarbeitet einen [duplicatefile-Tabellen](duplicatefile-table.md) Eintrag nur dann, wenn die mit diesem Eintrag verknüpfte Komponente lokal installiert wird. Weitere Informationen finden Sie unter [Component Table](component-table.md).

Die Zeichenfolge im Feld "destfolder" ist ein Eigenschaftsname, dessen Wert in einen voll qualifizierten Pfad aufgelöst werden soll. Diese Eigenschaft kann entweder ein beliebiger Verzeichniseintrag in der [Verzeichnis](directory-table.md) Tabelle, eine vordefinierte Ordner Eigenschaft (z. b.[**CommonFilesFolder**](commonfilesfolder.md)) oder eine Eigenschaft sein, die von einem beliebigen Eintrag in der [AppSearch](appsearch-table.md) -Tabelle festgelegt wird. Wenn die **destfolder** -Eigenschaft nicht als gültiger Pfad ausgewertet wird, führt die duplicatefiles-Aktion für diesen Eintrag keine Aktion aus.

Wenn der Name der Zieldatei in der Spalte destname der duplicatefile-Tabelle leer bleibt, entspricht der Name der Ziel Datei dem ursprünglichen Dateinamen.

Dateien, die von der duplicatefiles-Aktion installiert werden, werden bei Bedarf von der Aktion " [RemoveDuplicateFiles](removeduplicatefiles-action.md) " entfernt.

 

 



