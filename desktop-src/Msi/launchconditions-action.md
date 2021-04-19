---
description: Mit der LaunchConditions-Aktion wird die LaunchCondition-Tabelle abgefragt und jede aufgezeichnete bedingte Anweisung ausgewertet. Wenn eine dieser Bedingungs Anweisungen fehlschlägt, wird dem Benutzer eine Fehlermeldung angezeigt, und die Installation wird beendet.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: LaunchConditions-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350449"
---
# <a name="launchconditions-action"></a>LaunchConditions-Aktion

Mit der LaunchConditions-Aktion wird die [LaunchCondition-Tabelle](launchcondition-table.md) abgefragt und jede aufgezeichnete bedingte Anweisung ausgewertet. Wenn eine dieser Bedingungs Anweisungen fehlschlägt, wird dem Benutzer eine Fehlermeldung angezeigt, und die Installation wird beendet.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion "LaunchConditions" ist optional. Diese Aktion ist normalerweise die erste in der Sequenz, aber die [AppSearch-Aktion](appsearch-action.md) kann vor der Aktion "LaunchConditions" sequenziert werden. Wenn Startbedingungen nicht auf alle Installations Modi zutreffen, sollte die entsprechende Eigenschaft für den Installationsmodus in einem bedingten Ausdruck in der entsprechenden Sequenz Tabelle verwendet werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

 

 



