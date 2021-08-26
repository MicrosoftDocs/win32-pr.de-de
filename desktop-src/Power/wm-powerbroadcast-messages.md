---
description: Das System sendet eine Nachricht an alle Anwendungen und installierbaren Treiber, wenn ein Energieverwaltungsereignis auftritt.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7997f6c9bed6b4d46068c9974f4ff3571a9617ba2bf09adc6b98bb33facb3d1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032690"
---
# <a name="wm_powerbroadcast-messages"></a>WM \_ POWERBROADCAST-Nachrichten

Das System sendet eine Nachricht an alle Anwendungen und installierbaren Treiber, wenn ein Energieverwaltungsereignis auftritt. Das System überträgt diese Ereignisse über die [**WM \_ POWERBROADCAST-Nachricht**](wm-powerbroadcast.md) und setzt den *wParam-Parameter* auf das entsprechende Energieverwaltungsereignis. Das [PBT-Ereignis \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) weist beispielsweise auf eine Änderung des Systemleistungsstatus hin. Sie müssen sicherstellen, dass Ihre Anwendung ordnungsgemäß auf die **WM \_ POWERBROADCAST-Nachricht** reagiert.

Das System überträgt ein [ \_ PBT-APMSUSPEND-Ereignis](pbt-apmsuspend.md) unmittelbar vor dem Aussetzen des Vorgangs. Dadurch erhalten Anwendungen und Treiber eine letzte Möglichkeit, sich auf das Ereignis vorzubereiten. In vielen Fällen überträgt das System diese Nachrichten, ohne dies zu tun. Dies geschieht beispielsweise, wenn eine Anwendung eine Unterbrechung mit der [**SetSuspendState-Funktion erzwingt.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

Das System überträgt das [ \_ PBT-Ereignis APMRESUMESUSPEND](pbt-apmresumesuspend.md) oder [PBT \_ APMRESUMECRITICAL,](pbt-apmresumecritical.md) wenn der Systemvorgang wiederhergestellt wurde. Wenn eine Anwendung ein [ \_ PBT-APMSUSPEND-Ereignis](pbt-apmsuspend.md) empfangen hat, bevor der Computer angehalten wurde, erhält sie das \_ PBT-Ereignis APMRESUMESUSPEND. Andernfalls wird das \_ PBT-Ereignis APMRESUMECRITICAL empfangen.

Das System sendet mit [**registerPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification)ein [PBT \_ POWERSETTINGCHANGE-Ereignis](pbt-powersettingchange.md) an Anwendungen, die sich für das spezifische Ereignis registriert haben. Weitere Informationen finden Sie unter [Registrieren für Power Events.](registering-for-power-events.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energieverwaltung](about-power-management.md)
</dt> </dl>

 

 



