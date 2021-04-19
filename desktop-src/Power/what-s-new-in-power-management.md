---
description: Windows 10 unterstützt Ihre Anwendung bei der Optimierung des Stromverbrauchs bei der Ausführung auf einem mobilen Gerät.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Neuerungen bei der Energie Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362464"
---
# <a name="whats-new-in-power-management"></a>Neues bei der Energieverwaltung

Windows 10 unterstützt Ihre Anwendung bei der Optimierung des Stromverbrauchs, wenn diese auf einem mobilen Gerät ausgeführt wird.

## <a name="battery-saver"></a>Stromsparmodus

In dieser Version kann die Anwendung benachrichtigt werden, wenn Akku Schoner aktiviert oder ausgeschaltet wird. Durch die Reaktion auf veränderliche Energiebedingungen kann die Anwendung zusammen mit Akku Schoner zusammenarbeiten, um Energie zu sparen und die Akku Lebensdauer zu erhöhen. Allgemeine Informationen zum Akku Schoner finden Sie unter [Batterie Schoner (in den Richtlinien für die Hardwarekomponente)](/windows-hardware/design/component-guidelines/battery-saver).

-   [**GUID \_ Energie \_ Spar \_ Status**](power-setting-guids.md) : Verwenden Sie diese neue GUID mit der Funktion " [**powersettingregisternotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) ", um benachrichtigt zu werden, wenn Akku Schoner aktiviert oder ausgeschaltet ist.

-   [**System \_ Energie \_ Status**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : Diese Struktur wurde aktualisiert, um den Akku Schoner zu unterstützen. Der vierte Member, **systemstatusflag** (früher **"reserved1"**), gibt nun an, ob der Akku Schoner eingeschaltet ist oder nicht. Verwenden Sie die [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) -Funktion, um einen Zeiger auf diese-Struktur abzurufen.

 

 
