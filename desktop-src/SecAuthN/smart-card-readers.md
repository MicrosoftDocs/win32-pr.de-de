---
description: Leser sind Standardgeräte in einem Smartcardsystem. Sie werden über Treiber gesteuert und in das System über Plug & Play oder über die System Steuerungsgeräte-Elemente eingeführt und daraus entfernt.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Smartcardleser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350814"
---
# <a name="smart-card-readers"></a>Smartcardleser

Leser sind Standardgeräte in einem [*Smartcardsystem*](../secgloss/s-gly.md) . Sie werden über Treiber gesteuert und in das System über Plug & Play oder über die System Steuerungsgeräte-Elemente eingeführt und daraus entfernt.

Jeder Reader muss für die Verwendung durch das [*Smartcard-Subsystem*](../secgloss/s-gly.md)definiert werden. Das Subsystem ist nicht verantwortlich für Leser, die ihm nicht explizit übergeben werden.

Smartcardleser können in logische Gruppen unterteilt werden, die als Lesergruppen bezeichnet werden. Diese Gruppen können durch das-Subsystem definiert und von Administratoren und Benutzern definiert werden. Ein Reader kann mehreren Lesegruppen angehören.

Das Smartcard-Subsystem definiert die folgenden Gruppen.



| Gruppieren                | Beschreibung                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Card $ allreaders     | Diese Gruppe enthält alle Leser im System. Ein neuer Reader, der dem Smartcard-Subsystem zugewiesen ist, wird automatisch in die systemweite Reader-Gruppe, "SCard $ allreaders", eingeschlossen.                         |
| "SCard $ defaultreaders" | Diese Standardgruppe, eine für jedes [*Terminal*](../secgloss/t-gly.md), enthält alle dem Terminal zugewiesenen Leser, die nicht für eine bestimmte Verwendung reserviert sind. |



 

 

 
