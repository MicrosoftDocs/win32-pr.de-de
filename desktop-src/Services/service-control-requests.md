---
description: Um Steuerungsanforderungen an einen laufenden Dienst zu senden, verwendet ein Dienst Steuerungsprogramm die ControlService-Funktion.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Dienst Steuerungsanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346508"
---
# <a name="service-control-requests"></a>Dienst Steuerungsanforderungen

Um Steuerungsanforderungen an einen laufenden Dienst zu senden, verwendet ein Dienst Steuerungsprogramm die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion. Diese Funktion gibt einen Steuerelement Wert an, der an die [**handlerex**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) -Funktion des angegebenen Dienstanbieter übermittelt wird. Bei diesem Steuerungs Wert kann es sich um einen benutzerdefinierten Code handeln, oder es kann sich um einen der Standard Codes handeln, die dem aufrufenden Programm das Ausführen der folgenden Aktionen ermöglichen:

-   Beendet einen Dienst (Dienst \_ Steuerungs \_ Ende).
-   Hält einen Dienst an (Anhalten der Dienst \_ Steuerung \_ ).
-   Fortsetzen der Ausführung eines angehaltenen Dienstanbieter (Dienst \_ Steuerung \_ fortsetzen).
-   Abrufen aktualisierter Statusinformationen von einem Dienst ( \_ Dienststeuerungs- \_ Abfrage).

Jeder Dienst gibt die Steuerungs Werte an, die er akzeptiert und verarbeitet. Wenn Sie bestimmen möchten, welche der Standard Steuerelement Werte von einem Dienst akzeptiert werden, verwenden Sie die Funktion [**QueryServiceStatus usex**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) , oder geben Sie den \_ Wert des Dienststeuerungs- \_ Abfrage Steuer Elements in einem Aufrufen der [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion an. Der **dwcontrolsaccepted** -Member der [**Dienst \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Struktur, die von diesen Funktionen zurückgegeben wird, gibt an, ob der Dienst beendet, angehalten oder fortgesetzt werden kann. Alle Dienste akzeptieren den \_ Wert der Dienststeuerungs- \_ Abfrage Steuerung.

Die Funktion [**queryservicestatusex**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) meldet den aktuellen Status für einen angegebenen Dienst, erhält aber keinen aktualisierten Status vom Dienst selbst. Durch die Verwendung des Dienstkontroll-Steuerelement-Steuerelement- \_ \_ Steuer Elements in einem Befehl von [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) wird sichergestellt, dass die zurückgegebenen Statusinformationen aktuell

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines Dienstanbieter mit SC](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



