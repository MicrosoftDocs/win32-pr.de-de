---
title: Auflisten von Gruppen (RRAS)
description: In der folgenden Tabelle werden eine Reihe von Schritten in einer Interaktion zwischen einem Routing Protokoll und dem Multicast-Gruppen-Manager zusammengefasst.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3860c6876ed6ea5caef4941efcdd949eb9890d
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104472037"
---
# <a name="enumerating-groups"></a>Auflisten von Gruppen

In der folgenden Tabelle werden eine Reihe von Schritten in einer Interaktion zwischen einem Routing Protokoll und dem Multicast-Gruppen-Manager zusammengefasst. In der ersten Spalte werden die Aktionen beschrieben, die das Routing Protokoll ausführt, und die Antwort des Routing Protokolls an den Multicast-Gruppen-Manager. In der zweiten Spalte werden die Antworten des Multicast-Gruppen-Managers auf das Routing Protokoll beschrieben. Die dritte Spalte enthält alle zusätzlichen Informationen.

Jede Zeile der Tabelle stellt einen Schritt dar.



| Routing Protokoll Aktion                                                                                                                                                    | Multicast-Gruppen-Manager-Aktion                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abrufen eines Handles für eine Enumeration mithilfe der [**mgmgroupumerationstart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) -Funktion.                                                         | Gibt ein Handle zurück.                                                                                                                                                                                                                                                                                             |
| Abrufen einer oder mehrerer Gruppen mithilfe der [**mgmgroupumschlag**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) -Funktion                                                             | Gibt beliebig viele Gruppen zurück, die in den vom Client bereitgestellten Puffer passen. Wenn im bereitgestellten Puffer keine Gruppen zurückgegeben werden können, geben \_ Sie nicht ausreichenden \_ Puffer und die Größe des Puffers zurück, der zum Zurückgeben einer Gruppe benötigt wird.<br/> Gibt einen Fehler zurück, \_ \_ \_ Wenn keine weiteren Gruppen vorhanden sind.<br/> |
| Wenn \_ \_ der Puffer nicht ausreichend ist, können Sie die Funktion [**mgmgroupenerationgetnext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) erneut aufrufen, indem Sie einen Puffer der angegeben Größe verwenden. |                                                                                                                                                                                                                                                                                                              |
| Fahren Sie mit dem Aufruf der [**mgmgroupenerationgetnext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) -Funktion fort, bis der Fehler \_ nicht \_ mehr \_ angezeigt wird.                                   |                                                                                                                                                                                                                                                                                                              |
| Beenden Sie den [**enumerationsprozess mithilfe der mgmgroupumerationend**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) -Funktion.                                                                   | Zerstören Sie das handle.                                                                                                                                                                                                                                                                                          |



 

 

 





