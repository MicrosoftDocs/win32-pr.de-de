---
description: Ein Dienst ist für das Melden von Zustandsänderungen an den Dienststeuerungs-Manager (Service Control Manager, SCM) verantwortlich.
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Dienststatusübergänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7039caf68ee7d9da93e86e1760e49df87667da8c16eb5ca6693cfdc7db7def2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967313"
---
# <a name="service-state-transitions"></a>Dienststatusübergänge

Ein Dienst ist für das Melden von Zustandsänderungen an den Dienststeuerungs-Manager (Service Control Manager, SCM) verantwortlich. Dienststeuerungsprogramme und das System können den Status eines Diensts nur über den SCM herausfinden. Daher ist es wichtig, dass ein Dienst seinen Zustand ordnungsgemäß berichtet. Ein Dienst meldet seinen Zustand, indem er die [**SetServiceStatus-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) mit einem Zeiger auf eine vollständig initialisierte [**SERVICE \_ STATUS-Struktur**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) aufruft. Das **dwCurrentState-Member** der -Struktur enthält den zu berichtenden Dienststatus.

Der anfängliche Zustand eines Diensts ist SERVICE \_ STOPPED. Wenn der SCM den Dienst startet, legt er den Dienststatus auf SERVICE START PENDING fest und ruft die \_ \_ [*ServiceMain-Funktion des Diensts*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) auf. Der Dienst schließt dann seine Initialisierung mithilfe einer der unter [Service ServiceMain-Funktion beschriebenen Verfahren ab.](service-servicemain-function.md) Nachdem der Dienst seine Initialisierung abgeschlossen hat und zum Empfangen von Steuerungsanforderungen bereit ist, ruft der Dienst [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) auf, um SERVICE RUNNING zu melden, und gibt die Steuerungsanforderungen an, die der Dienst akzeptieren \_ kann. Der Übergang von SERVICE START PENDING zu SERVICE RUNNING gibt an, dass der Dienst erfolgreich gestartet wurde. \_ \_ \_ Wenn der Dienst einen anderen Status als SERVICE RUNNING meldet, kann der SCM oder die Dienstüberwachungstools den Dienst als nicht \_ gestartet kennzeichnen.

Der SCM sendet nur die angegebenen Steuerungsanforderungen an den Dienst (mit Ausnahme der SERVICE \_ CONTROL \_ INTERROGATE-Anforderung, die immer gesendet wird). Eine Liste der Steuerungsanforderungen, die ein Dienst akzeptieren kann, finden Sie unter **dem dwControlsAccepted-Member** der [**SERVICE \_ STATUS-Struktur.**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Informationen zum Registrieren für den Empfang von Geräteereignissen finden Sie in der [**RegisterDeviceNotification-Funktion.**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)

Der Dienststatus ändert sich in der Regel durch die Verarbeitung einer Steuerungsanforderung. Zu den Steuerungsanforderungen, die zu einer Änderung des Dienstzustands führen, gehören SERVICE \_ CONTROL \_ STOP, SERVICE \_ CONTROL PAUSE und SERVICE CONTROL \_ \_ \_ CONTINUE. Wenn der Dienst eine lange Verarbeitung durchführen muss, um eine dieser Anforderungen zu verarbeiten, sollte er einen sekundären Thread erstellen, um die langwierige Verarbeitung durchzuführen und den entsprechenden ausstehenden Zustand an den SCM zu melden. (Für eine optimale Leistung Windows Vista und neueren Versionen von Windows sollte der [](/windows/desktop/ProcThread/thread-pools) Dienst zu diesem Zweck einen Arbeitsthread aus einem Threadpool verwenden.) Der Dienst sollte dann den Übergang des abgeschlossenen Zustands melden, wenn die langwierige Verarbeitung abgeschlossen ist. Weitere Informationen zum Behandeln von Steuerelementanforderungen finden Sie unter [Service Control Handler Function](service-control-handler-function.md).

Nur bestimmte Dienststatusübergänge sind gültig. Das folgende Diagramm zeigt die gültigen Übergänge.

![Gültige Dienststatusübergänge](images/service-status-transitions.png)

Der an den SCM gemeldete Dienststatus bestimmt, wie der SCM mit dem Dienst interagiert. Wenn ein Dienst beispielsweise SERVICE STOP PENDING meldet, überträgt der SCM keine weiteren Steuerungsanforderungen an den Dienst, da dieser Zustand angibt, dass der Dienst \_ \_ heruntergefahren wird. Der nächste vom Dienst gemeldete Zustand sollte SERVICE STOPPED lauten, da dies der einzige gültige Zustand \_ nach SERVICE STOP PENDING \_ \_ ist. Wenn ein Dienst jedoch einen ungültigen Übergang meldet, führt der SCM nicht zum Fehlschlagen des Aufrufs.

Das folgende Diagramm zeigt Dienststatusübergänge ausführlicher, einschließlich der Steuerungsanforderungen, die von einem Dienststeuerungsprogramm (dem Dienstclient) initiiert werden, und den [**SetServiceStatus-Aufrufen,**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) die ein Dienst zum Melden von Zustandsänderungen an den SCM vorträgt. Wie bereits erwähnt, sendet der SCM nur Steuerungsanforderungen, die der Dienst akzeptiert, sodass ein Dienst möglicherweise nicht alle im Diagramm gezeigten Anforderungen erhält.

![Dienststatusübergänge im Detail ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
