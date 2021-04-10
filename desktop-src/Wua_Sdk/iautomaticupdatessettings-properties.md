---
description: Die iautomaticupdatessettings-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Iautomaticupdatessettings-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958992"
---
# <a name="iautomaticupdatessettings-properties"></a>Iautomaticupdatessettings-Eigenschaften

Die [**iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                 | BESCHREIBUNG                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Ruft ab und legt fest, wie Benutzer über automatische Aktualisierungs Ereignisse benachrichtigt werden.                              |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Ruft einen booleschen Wert ab, der angibt, ob die Einstellungen für automatisches Update schreibgeschützt sind.         |
| [**Erforderlich**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Ruft einen booleschen Wert ab, der angibt, ob für Gruppenrichtlinie der automatische Updates-Dienst erforderlich ist. |
| [**Scheduledinstallationday**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Ruft die Wochentage ab, an denen automatische Updates Updates installiert oder deinstalliert, oder legt Sie fest.    |
| [**Scheduledinstallationtime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Ruft den Zeitpunkt ab, zu dem automatische Updates Updates installiert oder deinstalliert, oder legt ihn fest.                |



 

> [!Note]  
> Windows 8, Windows 8.1, Windows Server 2012 und Windows Server 2012 R2 bieten nur eingeschränkte Unterstützung für [**scheduledinstallationday**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) und [**scheduledinstallationtime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Wenn der Computer über Gruppenrichtlinie konfiguriert wurde, um einen Tag und eine Uhrzeit für die geplante Installation zu verwenden, geben die Eigenschaften **scheduledinstallationday** und **scheduledinstallationtime** diesen geplanten Tag und diese Uhrzeit zurück. Wenn der Computer auf diese Weise nicht über Gruppenrichtlinie konfiguriert wurde, geben die Eigenschaften **scheduledinstallationday** und **scheduledinstallationtime** standardmäßige und unzuverlässige Werte zurück. Wenn Sie versuchen, den Tag und die Uhrzeit für die geplante Installation unter diesen Betriebssystemen zu ändern, sind **scheduledinstallationday** und **scheduledinstallationtime** anscheinend erfolgreich, haben jedoch keine Auswirkungen.

 

 

 



