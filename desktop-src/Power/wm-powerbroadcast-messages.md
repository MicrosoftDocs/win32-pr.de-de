---
description: Das System überträgt immer dann eine Nachricht an alle Anwendungen und installierbaren Treiber, wenn ein Energie Verwaltungs Ereignis auftritt.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: WM_POWERBROADCAST Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348010"
---
# <a name="wm_powerbroadcast-messages"></a>WM- \_ powerbroadcast-Meldungen

Das System überträgt immer dann eine Nachricht an alle Anwendungen und installierbaren Treiber, wenn ein Energie Verwaltungs Ereignis auftritt. Das System überträgt diese Ereignisse über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht, wobei der *wParam* -Parameter auf das entsprechende Energie Verwaltungs Ereignis festgelegt wird. Beispielsweise zeigt das [PBT \_ apmpowerstatuschange](pbt-apmpowerstatuschange.md) -Ereignis eine Änderung des System Energiestatus an. Sie müssen sicherstellen, dass Ihre Anwendung ordnungsgemäß auf die **WM- \_ powerbroadcast** -Nachricht antwortet.

Das System überträgt ein [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis unmittelbar vor dem Anhalten des Vorgangs. Dadurch haben Anwendungen und Treiber eine letzte Chance, das Ereignis vorzubereiten. In vielen Fällen überträgt das System diese Nachrichten, ohne dafür die entsprechende Berechtigung anzufordern. Dies ist z. b. der Fall, wenn eine Anwendung die Unterbrechung mit der [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) -Funktion erzwingt.

Das System überträgt das [PBT \_ apmresumesuspend](pbt-apmresumesuspend.md) -oder [PBT \_ apmresumecritical](pbt-apmresumecritical.md) -Ereignis, wenn der System Vorgang wieder hergestellt wurde. Wenn eine Anwendung ein [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis empfangen hat, bevor der Computer angehalten wurde, wird das PBT \_ apmresumesuspend-Ereignis empfangen. Andernfalls wird das PBT \_ apmresumecritical-Ereignis empfangen.

Das System sendet ein [PBT- \_ powersettingchange](pbt-powersettingchange.md) -Ereignis an Anwendungen, die mithilfe von [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification)für das jeweilige Ereignis registriert wurden. Weitere Informationen finden Sie unter [registrieren für Power Events](registering-for-power-events.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> </dl>

 

 



