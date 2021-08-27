---
title: Aufzählen von Gruppen (RRAS)
description: In der folgenden Tabelle sind eine Reihe von Schritten in einer Interaktion zwischen einem Routingprotokoll und dem Multicastgruppen-Manager zusammengefasst.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df3731e8370a213636ea12ad2a9b072903908888eba6983909c01201c655ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101840"
---
# <a name="enumerating-groups"></a>Aufzählen von Gruppen

In der folgenden Tabelle sind eine Reihe von Schritten in einer Interaktion zwischen einem Routingprotokoll und dem Multicastgruppen-Manager zusammengefasst. Die erste Spalte beschreibt die Aktionen, die das Routingprotokoll ausführt, und die Antworten des Routingprotokolls an den Multicastgruppen-Manager. In der zweiten Spalte werden die Antworten des Multicastgruppen-Managers auf das Routingprotokoll beschrieben. Die dritte Spalte enthält alle zusätzlichen Informationen.

Jede Zeile der Tabelle stellt einen Schritt dar.



| Routingprotokollaktion                                                                                                                                                    | Multicast-Gruppen-Manager-Aktion                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rufen Sie mithilfe der [**MgmGroupEnumerationStart-Funktion**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) ein Handle für eine Enumeration ab.                                                         | Gibt ein Handle zurück.                                                                                                                                                                                                                                                                                             |
| Rufen Sie mithilfe der [**MgmGroupEnumerationGetNext-Funktion**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) eine oder mehrere Gruppen ab.                                                             | Gibt so viele Gruppen zurück, wie in den vom Client bereitgestellten Puffer passen. Wenn im angegebenen Puffer keine Gruppen zurückgegeben werden können, geben Sie ERROR \_ INSUFFICIENT BUFFER und die Größe des \_ Puffers zurück, der zum Zurückgeben einer Gruppe erforderlich ist.<br/> Gibt ERROR \_ NO \_ MORE ITEMS \_ zurück, wenn keine Weiteren Gruppen vorhanden sind.<br/> |
| Wenn ERROR \_ INSUFFICIENT \_ BUFFER empfangen wird, rufen Sie die [**MgmGroupEnumerationGetNext-Funktion**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) erneut auf, indem Sie einen Puffer der angegebenen Größe verwenden. |                                                                                                                                                                                                                                                                                                              |
| Fahren Sie mit dem Aufrufen der [**MgmGroupEnumerationGetNext-Funktion**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) fort, bis ERROR \_ NO MORE ITEMS empfangen \_ \_ wird.                                   |                                                                                                                                                                                                                                                                                                              |
| Beenden Sie den Enumerationsprozess mithilfe der [**MgmGroupEnumerationEnd-Funktion.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)                                                                   | Zerstören Sie das Handle.                                                                                                                                                                                                                                                                                          |



 

 

 





