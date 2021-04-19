---
description: Administrator Überschreibungen
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Administrator Überschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363468"
---
# <a name="administrator-overrides"></a>Administrator Überschreibungen

Windows verfügt über eine einzige Standard-Zugriffs Steuerungs Liste (ACL) für alle Energierichtlinien Objekte. Die ACL gewährt Mitgliedern der Gruppe "authentifizierte Benutzer" Lese-, Schreib-und Änderungs Berechtigungen. Allen anderen Benutzern wird die Berechtigung schreibgeschützt erteilt. Anwendungen, die Energierichtlinien Funktionen aufzurufen, können bestimmen, ob ein Benutzer über Berechtigungen für eine angegebene Energie Einstellung verfügt, indem er die Funktion " [**powersettingaccesscheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) " verwendet.

Energie Einstellungen können über Gruppenrichtlinie überschrieben werden. Außer Kraft setzungen können über eine Domänen Gruppenrichtlinie oder eine lokale Gruppenrichtlinie festgelegt werden. [**Powersettingaccesscheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) meldet, ob eine angegebene Energie Einstellung eine Gruppenrichtlinien-außer Kraft Setzung aufweist.

Das Befehlszeilen Tool **PowerCfg.exe** zeigt eine Fehlermeldung an, wenn ein Befehl nicht abgeschlossen werden kann, da der Benutzer nicht über Berechtigungen zum Ändern der Energie Einstellung verfügt oder weil die Energie Einstellung eine Gruppenrichtlinien-außer Kraft Setzung aufweist.

Die Anwendung Energieoptionen in der Systemsteuerung bietet keine Unterstützung für das Konfigurieren von Berechtigungen für den Energierichtlinien Zugriff. Das Ändern von Berechtigungen muss über **PowerCfg.exe** erfolgen.

 

 



