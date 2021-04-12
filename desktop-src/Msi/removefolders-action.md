---
description: Die Aktion RemoveFolders entfernt alle Ordner, die mit Komponenten verknüpft sind, die entfernt oder aus der Quelle ausgeführt werden sollen. Diese Ordner werden nur entfernt, wenn Sie leer sind. Wenn ein Ordner entfernt wird, wird die Registrierung mit dem entsprechenden Komponenten Bezeichner aufgehoben.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: RemoveFolders-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216935"
---
# <a name="removefolders-action"></a>RemoveFolders-Aktion

Die Aktion RemoveFolders entfernt alle Ordner, die mit Komponenten verknüpft sind, die entfernt oder aus der Quelle ausgeführt werden sollen. Diese Ordner werden nur entfernt, wenn Sie leer sind. Wenn ein Ordner entfernt wird, wird die Registrierung mit dem entsprechenden Komponenten Bezeichner aufgehoben.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die RemoveFolders-Aktion muss nach der [RemoveFiles](removefiles-action.md) -Aktion oder einer beliebigen Aktion erfolgen, die möglicherweise Dateien aus Ordnern entfernt.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten    |
|-------|-------------------------------|
| \[1\] | Der Bezeichner des entfernten Ordners. |



 

## <a name="remarks"></a>Bemerkungen

Der Installer entfernt nicht automatisch die Ordner, die von der [Aktion](createfolders-action.md) "Erstellungs Ordner" während einer Deinstallieren der Anwendung erstellt wurden. Das Installationsprogramm muss angewiesen werden, diese Ordner zu entfernen, indem Sie die RemoveFolders-Aktion in der Aktions Sequenz erstellen.

Um den Namen und den Speicherort des Ordners anzugeben, verwenden Sie die \_ Spalte Verzeichnis der [Tabelle "Tabelle](createfolder-table.md)". Es wird davon ausgegangen, dass jeder Ordnername in der Tabelle "foratefolder" eine Eigenschaft ist, die den Ordner Speicherort definiert.

Um die Komponente anzugeben, die den Ordner besitzt, verwenden Sie die Spalte ComponentID der [Component-Tabelle](component-table.md).

 

 



