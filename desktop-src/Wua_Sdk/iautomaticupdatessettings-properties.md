---
description: Die IAutomaticUpdatesSettings-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: IAutomaticUpdatesSettings-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6995264aebed44e8cb21e3880268a1488157ed5085645e5232feaa94a8786eed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897150"
---
# <a name="iautomaticupdatessettings-properties"></a>IAutomaticUpdatesSettings-Eigenschaften

Die [**IAutomaticUpdatesSettings-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                 | BESCHREIBUNG                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Ruft ab und legt fest, wie Benutzer über Automatische Updateereignisse benachrichtigt werden.                              |
| [**Readonly**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Ruft einen booleschen Wert ab, der angibt, ob die Einstellungen für automatische Updates schreibgeschützt sind.         |
| [**Erforderlich**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Ruft einen booleschen Wert ab, der angibt, ob Gruppenrichtlinie den Automatische Updates erfordert. |
| [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Ruft die Wochentage ab, an denen updates von Automatische Updates installiert oder deinstalliert werden, und legt diese fest.    |
| [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Ruft den Zeitpunkt ab, zu dem Automatische Updates Updates installiert oder deinstalliert, und legt diese fest.                |



 

> [!Note]  
> Windows 8, Windows 8.1, Windows Server 2012 und Windows Server 2012 R2 bieten nur eingeschränkte Unterstützung für [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) und [**ScheduledInstallationTime.**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) Wenn der Computer über Gruppenrichtlinie für die Verwendung eines geplanten Installationstags und einer geplanten Installationszeit konfiguriert wurde, geben die **Eigenschaften ScheduledInstallationDay** und **ScheduledInstallationTime** diesen geplanten Tag und diese Uhrzeit zurück. Wenn der Computer nicht auf diese Weise über Gruppenrichtlinie konfiguriert wurde, geben die **Eigenschaften ScheduledInstallationDay** und **ScheduledInstallationTime** Standardwerte und unzuverlässige Werte zurück. Wenn Sie versuchen, den Tag und die Uhrzeit der geplanten Installation auf diesen Betriebssystemen zu ändern, scheinen **ScheduledInstallationDay** und **ScheduledInstallationTime** erfolgreich zu sein, haben jedoch keine Auswirkungen.

 

 

 



