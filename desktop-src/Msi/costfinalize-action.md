---
description: Die Aktion "costfinalize" beendet den Prozess der internen Installationskosten, der von der Aktion "costinitialize" gestartet wurde.
ms.assetid: ae69ad03-5acc-4a62-ba71-3a4e477d34ab
title: Costfinalize-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5423f1050f9c9d755d33e492b9b65cfcaa08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369018"
---
# <a name="costfinalize-action"></a>Costfinalize-Aktion

Die Aktion "costfinalize" beendet den Prozess der internen Installations [*Kosten*](c-gly.md) , der von der Aktion " [costinitialize](costinitialize-action.md) " gestartet wurde.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Alle standardmäßigen oder [benutzerdefinierten Aktionen](custom-actions.md) , die sich auf die Kosten auswirken, sollten vor der [costinitialize](costinitialize-action.md) -Aktion sequenziert werden. Nennen Sie die Aktion " [filecost](filecost-action.md) " unmittelbar nach der Aktion "costinitialize", und wenden Sie dann die Aktion "costfinalize" an, um dem Installer alle abschließenden Kostenberechnungen über die [Komponenten](component-table.md) Tabelle zur Verfügung zu stellen

Die costfinalize-Aktion muss ausgeführt werden, bevor eine Benutzeroberflächen Sequenz gestartet wird, die es dem Benutzer [](feature-table.md) ermöglicht, featuretabellenauswahl oder-Verzeichnisse anzuzeigen oder zu ändern.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Mit der costfinalize-Aktion wird die [Bedingungs Tabelle](condition-table.md) abgefragt, um zu bestimmen, welche Features installiert werden sollen. Die Kosten werden für jede Komponente in der [Komponenten](component-table.md) Tabelle durchgeführt.

Mit der Aktion "costfinalize" wird außerdem überprüft, ob alle Zielverzeichnisse beschreibbar sind, bevor die Installation fortgesetzt werden kann.

> [!Note]  
> Bei einer [administrativen Installation](administrative-installation.md)werden von "costfinalize" alle Features für die Installation festgelegt, außer bei den Funktionen, die in der Spalte Ebene der [Featuretabelle](feature-table.md)erstellt wurden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datei Kosten](file-costing.md)
</dt> </dl>

 

 



