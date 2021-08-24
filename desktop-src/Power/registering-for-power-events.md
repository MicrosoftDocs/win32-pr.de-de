---
description: Anwendungen können ihr Verhalten besser an den aktuellen Energiezustand des Computers anpassen, indem sie sich für Energieereignisse registrieren.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registrieren für Power Events
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c360905800ad3fdce047e16a0244cd3dbf1ca312f18154f0be0c36b75e546d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143323"
---
# <a name="registering-for-power-events"></a>Registrieren für Power Events

Anwendungen können ihr Verhalten besser an den aktuellen Energiezustand des Computers anpassen, indem sie sich für Energieereignisse registrieren. Eine Anwendung sollte sich für jedes Energieänderungsereignis registrieren, das sich auf ihr Verhalten auswirken kann.

Eine Anwendung oder ein Dienst verwendet die [**RegisterPowerSettingNotification-Funktion,**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) um sich für Benachrichtigungen zu registrieren. Wenn sich die entsprechende Energieeinstellung ändert, sendet das System Benachrichtigungen wie folgt:

-   Eine Anwendung empfängt eine [**\_ WM-POWERBROADCAST-Nachricht**](wm-powerbroadcast.md) mit einem *wParam* von [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) und einem *lParam,* der auf eine [**POWERBROADCAST \_ SETTING-Struktur**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) verweist.
-   Ein Dienst empfängt einen Aufruf der [*HandlerEx-Rückruffunktion,*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) die er registriert hat, indem er die [**RegisterServiceCtrlHandlerEx-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) aufruft. Der an die *HandlerEx-Rückruffunktion* gesendete *lpEventData-Parameter* verweist auf eine [**POWERBROADCAST \_ SETTING-Struktur.**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)

In der [**POWERBROADCAST \_ SETTING-Struktur**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) enthält das **PowerSetting-Element** die GUID, die die Benachrichtigung identifiziert, und das **Data-Element** enthält den neuen Wert der Energieeinstellung.

Eine Liste der Energieeinstellungs-GUIDs für Benachrichtigungen, die für Anwendungen am nützlichsten sind, finden Sie unter [**Power Setting GUIDs**](power-setting-guids.md).

 

 
