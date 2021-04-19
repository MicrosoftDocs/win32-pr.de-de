---
description: Mit der Aktion "costinitialize" wird der Installationskosten Prozess initiiert.
ms.assetid: be9a8382-c892-44ae-8b59-c665b5cca2d2
title: Costinitialize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251bb0ae7508c87cd0af7ab81196c5d739e923a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350294"
---
# <a name="costinitialize-action"></a>Costinitialize-Aktion

Mit der Aktion "costinitialize" wird der Installations [*Kosten*](c-gly.md) Prozess initiiert.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Alle standardmäßigen oder [benutzerdefinierten](custom-actions.md) Aktionen, die sich auf die Kosten auswirken, sollten vor der costinitialize-Aktion sequenziert werden. Wenden Sie die Aktion " [filecost](filecost-action.md) " direkt nach der Aktion "costinitialize" an. Anschließend können Sie die Aktion " [costfinalize](costfinalize-action.md) " nach der Aktion "costinitialize Action" aufzurufen, um dem Installer mithilfe der [Komponenten](component-table.md) Tabelle alle abschließenden Kostenberechnungen zur Verfügung zu stellen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die costinitialize-Aktion lädt die [Komponenten Tabelle und](feature-table.md) die Featuretabelle in den Arbeitsspeicher.

Weitere Informationen zum [*Kosten*](c-gly.md) Prozess im Installationsprogramm finden Sie unter [Datei Kosten](file-costing.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datei Kosten](file-costing.md)
</dt> </dl>

 

 



