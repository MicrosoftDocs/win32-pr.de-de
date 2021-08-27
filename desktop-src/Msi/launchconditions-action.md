---
description: Die LaunchConditions-Aktion fragt die LaunchCondition-Tabelle ab und wertet jede dort aufgezeichnete bedingte Anweisung aus. Wenn eine dieser bedingungsbedingten Anweisungen fehlschlägt, wird dem Benutzer eine Fehlermeldung angezeigt, und die Installation wird beendet.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: LaunchConditions-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a973e6e1de81091039de12e07e8edb890c860e5be54e942f00406e39e62e229
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086030"
---
# <a name="launchconditions-action"></a>LaunchConditions-Aktion

Die LaunchConditions-Aktion fragt die [LaunchCondition-Tabelle](launchcondition-table.md) ab und wertet jede dort aufgezeichnete bedingte Anweisung aus. Wenn eine dieser bedingungsbedingten Anweisungen fehlschlägt, wird dem Benutzer eine Fehlermeldung angezeigt, und die Installation wird beendet.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die LaunchConditions-Aktion ist optional. Diese Aktion ist normalerweise die erste in der Sequenz, aber die [AppSearch-Aktion](appsearch-action.md) kann vor der LaunchConditions-Aktion sequenziert werden. Wenn Startbedingungen nicht für alle Installationsmodi gelten, sollte die entsprechende Installationsmoduseigenschaft in einem bedingten Ausdruck in der entsprechenden Sequenztabelle verwendet werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

 

 



