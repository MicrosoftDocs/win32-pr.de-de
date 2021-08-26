---
description: Administratorüberschreibungen
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Administratorüberschreibungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af73f6d6fe3fe7d4edb8272c4d39c385a84973e4a3263c448505f5235adec855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033020"
---
# <a name="administrator-overrides"></a>Administratorüberschreibungen

Windows verfügt über eine einzelne Standardzugriffssteuerungsliste (Access Control List, ACL) für alle Energierichtlinienobjekte. Die Zugriffssteuerungsliste gewährt Mitgliedern der Gruppe Authentifizierte Benutzer Lese-, Schreib- und Änderungsberechtigungen. Allen anderen Benutzern wird eine schreibgeschützte Berechtigung erteilt. Anwendungen, die Energierichtlinienfunktionen aufrufen, können mithilfe der [**PowerSettingAccessCheck-Funktion**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) bestimmen, ob ein Benutzer über Berechtigungen für eine angegebene Energieeinstellung verfügt.

Energieeinstellungen können über Gruppenrichtlinie überschrieben werden. Außerkraftsetzungen können über Domänengruppenrichtlinien oder lokale Gruppenrichtlinien festgelegt werden. [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) meldet, ob eine angegebene Energieeinstellung über eine Außerkraftsetzung der Gruppenrichtlinie verfügt.

Das Befehlszeilentool **PowerCfg.exe** zeigt eine Fehlermeldung an, wenn ein Befehl nicht abgeschlossen werden kann, weil der Benutzer nicht über die Berechtigungen zum Ändern der Energieeinstellung verfügt oder weil die Energieeinstellung eine Gruppenrichtlinienüberschreibung aufweist.

Die Energieoptionen Anwendung in Systemsteuerung bietet keine Unterstützung für die Konfiguration von Energierichtlinienzugriffsberechtigungen. Das Ändern von Berechtigungen muss über **PowerCfg.exe** erfolgen.

 

 



