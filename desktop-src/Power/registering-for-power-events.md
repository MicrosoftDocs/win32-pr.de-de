---
description: Anwendungen können Ihr Verhalten besser an den aktuellen Energiezustand des Computers anpassen, indem Sie sich für Strom Ereignisse registrieren.
ms.assetid: 840390ca-d32a-4cf3-9e75-66322c7cdee0
title: Registrieren für Strom Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da084592414d1c58ab4ab43dd2b5c35f028552b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216023"
---
# <a name="registering-for-power-events"></a>Registrieren für Strom Ereignisse

Anwendungen können Ihr Verhalten besser an den aktuellen Energiezustand des Computers anpassen, indem Sie sich für Strom Ereignisse registrieren. Eine Anwendung sollte für jedes Strom Änderungs Ereignis registriert werden, das sich auf das Verhalten auswirken könnte.

Eine Anwendung oder ein Dienst verwendet die [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) -Funktion, um Benachrichtigungen für Benachrichtigungen zu registrieren. Wenn die entsprechende Energie Einstellung geändert wird, sendet das System wie folgt Benachrichtigungen:

-   Eine Anwendung empfängt eine [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht mit einem *wParam* -Wert von [PBT \_ powersettingchange](pbt-powersettingchange.md) und einem *LPARAM* , der auf eine [**powerbroadcast- \_ Einstellungs**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) Struktur verweist.
-   Ein Dienst empfängt einen Aufruf der [*handlerex*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) -Rückruffunktion, die er durch Aufrufen der [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) -Funktion registriert hat. Der an die *handlerex* -Rückruffunktion gesendete *lpeer ventdata* -Parameter verweist auf eine [**powerbroadcast- \_ Einstellungs**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) Struktur.

In der Struktur der [**powerbroadcast- \_ Einstellungen**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) enthält das **Powersetting** -Element die GUID, die die Benachrichtigung identifiziert, und das **Datenmember** enthält den neuen Wert der Energie Einstellung.

Eine Liste der Powersetting-GUIDs für Benachrichtigungen, die für-Anwendungen am nützlichsten sind, finden Sie unter [**Power Setting-GUIDs**](power-setting-guids.md).

 

 
