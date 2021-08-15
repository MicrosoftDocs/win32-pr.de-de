---
description: Commit Benutzerdefinierte Aktionen werden nach erfolgreichem Abschluss des Installationsskripts ausgeführt.
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: Ausführen eines Commits für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a126468df400e23c8eb59885b6e5a66c96d740c0c0e0959320697da293d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380305"
---
# <a name="commit-custom-actions"></a>Ausführen eines Commits für benutzerdefinierte Aktionen

Commit Benutzerdefinierte Aktionen werden nach erfolgreichem Abschluss des Installationsskripts ausgeführt. Wenn die [Aktion InstallFinalize erfolgreich](installfinalize-action.md) ist, werden vom Installationsprogramm alle vorhandenen Benutzerdefinierten Commitaktionen ausgeführt. Der einzige Modusparameter, den das Installationsprogramm in diesem Fall legt, ist MSIRUNMODE \_ COMMIT. Eine Beschreibung der Ausführungsmodusparameter finden Sie unter [**MsiGetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)

Eine benutzerdefinierte Commitaktion kann angegeben werden, indem dem Feld Type der CustomAction-Tabelle ein [Optionsflag hinzugefügt wird.](customaction-table.md) Unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen finden](custom-action-in-script-execution-options.md) Sie das Optionsflag zum Festlegen einer benutzerdefinierten Commitaktion.

Eine benutzerdefinierte Commitaktion ist das Komplement zu einer benutzerdefinierten Rollbackaktion und kann mit benutzerdefinierten [Rollbackaktionen](rollback-custom-actions.md) verwendet werden, um benutzerdefinierte Aktionen umzukehren, die Änderungen direkt am System vornehmen.

Beachten Sie, dass eine benutzerdefinierte Rollbackaktion möglicherweise nicht alle Änderungen entfernen kann, die durch benutzerdefinierte Commitaktionen vorgenommen wurden. Obwohl das Installationsprogramm sowohl rollback- als auch commit-benutzerdefinierte Aktionen in das Rollbackskript schreibt, werden commit-benutzerdefinierte Aktionen nur ausgeführt, nachdem das Installationsskript erfolgreich verarbeitet wurde. Benutzerdefinierte Aktionen ausführen sind die ersten Aktionen, die im Rollbackskript ausgeführt werden. Wenn bei einer benutzerdefinierten Commitaktion ein Fehler auftritt, initiiert das Installationsprogramm ein Rollback, kann aber nur die Vorgänge ausführen, die bereits in das Rollbackskript geschrieben wurden. Dies bedeutet, dass ein Rollback abhängig von der benutzerdefinierten Commitaktion die von der Aktion vorgenommenen Änderungen möglicherweise nicht rückgängig machen kann. Sie können Fehler in benutzerdefinierten Commitaktionen ignorieren, indem Sie die benutzerdefinierte Aktion erstellen, um Rückgabecodes zu ignorieren.

Benutzerdefinierte Aktionen zum Rollback und Commit werden nicht ausgeführt, wenn das Rollback deaktiviert ist. Wenn ein Paketautor diese Arten von benutzerdefinierten Aktionen für die ordnungsgemäße Installation benötigt, sollte er die [**RollbackDisabled-Eigenschaft**](rollbackdisabled.md) in einer Bedingung verwenden, die verhindert, dass die Installation fortgesetzt wird, wenn das Rollback deaktiviert ist.

 

 



