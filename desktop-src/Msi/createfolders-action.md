---
description: Die Aktion CreateFolders erstellt leere Ordner für Komponenten, die für die Installation festgelegt sind.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: CreateFolders-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61182143488627c4724e470bf7f5158ed524cb4bc344c972c6744d14f773f6cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105270"
---
# <a name="createfolders-action"></a>CreateFolders-Aktion

Die Aktion CreateFolders erstellt leere Ordner für Komponenten, die für die Installation festgelegt sind. Das Installationsprogramm erstellt Ordner für Komponenten, die lokal und aus der Quelle ausgeführt werden. Neu erstellte Ordner werden mit dem entsprechenden Komponentenbezeichner registriert.

Die CreateFolders-Aktion fragt die [CreateFolder-Tabelle und](createfolder-table.md) die [Component-Tabelle ab.](component-table.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die CreateFolders-Aktion muss entweder vor der [InstallFiles-Aktion](installfiles-action.md) oder vor jeder Aktion ausgeführt werden, die Dateien zu Ordnern hinzufügt.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Beschreibung der Aktionsdaten |
|-------|----------------------------------------|
| \[1\] | Verzeichnisbezeichner des Ordners.        |



 

## <a name="remarks"></a>Hinweise

Das Installationsprogramm entfernt ordner, die während einer Deinstallation der Anwendung von der CreateFolders-Aktion erstellt wurden, nicht automatisch. Das Installationsprogramm entfernt Ordner nur, wenn die [RemoveFolders-Aktion](removefolders-action.md) in der Aktionssequenz enthalten ist.

 

 



