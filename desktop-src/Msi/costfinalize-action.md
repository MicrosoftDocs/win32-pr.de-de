---
description: Die CostFinalize-Aktion beendet den internen Installationskostenprozess, der von der CostInitialize-Aktion gestartet wurde.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: CostFinalize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6b8fb49218925d3f517a9d198a638bc9dff5a1184beef24a487de0112830f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638354"
---
# <a name="costfinalize-action"></a>CostFinalize-Aktion

Die CostFinalize-Aktion beendet den internen [*Installationskostenprozess,*](c-gly.md) der von der [CostInitialize-Aktion](costinitialize-action.md) gestartet wurde.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Alle standard- oder [benutzerdefinierten Aktionen,](custom-actions.md) die sich auf die Kosten auswirken, sollten vor der [CostInitialize-Aktion](costinitialize-action.md) sequenziert werden. Rufen Sie die [FileCost-Aktion](filecost-action.md) unmittelbar nach der CostInitialize-Aktion auf, und rufen Sie dann die CostFinalize-Aktion auf, um alle endgültigen Kostenberechnungen für das Installationsprogramm über die [Tabelle Komponente](component-table.md) verfügbar zu machen.

Die CostFinalize-Aktion muss ausgeführt werden, bevor eine Benutzeroberflächensequenz gestartet wird, die es dem Benutzer ermöglicht, Funktionstabellenauswahlen oder [-verzeichnisse](feature-table.md) anzuzeigen oder zu ändern.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Die CostFinalize-Aktion fragt die [Tabelle Bedingung](condition-table.md) ab, um zu bestimmen, welche Features installiert werden sollen. Die Kosten werden für jede Komponente in der [Tabelle Komponente](component-table.md) durchgeführt.

Die Aktion CostFinalize überprüft außerdem, ob alle Zielverzeichnisse schreibbar sind, bevor die Installation fortgesetzt werden kann.

> [!Note]  
> Während einer [Administratorinstallation](administrative-installation.md)legt CostFinalize alle Features für die Installation fest, mit Ausnahme von Features, für die 0 in der Spalte Ebene der [Featuretabelle](feature-table.md)erstellt wurde.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateikosten](file-costing.md)
</dt> </dl>

 

 



