---
description: Mit der Aktion "Aktionen erstellen" werden leere Ordner für Komponenten erstellt, die für die Installation festgelegt sind.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Aktion "kreatefolders"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366241"
---
# <a name="createfolders-action"></a>Aktion "kreatefolders"

Mit der Aktion "Aktionen erstellen" werden leere Ordner für Komponenten erstellt, die für die Installation festgelegt sind. Das Installationsprogramm erstellt Ordner für Komponenten, die lokal ausgeführt werden und von der Quelle ausgeführt werden. Neu erstellte Ordner werden mit dem entsprechenden Komponenten Bezeichner registriert.

Mit der Aktion "Up Folder" werden die Tabelle "die [Tabelle](createfolder-table.md) " und die [Komponenten Tabelle](component-table.md)abgefragt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion "up Folders" muss entweder vor der Aktion " [InstallFiles](installfiles-action.md) " oder vor einer Aktion ausgeführt werden, durch die Dateien zu Ordnern hinzugefügt werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Beschreibung der Aktions Daten |
|-------|----------------------------------------|
| \[1\] | Verzeichnis Bezeichner des Ordners.        |



 

## <a name="remarks"></a>Bemerkungen

Beim Deinstallieren der Anwendung werden von der Aktion "Aktionen erstellen" erstellte Ordner nicht automatisch entfernt. Der Installer entfernt nur Ordner, wenn die Aktion [RemoveFolders](removefolders-action.md) in der Aktions Sequenz enthalten ist.

 

 



