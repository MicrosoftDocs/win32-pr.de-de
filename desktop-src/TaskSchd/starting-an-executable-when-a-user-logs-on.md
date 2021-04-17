---
title: Starten einer ausführbaren Datei, wenn sich ein Benutzer anmeldet
description: Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn sich ein Benutzer anmeldet, definieren Sie einen LOGON-und eine ausführbare Aktion.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Taskplaner Beispiele Taskplaner, LOGON-Auslösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387952"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>Starten einer ausführbaren Datei, wenn sich ein Benutzer anmeldet

Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn sich ein Benutzer anmeldet, definieren Sie einen LOGON-und eine ausführbare Aktion.

## <a name="logon-trigger"></a>Logon-Auslösung

LOGON-Trigger werden über die Start Grenze aktiviert, starten die ausführbare Datei jedoch erst, wenn sich ein angegebener Benutzer anmeldet. Sie können den Logon-Zeitpunkt angeben, der gestartet werden soll, wenn sich ein bestimmter Benutzer anmeldet, indem Sie den Benutzer in der [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) -Eigenschaft der [**iLogon-**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) Schnittstelle angeben ([**Logon-**](logontrigger.md) Auslösung für Skripterstellung).

## <a name="logontrigger-examples"></a>Logon-auslöserbeispiele

In den folgenden Beispielen wird Notepad gestartet, nachdem sich ein Benutzer angemeldet hat.

-   [Beispiel für LOGON-Auslösung (Skripterstellung)](logon-trigger-example--scripting-.md)
-   [Beispiel eines LOGON-Auslösers (C++)](logon-trigger-example--c---.md)
-   [Beispiel eines LOGON-Auslösers (XML)](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




