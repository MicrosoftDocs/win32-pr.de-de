---
description: Ein Dienst ist dafür verantwortlich, seine Statusänderungen an den Dienststeuerungs-Manager (Service Control Manager, SCM) zu melden.
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Dienststatus Übergänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df7684b1ebc04aa1116b09a3ae4321f2552d7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568619"
---
# <a name="service-state-transitions"></a>Dienststatus Übergänge

Ein Dienst ist dafür verantwortlich, seine Statusänderungen an den Dienststeuerungs-Manager (Service Control Manager, SCM) zu melden. Dienst Steuerungsprogramme und das System können den Zustand eines Dienstanbieter nur über den SCM ermitteln, daher ist es wichtig, dass ein Dienst seinen Zustand korrekt meldet. Ein Dienst meldet seinen Zustand, indem er die Funktion [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) mit einem Zeiger auf eine vollständig initialisierte [**Dienst \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Struktur aufruft. Der **dwcurrentstate** -Member der-Struktur enthält den Dienststatus, der gemeldet werden soll.

Der anfängliche Zustand eines Dienstanbieter ist "Dienst \_ beendet". Wenn der SCM den Dienst startet, legt er den Dienststatus auf " \_ ausstehende Dienst Start" fest \_ und ruft die [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion des dienstaners auf. Der Dienst schließt dann seine Initialisierung mit einer der in [Service Main-Funktion](service-servicemain-function.md)beschriebenen Verfahren ab. Nachdem der Dienst seine Initialisierung abgeschlossen hat und bereit ist, mit dem Empfang von Steuerungsanforderungen zu beginnen, ruft der Dienst [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) für den Berichts Dienst auf, der ausgeführt wird, \_ und gibt die Steuerungsanforderungen an, die der Dienst akzeptiert. Der Übergang vom Dienst \_ Start \_ Pending to Service \_ Running zeigt den SCM-und Dienst Überwachungstools an, dass der Dienst erfolgreich gestartet wurde. Wenn der Dienst einen anderen Zustand als den Dienst meldet \_ , der ausgeführt wird, können die SCM-oder Dienst Überwachungstools den Dienst als fehlerhaft markieren.

Der SCM sendet nur die angegebenen Steuerungsanforderungen an den Dienst (mit Ausnahme der \_ Anforderung der Dienststeuerungs- \_ Abfrage, die immer gesendet wird). Eine Liste der Steuerungsanforderungen, die ein Dienst annehmen kann, finden Sie unter dem **dwcontrolsaccepted** -Member der [**Service \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) -Struktur. Informationen zum Registrieren von für den Empfang von Geräte Ereignissen finden Sie in der [**registerdevicenotifi-**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) Funktion.

Der Dienststatus ändert sich in der Regel aufgrund der Verarbeitung einer Steuerungs Anforderung. Steuerungsanforderungen, die bewirken, dass der Dienststatus geändert \_ wird, umfassen das Anhalten der Dienst Kontrolle \_ , das Anhalten der Dienst \_ Kontrolle und die \_ Dienst \_ Steuerung \_ . Wenn der Dienst lange Verarbeitung ausführen muss, um eine dieser Anforderungen zu verarbeiten, sollte ein sekundärer Thread erstellt werden, um die lange Verarbeitung auszuführen und den entsprechenden ausstehenden Status an den SCM zu melden. (Um eine optimale Leistung bei Windows Vista und höheren Versionen von Windows zu erzielen, sollte der Dienst für diesen Zweck einen Arbeits Thread aus einem [Thread Pool](/windows/desktop/ProcThread/thread-pools) verwenden.) Der Dienst sollte dann den abgeschlossenen Zustandsübergang melden, wenn die lange Verarbeitung abgeschlossen ist. Weitere Informationen zum Verarbeiten von Steuerungsanforderungen finden Sie unter [Dienststeuerungs-Handlerfunktion](service-control-handler-function.md).

Nur bestimmte Dienst Zustandsübergänge sind gültig. Das folgende Diagramm zeigt die gültigen Übergänge.

![gültige Dienststatus Übergänge](images/service-status-transitions.png)

Der Dienststatus, der dem SCM gemeldet wird, bestimmt, wie der SCM mit dem Dienst interagiert. Wenn beispielsweise ein Dienst Berichte \_ \_ nicht mehr ausstehend ist, überträgt der SCM keine weiteren Steuerungsanforderungen an den Dienst, da dieser Zustand angibt, dass der Dienst heruntergefahren wird. Der nächste vom Dienst gemeldete Status sollte vom Dienst \_ beendet werden, da dies der einzige gültige Status ist, nachdem der Dienst \_ beendet wurde \_ . Wenn ein Dienst jedoch einen Übergang meldet, der nicht gültig ist, kann der SCM den-Befehl nicht ausführen.

Im folgenden Diagramm werden Dienst Zustandsübergänge ausführlicher dargestellt, einschließlich der Steuerungsanforderungen, die von einem Dienst Steuerungsprogramm (dem Dienst Client) initiiert werden, und den [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) -aufrufen, die ein Dienst zum Melden von Zustandsänderungen an den SCM vornimmt. Wie bereits erwähnt, sendet der SCM nur Steuerungsanforderungen, die der Dienst angegeben hat, damit ein Dienst möglicherweise nicht alle im Diagramm angezeigten Anforderungen empfängt.

![Dienststatus Übergänge im Detail ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**Controlserviceex**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
