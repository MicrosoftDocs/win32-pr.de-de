---
description: Der Windows Installer verarbeitet benutzerdefinierte Aktionen als separaten Thread von der Haupt Installation.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Synchrone und asynchrone benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372896"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Synchrone und asynchrone benutzerdefinierte Aktionen

Der Windows Installer verarbeitet benutzerdefinierte Aktionen als separaten Thread von der Haupt Installation. Beim synchronen Ausführen einer benutzerdefinierten Aktion wartet das Installationsprogramm darauf, dass der Thread der benutzerdefinierten Aktion vollständig ausgeführt wird, bevor die Haupt Installation fortgesetzt wird. Während der asynchronen Ausführung führt das Installationsprogramm die benutzerdefinierte Aktion gleichzeitig aus, da die aktuelle Installation fortgesetzt wird. Autoren benutzerdefinierter Aktionen müssen daher alle asynchronen Threads beachten, die möglicherweise Änderungen an der Installations Datenbank zwischen Funktionsaufrufen vornehmen.

Insbesondere sollten Aufrufe von [**msigettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) und [**msisettargetpath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) in asynchronen benutzerdefinierten Aktionen vermieden werden. Verwenden Sie stattdessen [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) zum Abrufen eines Zielpfads. Massendaten Bank Vorgänge, z. b. Import-, Export-und Transformations Vorgänge, sollten in jeder Art von benutzerdefinierter Aktion vermieden werden.

Optionsflags können im type-Feld der [CustomAction-Tabelle](customaction-table.md) festgelegt werden, um anzugeben, dass die Haupt-und benutzerdefinierten aktionsthreads synchron oder asynchron ausgeführt werden. Weitere Informationen finden Sie unter [benutzerdefinierte Aktion Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md).

Das Installationsprogramm kann [benutzerdefinierte Rollbacks-Aktionen](rollback-custom-actions.md) und [gleichzeitige Installations](concurrent-installations.md) Aktionen nur als synchrone benutzerdefinierte Aktionen ausführen.

 

 



