---
description: Der Zweck einer benutzerdefinierten Aktion zur verzögerten Ausführung besteht darin, die Ausführung einer Systemänderung auf den Zeitpunkt zu verzögern, zu dem das Installationsskript ausgeführt wird.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Benutzerdefinierte Aktionen für verzögerte Ausführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cec06600fa2cdb447ace579ecf9d19be62e5f4824ecf2d34d77ed879a717d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379177"
---
# <a name="deferred-execution-custom-actions"></a>Benutzerdefinierte Aktionen für verzögerte Ausführung

Der Zweck einer benutzerdefinierten Aktion zur verzögerten Ausführung besteht darin, die Ausführung einer Systemänderung auf den Zeitpunkt zu verzögern, zu dem das Installationsskript ausgeführt wird. Dies unterscheidet sich von einer regulären benutzerdefinierten Aktion oder einer Standardaktion, bei der das Installationsprogramm die Aktion sofort ausführt, wenn sie in einer Sequenztabelle oder in einem Aufruf von [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)gefunden wird. Eine benutzerdefinierte Aktion zur verzögerten Ausführung ermöglicht es einem Paketautor, Systemvorgänge an einem bestimmten Punkt innerhalb der Ausführung des Installationsskripts anzugeben.

Das Installationsprogramm führt zum Zeitpunkt der Verarbeitung der Installationssequenz keine benutzerdefinierte Aktion mit verzögerter Ausführung aus. Stattdessen schreibt das Installationsprogramm die benutzerdefinierte Aktion in das Installationsskript. Der einzige Modusparameter, den das Installationsprogramm in diesem Fall festlegt, ist MSIRUNMODE \_ SCHEDULED. Eine Beschreibung der Parameter für den Ausführungsmodus finden Sie unter [**MsiGetMode.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode)

Eine benutzerdefinierte Aktion für die verzögerte Ausführung muss in der Ausführungssequenztabelle innerhalb des Abschnitts geplant werden, der die Skriptgenerierung ausführt. Benutzerdefinierte Aktionen mit verzögerter Ausführung müssen nach [InstallInitialize](installinitialize-action.md) und in der Aktionssequenz vor [InstallFinalize](installfinalize-action.md) ausgeführt werden.

Benutzerdefinierte Aktionen, die Eigenschaften, Featurezustände, Komponentenzustände oder Zielverzeichnisse festlegen oder Systemvorgänge durch Einfügen von Zeilen in Sequenztabellen planen, können in vielen Fällen die sofortige Ausführung sicher verwenden. Benutzerdefinierte Aktionen, die das System direkt ändern oder einen anderen Systemdienst aufrufen, müssen jedoch auf den Zeitpunkt zurückgestellt werden, zu dem das Installationsskript ausgeführt wird. Weitere Informationen zu möglichen Konflikten zwischen ihren benutzerdefinierten Aktionen und dem Hauptinstallationsthread finden Sie unter [Synchrone und asynchrone benutzerdefinierte](synchronous-and-asynchronous-custom-actions.md) Aktionen.

Da das Installationsskript außerhalb der Installationssitzung ausgeführt werden kann, in der es geschrieben wurde, ist die Sitzung während der Ausführung des Installationsskripts möglicherweise nicht mehr vorhanden. Dies bedeutet, dass das ursprüngliche Sitzungshandle und das Eigenschaftendatensatz während der Installationssequenz für eine benutzerdefinierte Aktion mit verzögerter Ausführung nicht verfügbar sind. Verzögerte benutzerdefinierte Aktionen, die DLLs (Dynamic Link Libraries) aufrufen, übergeben ein Handle, das nur zum Abrufen einer sehr begrenzten Menge von Informationen verwendet werden kann, wie unter [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md)beschrieben.

Beachten Sie, dass verzögerte benutzerdefinierte Aktionen, einschließlich [Rollbacks für benutzerdefinierte Aktionen](rollback-custom-actions.md) und [Commits für benutzerdefinierte Aktionen,](commit-custom-actions.md)die einzigen Arten von Aktionen sind, die außerhalb des Sicherheitskontexts des Benutzers ausgeführt werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte Aktion In-Script Ausführungsoptionen](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> </dl>

 

 



