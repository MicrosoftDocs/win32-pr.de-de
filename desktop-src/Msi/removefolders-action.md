---
description: Die Aktion RemoveFolders entfernt alle Ordner, die mit Komponenten verknüpft sind, die entfernt oder aus der Quelle ausgeführt werden sollen. Diese Ordner werden nur entfernt, wenn sie leer sind. Wenn ein Ordner entfernt wird, wird die Registrierung mit dem entsprechenden Komponentenbezeichner aufgehoben.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: RemoveFolders-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b476de044ef48b50120575a8d6991d27bf063dec37a026a2f5d2ea0e604abee0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082540"
---
# <a name="removefolders-action"></a>RemoveFolders-Aktion

Die Aktion RemoveFolders entfernt alle Ordner, die mit Komponenten verknüpft sind, die entfernt oder aus der Quelle ausgeführt werden sollen. Diese Ordner werden nur entfernt, wenn sie leer sind. Wenn ein Ordner entfernt wird, wird die Registrierung mit dem entsprechenden Komponentenbezeichner aufgehoben.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RemoveFolders-Aktion muss nach der [RemoveFiles-Aktion](removefiles-action.md) oder einer beliebigen Aktion folgen, die Dateien aus Ordnern entfernen kann.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten    |
|-------|-------------------------------|
| \[1\] | Bezeichner des entfernten Ordners. |



 

## <a name="remarks"></a>Hinweise

Das Installationsprogramm entfernt nicht automatisch die Ordner, die während einer Deinstallation der Anwendung durch die [CreateFolders-Aktion](createfolders-action.md) erstellt wurden. Das Installationsprogramm muss angewiesen werden, diese Ordner zu entfernen, indem die Aktion RemoveFolders in der Aktionssequenz erstellt wird.

Um den Namen und Speicherort des Ordners anzugeben, verwenden Sie die \_ Directory-Spalte der [CreateFolder-Tabelle](createfolder-table.md). Jeder Ordnername in der CreateFolder-Tabelle wird als Eigenschaft angenommen, die den Speicherort des Ordners definiert.

Um die Komponente anzugeben, die den Ordner besitzt, verwenden Sie die ComponentId -Spalte der [Component-Tabelle](component-table.md).

 

 



