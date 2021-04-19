---
description: Zum Starten eines Dienst-oder Treiber Dienstanbieter verwendet das Dienst Steuerungsprogramm die Start Service-Funktion.
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: Dienststart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5fcd9ee820357e75bf07649da8e6c5445d3f42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369807"
---
# <a name="service-startup"></a>Dienststart

Zum Starten eines Dienst-oder Treiber Dienstanbieter verwendet das Dienst Steuerungsprogramm die [**Start Service**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) -Funktion. Die Funktion " **StartService** " schlägt fehl, wenn die Datenbank gesperrt ist. Wenn dies auftritt, sollte das Dienst Steuerungsprogramm einige Sekunden warten und " **StartService** " erneut aufrufen. Der aktuelle Sperr Status der Datenbank kann durch Aufrufen der [**queryservicelockstatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) -Funktion überprüft werden.

Wenn das Dienst Steuerungsprogramm einen Dienst startet, kann es die [**Start Service**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) -Funktion verwenden, um ein Array von Argumenten anzugeben, die an die [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion des dienstanders übermittelt werden sollen. Die **Start Service** -Funktion gibt zurück, nachdem ein neuer Thread erstellt wurde, um die **ServiceMain** -Funktion auszuführen. Das Dienst Steuerungsprogramm kann den Status des neu gestarteten dienstangangs in einer [**Dienst \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Struktur abrufen, indem er die [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) -Funktion aufrufen. Während der Initialisierung sollte der **dwcurrentstate** -Member "Service \_ Start Pending" lauten \_ . Beim **dwwaithint** -Element handelt es sich um ein Zeitintervall (in Millisekunden), das angibt, wie lange das Dienst Steuerungsprogramm warten soll, bis der **QueryServiceStatus** erneut aufgerufen wird. Wenn die Initialisierung vollständig ist, ändert der Dienst **dwcurrentstate** in den Dienst, der \_ ausgeführt wird.

Der Dienststeuerungs-Manager unterstützt das Übergeben von benutzerdefinierten Umgebungsvariablen an einen Dienst beim Start nicht. Der Dienststeuerungs-Manager erkennt und übergibt auch keine Änderungen an Umgebungsvariablen, während der Dienst ausgeführt wird. Anstatt einen Dienst von einer Umgebungsvariablen abhängig zu gestalten, verwenden Sie Registrierungs Werte oder [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Argumente.

Im folgenden finden Sie eine vereinfachte Übersicht darüber, was geschieht, wenn ein typischer Dienst vom Dienststeuerungs-Manager gestartet wird:

-   Der SCM liest den Dienst Pfad aus der Registrierung und bereitet den Start des Dienstanbieter vor. Dies schließt das Abrufen der Dienst Sperre ein. Jeder Versuch, einen anderen Dienst zu starten, während die Dienst Sperre aufrechterhalten wird, wird blockiert, bis die Dienst Sperre aufgehoben wird.
-   Der SCM startet den Prozess und wartet, bis der untergeordnete Prozess beendet wird (was auf einen Fehler hinweist) oder meldet, dass der Dienst \_ ausgeführt wird.
-   Die Anwendung führt die sehr einfache Initialisierung durch und ruft die [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) -Funktion auf.
-   [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) stellt eine Verbindung mit dem Dienststeuerungs-Manager her und startet einen zweiten Thread, der die [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion für den Dienst aufruft. **ServiceMain** sollte melden, dass der Dienst \_ so schnell wie möglich ausgeführt wird.
-   Wenn der Dienststeuerungs-Manager benachrichtigt wird, dass der Dienst ausgeführt wird, wird die Dienst Sperre freigegeben.

Wenn der Dienst seinen Status nicht innerhalb von 80 Sekunden aktualisiert, zuzüglich des letzten warte Hinweises, stellt der Dienststeuerungs-Manager fest, dass der Dienst nicht mehr reagiert. Der Dienststeuerungs-Manager protokolliert ein Ereignis und beendet den Dienst.

Wenn das Programm einen Treiber Dienst startet, wird " [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) " zurückgegeben, nachdem die Initialisierung des Gerätetreibers abgeschlossen wurde.

Weitere Informationen finden Sie unter [Starten eines Dienstanbieter](starting-a-service.md).

 

 
