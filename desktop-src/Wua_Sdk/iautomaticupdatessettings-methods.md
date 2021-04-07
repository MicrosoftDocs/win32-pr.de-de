---
description: Die iautomaticupdatessettings-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Iautomaticupdatessettings-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863747"
---
# <a name="iautomaticupdatessettings-methods"></a>Iautomaticupdatessettings-Methoden

Die [**iautomaticupdatessettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) -Schnittstelle definiert die folgenden Methoden.



| Methode                                               | BESCHREIBUNG                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Aktualisieren**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Ruft die neuesten automatische Updates Einstellungen ab. |
| [**Speichern**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Wendet die aktuellen automatische Updates Einstellungen an.  |



 

> [!Note]  
> Unter Windows RT können Sie die [**iautomaticupdatessettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) -Methode nicht mehr verwenden, um Windows Update Einstellungen Programm gesteuert zu konfigurieren. Der Konfigurations Vorgang schlägt fehl, wenn Sie " **Speichern** " verwenden, um einen anderen Wert als 4 ("[**aunlscheduledinstallations**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)") festzulegen.

 

 

 



