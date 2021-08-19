---
description: Um Steuerungsanforderungen an einen ausgeführten Dienst zu senden, verwendet ein Dienststeuerungsprogramm die ControlService-Funktion.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Dienststeuerungsanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4320aad28f8a176fbf4aaa6b51539256a376a01b8edea034341cae7831ca4c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967569"
---
# <a name="service-control-requests"></a>Dienststeuerungsanforderungen

Um Steuerungsanforderungen an einen ausgeführten Dienst zu senden, verwendet ein Dienststeuerungsprogramm die [**ControlService-Funktion.**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) Diese Funktion gibt einen Steuerelementwert an, der an die [**HandlerEx-Funktion**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) des angegebenen Diensts übergeben wird. Dieser Steuerelementwert kann ein benutzerdefinierter Code oder einer der Standardcodes sein, die es dem aufrufenden Programm ermöglichen, die folgenden Aktionen durchzuführen:

-   Beenden eines Diensts (SERVICE \_ CONTROL \_ STOP).
-   Anhalten eines Diensts (SERVICE \_ CONTROL \_ PAUSE).
-   Setzen Sie die Ausführung eines angehaltenen Diensts fort (SERVICE \_ CONTROL \_ CONTINUE).
-   Abrufen aktualisierter Statusinformationen von einem Dienst (SERVICE \_ CONTROL \_ INTERROGATE).

Jeder Dienst gibt die Steuerelementwerte an, die er akzeptiert und verarbeiten wird. Um zu bestimmen, welche standard-Steuerelementwerte von einem Dienst akzeptiert werden, verwenden Sie die [**QueryServiceStatusEx-Funktion,**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) oder geben Sie den SERVICE CONTROL INTERROGATE-Steuerelementwert in einem Aufruf der \_ \_ [**ControlService-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) an. Der **dwControlsAccepted-Member** der [**SERVICE \_ STATUS-Struktur,**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) der von diesen Funktionen zurückgegeben wird, gibt an, ob der Dienst beendet, angehalten oder fortgesetzt werden kann. Alle Dienste akzeptieren den SERVICE \_ CONTROL \_ INTERROGATE-Steuerungswert.

Die [**QueryServiceStatusEx-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) meldet den aktuellen Status für einen angegebenen Dienst, aber vom Dienst selbst wird kein aktualisierter Status angezeigt. Die Verwendung des SERVICE \_ CONTROL \_ INTERROGATE-Steuerelementwerts in einem Aufruf von [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) stellt sicher, dass die zurückgegebenen Statusinformationen aktuell sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines Diensts mit sc](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



