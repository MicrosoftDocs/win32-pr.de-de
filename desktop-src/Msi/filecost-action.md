---
description: Die filecostaction initiiert dynamische costingof-Standard Installations Aktionen.
ms.assetid: 1b3f2baf-6191-452e-955d-8ac903edc1b7
title: Filecost-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9d87cb73353ef80f956ce13ec1940f1a4adee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050635"
---
# <a name="filecost-action"></a>Filecost-Aktion

Mit filecostaction werden die dynamischen [*Kosten*](c-gly.md)der Standard Installations Aktionen initiiert.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Alle standardmäßigen oder [benutzerdefinierten Aktionen](custom-actions.md) , die die Kosten beeinflussen, sollten vor der [costinitialize](costinitialize-action.md) -Aktion sequenziert werden. Wenden Sie die Aktion "filecost" direkt nach der Aktion "costinitialize" an. Anschließend können Sie die Aktion " [costfinalize](costfinalize-action.md) " nach der Aktion "costinitialize" aufzurufen, um dem Installer alle abschließenden Kostenberechnungen über die [Komponenten](component-table.md) Tabelle zur Verfügung zu stellen.

Die [costinitialize](costinitialize-action.md) -Aktion muss vor der filecost-Aktion ausgeführt werden. Das Installationsprogramm ermittelt dann die Speicherplatz Kosten jeder Datei in der [Datei](file-table.md) Tabelle pro Komponente (siehe [Komponenten Tabelle](component-table.md)) und übernimmt sowohl das volumeclustering als [](v-gly.md) auch das vorhanden sein vorhandener Dateien, die möglicherweise in das Konto überschrieben werden müssen. Alle Aktionen, die Speicherplatz belegen oder freigeben, werden ebenfalls berücksichtigt. Wenn eine vorhandene Datei gefunden wird, wird eine Überprüfung der Dateiversion durchgeführt, um zu bestimmen, ob die neue Datei tatsächlich installiert werden muss oder nicht. Wenn die vorhandene Datei dieselbe oder eine höhere Versionsnummer hat, wird die vorhandene Datei nicht überschrieben, und es fallen keine Kosten für den Speicherplatz an. In allen Fällen verwendet das Installationsprogramm die Ergebnisse der Versionsnummern Überprüfung, um den Installationsstatus der einzelnen Dateien festzulegen.

Die filecost-Aktion initialisiert die Kostenberechnung mit TheInstaller. Die tatsächliche dynamische [*Kosten*](c-gly.md) tritt erst auf, wenn die [costfinalize](costfinalize-action.md) -Aktion ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datei Kosten](file-costing.md)
</dt> </dl>

 

 



