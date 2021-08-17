---
description: Leser sind Standardgeräte in einem Smartcardsystem. Sie werden über Treiber gesteuert und mit dem System über Plug & Play oder über das Systemsteuerung Devices-Element aus dem System eingeführt und daraus entfernt.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Smartcardleser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335aabe1d815e9b6d41ccfd820242209da63134797595d8a1c85f009f8551b7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917749"
---
# <a name="smart-card-readers"></a>Smartcardleser

Leser sind Standardgeräte in einem [*Smartcardsystem.*](../secgloss/s-gly.md) Sie werden über Treiber gesteuert und mit dem System über Plug & Play oder über das Systemsteuerung Devices-Element aus dem System eingeführt und daraus entfernt.

Jeder Reader muss für die Verwendung durch das [*Smartcardsubsystem definiert werden.*](../secgloss/s-gly.md) Das Subsystem ist nicht für Leser verantwortlich, die ihm nicht speziell erteilt wurden.

Smartcardleser können in logische Gruppen unterteilt werden, die als Lesergruppen bezeichnet werden. Diese Gruppen können vom Subsystem sowie von Administratoren und Benutzern definiert werden. Ein Leser kann zu mehr als einer Lesergruppe gehören.

Das Smartcardsubsystem definiert die folgenden Gruppen.



| Gruppieren                | Beschreibung                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCard$AllReaders     | Diese Gruppe enthält alle Leser im System. Ein neuer Reader, der dem Smartcardsubsystem gegeben wird, wird automatisch in die systemweite Lesergruppe SCard$AllReaders aufgenommen.                         |
| SCard$DefaultReaders | Diese Standardgruppe, eine für [*jedes*](../secgloss/t-gly.md)Terminal, enthält alle Leser, die dem Terminal zugewiesen sind und nicht für eine bestimmte Verwendung reserviert sind. |



 

 

 
