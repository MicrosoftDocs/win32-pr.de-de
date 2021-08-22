---
description: Windows 10 unterstützt Ihre Anwendung bei der Optimierung des Energieverbrauchs bei der Ausführung auf einem mobilen Gerät.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Neuerungen in der Energieverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ac6ba320a98fce339f5bfacfe2d9b4a259be5a8150b2bcaabcac41179869e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143193"
---
# <a name="whats-new-in-power-management"></a>Neues bei der Energieverwaltung

Windows 10 hilft Ihrer Anwendung, den Stromverbrauch zu optimieren, wenn sie auf einem mobilen Gerät ausgeführt wird.

## <a name="battery-saver"></a>Stromsparmodus

In dieser Version kann Ihre Anwendung benachrichtigt werden, wenn Stromsparmodus aktiviert oder deaktiviert ist. Wenn Sie auf sich ändernde Energiebedingungen reagieren, kann Ihre Anwendung zusammen mit Stromsparmodus arbeiten, um Energie zu sparen und die Akkulebensdauer zu verlängern. Allgemeine Informationen zu Stromsparmodus finden Sie unter [Stromsparmodus (in den Richtlinien für Hardwarekomponenten).](/windows-hardware/design/component-guidelines/battery-saver)

-   [**GUID \_ \_ \_ ENERGIESPARSTATUS:**](power-setting-guids.md) Verwenden Sie diese neue GUID mit der [**PowerSettingRegisterNotification-Funktion,**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) um benachrichtigt zu werden, wenn Stromsparmodus ein- oder ausgeschaltet ist.

-   [**SYSTEM \_ POWER \_ STATUS:**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) Diese Struktur wurde aktualisiert, um Stromsparmodus zu unterstützen. Das vierte Element, **SystemStatusFlag** (zuvor **reserved1** genannt), gibt jetzt an, ob Stromsparmodus aktiv ist oder nicht. Verwenden Sie die [**GetSystemPowerStatus-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) um einen Zeiger auf diese Struktur abzurufen.

 

 
