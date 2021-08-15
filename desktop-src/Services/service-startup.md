---
description: Zum Starten eines Dienst- oder Treiberdiensts verwendet das Dienststeuerungsprogramm die StartService-Funktion.
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: Dienststart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17901987581b6a2680e0a70cfe2e0ed80472d293cbe32932f768e9133b6a058d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888699"
---
# <a name="service-startup"></a>Dienststart

Zum Starten eines Dienst- oder Treiberdiensts verwendet das Dienststeuerungsprogramm die [**StartService-Funktion.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) Die **StartService-Funktion** schlägt fehl, wenn die Datenbank gesperrt ist. In diesem Fall sollte das Dienststeuerungsprogramm einige Sekunden warten und **StartService erneut** aufrufen. Sie kann den aktuellen Sperrstatus der Datenbank überprüfen, indem die [**QueryServiceLockStatus-Funktion aufruft.**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)

Wenn das Dienststeuerungsprogramm einen Dienst startet, kann es die [**StartService-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) verwenden, um ein Array von Argumenten anzugeben, die an die [**ServiceMain-Funktion des**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) Diensts übergeben werden sollen. Die **StartService-Funktion** gibt zurück, nachdem ein neuer Thread erstellt wurde, um die **ServiceMain-Funktion** auszuführen. Das Dienststeuerungsprogramm kann den Status des neu gestarteten Diensts in einer [**SERVICE \_ STATUS-Struktur**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) abrufen, indem die [**QueryServiceStatus-Funktion aufgerufen**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) wird. Während der Initialisierung sollte **das dwCurrentState-Member** SERVICE \_ START PENDING \_ lauten. Das **dwWaitHint-Member** ist ein Zeitintervall in Millisekunden, das angibt, wie lange das Dienststeuerungsprogramm warten soll, bevor **QueryServiceStatus erneut aufruft.** Nach Abschluss der Initialisierung ändert der Dienst **dwCurrentState** in SERVICE \_ RUNNING.

Der Dienststeuerungs-Manager unterstützt das Übergeben benutzerdefinierter Umgebungsvariablen an einen Dienst beim Start nicht. Außerdem erkennt der Dienststeuerungs-Manager während der Ausführung des Diensts keine Änderungen an Umgebungsvariablen und gibt sie weiter. Anstatt einen Dienst von einer Umgebungsvariablen abhängig zu machen, verwenden Sie Registrierungswerte oder [**ServiceMain-Argumente.**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)

Im Folgenden finden Sie eine vereinfachte Übersicht darüber, was geschieht, wenn ein typischer Dienst vom Dienststeuerungs-Manager gestartet wird:

-   Der SCM liest den Dienstpfad aus der Registrierung und bereitet den Start des Diensts vor. Dies schließt das Abrufen der Dienstsperre ein. Jeder Versuch, einen anderen Dienst zu starten, während die Dienstsperre besteht, wird blockiert, bis die Dienstsperre freigegeben wird.
-   Der SCM startet den Prozess und wartet, bis der untergeordnete Prozess beendet wird (was auf einen Fehler hinweist) oder den Status SERVICE \_ RUNNING meldet.
-   Die Anwendung führt ihre sehr einfache Initialisierung durch und ruft die [**StartServiceCtrlDispatcher-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) auf.
-   [**StartServiceCtrlDispatcher stellt**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) eine Verbindung mit dem Dienststeuerungs-Manager und startet einen zweiten Thread, der die [**ServiceMain-Funktion**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) für den Dienst aufruft. **ServiceMain** sollte service \_ running so bald wie möglich melden.
-   Wenn der Dienststeuerungs-Manager benachrichtigt wird, dass der Dienst ausgeführt wird, wird die Dienstsperre wieder frei.

Wenn der Dienst seinen Status nicht innerhalb von 80 Sekunden plus dem letzten Wartehinweis aktualisiert, stellt der Dienststeuerungs-Manager fest, dass der Dienst nicht mehr reagiert hat. Der Dienststeuerungs-Manager protokolliert ein Ereignis und stoppt den Dienst.

Wenn das Programm einen Treiberdienst startet, wird [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) zurückgegeben, nachdem die Initialisierung des Gerätetreibers abgeschlossen wurde.

Weitere Informationen finden Sie unter [Starten eines Diensts.](starting-a-service.md)

 

 
