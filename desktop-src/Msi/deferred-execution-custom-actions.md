---
description: Der Zweck einer benutzerdefinierten Aktion für eine verzögerte Ausführung besteht darin, die Ausführung einer Systemänderung auf den Zeitpunkt der Ausführung des Installations Skripts zu verzögern.
ms.assetid: 79bf4d0b-624d-4652-8c4f-0ecd928a88e3
title: Benutzerdefinierte Aktionen für verzögerte Ausführung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09b91793f5d5bbc7be7099c92f8d8f212012d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960063"
---
# <a name="deferred-execution-custom-actions"></a>Benutzerdefinierte Aktionen für verzögerte Ausführung

Der Zweck einer benutzerdefinierten Aktion für eine verzögerte Ausführung besteht darin, die Ausführung einer Systemänderung auf den Zeitpunkt der Ausführung des Installations Skripts zu verzögern. Dies unterscheidet sich von einer regulären benutzerdefinierten Aktion oder einer Standardaktion, bei der das Installationsprogramm die Aktion unmittelbar nach dem Auffinden in einer Sequenz Tabelle oder in einem [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)-Aufrufvorgang ausführt. Eine benutzerdefinierte Aktion für die verzögerte Ausführung ermöglicht einem Paket Ersteller, System Vorgänge an einem bestimmten Punkt innerhalb der Ausführung des Installations Skripts anzugeben.

Der Installer führt zum Zeitpunkt der Verarbeitung der Installations Sequenz keine benutzerdefinierte Aktion für die verzögerte Ausführung aus. Stattdessen schreibt der Installer die benutzerdefinierte Aktion in das Installationsskript. Der einzige Modusparameter, der vom Installer festgelegt wird, ist msirunmode \_ geplant. Unter [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) finden Sie eine Beschreibung der Parameter für den Testlauf.

Eine benutzerdefinierte Aktion für die verzögerte Ausführung muss in der Sequenz Tabelle ausführen innerhalb des Abschnitts, der die Skript Generierung ausführt, geplant werden. Benutzerdefinierte Aktionen der verzögerten Ausführung müssen nach [InstallInitialize](installinitialize-action.md) erfolgen und vor [InstallFinalize](installfinalize-action.md) in der Aktions Sequenz stehen.

Benutzerdefinierte Aktionen, mit denen Eigenschaften, Funktions Zustände, Komponenten Zustände oder Zielverzeichnisse festgelegt oder System Vorgänge durch Einfügen von Zeilen in Sequenz Tabellen geplant werden, können in vielen Fällen die sofortige Ausführung sicher verwenden. Benutzerdefinierte Aktionen, die das System direkt ändern oder einen anderen Systemdienst aufzurufen, müssen jedoch bis zu dem Zeitpunkt verzögert werden, zu dem das Installationsskript ausgeführt wird. Weitere Informationen zu möglichen Konflikten zwischen den benutzerdefinierten Aktionen und dem Hauptinstallations Thread finden Sie unter [synchrone und asynchrone benutzerdefinierte Aktionen](synchronous-and-asynchronous-custom-actions.md) .

Da das Installationsskript außerhalb der Installationssitzung ausgeführt werden kann, in der es geschrieben wurde, ist die Sitzung während der Ausführung des Installations Skripts möglicherweise nicht mehr vorhanden. Dies bedeutet, dass das ursprüngliche Sitzungs Handle und das Eigenschafts DataSet während der Installations Sequenz für eine benutzerdefinierte Aktion zur verzögerten Ausführung nicht verfügbar sind. Verzögerte benutzerdefinierte Aktionen, die Dynamic Link Libraries (DLLs) aufrufen, übergeben ein Handle, das nur zum Abrufen einer sehr begrenzten Menge von Informationen verwendet werden kann, wie unter Abrufen [von Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md)beschrieben.

Beachten Sie, dass verzögerte benutzerdefinierte Aktionen, einschließlich [Rollback von benutzerdefinierten Aktionen](rollback-custom-actions.md) und [Commit für benutzerdefinierte Aktionen](commit-custom-actions.md), die einzigen Aktions Typen sind, die außerhalb des Benutzer Sicherheits Kontexts ausgeführt werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md)
</dt> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> </dl>

 

 



