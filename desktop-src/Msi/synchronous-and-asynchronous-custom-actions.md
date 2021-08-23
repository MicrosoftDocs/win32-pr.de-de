---
description: Der Windows-Installer verarbeitet benutzerdefinierte Aktionen als separaten Thread von der Hauptinstallation.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Synchrone und asynchrone benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ffa9de75d81cfe0c824bab0580f0e6565567a187f768d99687169b47543a41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893610"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Synchrone und asynchrone benutzerdefinierte Aktionen

Der Windows-Installer verarbeitet benutzerdefinierte Aktionen als separaten Thread von der Hauptinstallation. Während der synchronen Ausführung einer benutzerdefinierten Aktion wartet das Installationsprogramm, bis der Thread der benutzerdefinierten Aktion abgeschlossen ist, bevor die Hauptinstallation fortgesetzt wird. Während der asynchronen Ausführung führt das Installationsprogramm die benutzerdefinierte Aktion gleichzeitig aus, während die aktuelle Installation fortgesetzt wird. Autoren benutzerdefinierter Aktionen müssen daher alle asynchronen Threads kennen, die zwischen Funktionsaufrufen Änderungen an der Installationsdatenbank vornehmen können.

Insbesondere sollten Aufrufe von [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) und [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) in asynchronen benutzerdefinierten Aktionen vermieden werden. Verwenden Sie [**stattdessen MsiGetProperty,**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) um einen Zielpfad zu erhalten. Massendatenbankvorgänge wie Import-, Export- und Transformationsvorgänge sollten bei jeder Art benutzerdefinierter Aktionen vermieden werden.

Optionsflags können im Feld Typ der [CustomAction-Tabelle](customaction-table.md) festgelegt werden, um anzugeben, dass die Hauptthreads und benutzerdefinierten Aktionsthreads synchron oder asynchron ausgeführt werden. Weitere Informationen finden [Sie unter Rückgabeverarbeitungsoptionen für benutzerdefinierte Aktionen.](custom-action-return-processing-options.md)

Das Installationsprogramm kann benutzerdefinierte [Rollbackaktionen und](rollback-custom-actions.md) Gleichzeitige [Installationsaktionen](concurrent-installations.md) nur als synchrone benutzerdefinierte Aktionen ausführen.

 

 



