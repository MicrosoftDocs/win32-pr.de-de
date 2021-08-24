---
description: Die IAutomaticUpdatesSettings-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: IAutomaticUpdatesSettings-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ae30a987dcf9d6573c179e7ef453c10c35a84b915b76a16439ba83a7174fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049468"
---
# <a name="iautomaticupdatessettings-methods"></a>IAutomaticUpdatesSettings-Methoden

Die [**IAutomaticUpdatesSettings-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) definiert die folgenden Methoden.



| Methode                                               | Beschreibung                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Aktualisieren**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Ruft die neuesten Automatische Updates ab. |
| [**Speichern**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Wendet die aktuellen Automatische Updates an.  |



 

> [!Note]  
> Auf Windows RT können Sie die [**IAutomaticUpdatesSettings::Save-Methode**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) nicht mehr verwenden, um die Einstellungen Windows Aktualisieren programmgesteuert zu konfigurieren. Der Konfigurationsvorgang schlägt fehl, wenn Sie **Speichern** verwenden, um einen anderen Wert als 4 [**(aunlScheduledInstallation) zu setzen.**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)

 

 

 



