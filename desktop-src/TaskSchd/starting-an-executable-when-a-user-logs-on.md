---
title: Starten einer ausführbaren Datei, wenn sich ein Benutzer anmeldet
description: Das Schreiben einer Aufgabe, die eine ausführbare Datei startet, wenn sich ein Benutzer anmeldet, erfolgt durch Definieren eines Anmeldetriggers und einer ausführbaren Aktion.
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- Taskplaner Beispiele Taskplaner , Logon-Trigger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd7cfc8412e33df47841cf33d2a4950061d39d77fbe76d3b896b5d220b04b8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132122"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>Starten einer ausführbaren Datei, wenn sich ein Benutzer anmeldet

Das Schreiben einer Aufgabe, die eine ausführbare Datei startet, wenn sich ein Benutzer anmeldet, erfolgt durch Definieren eines Anmeldetriggers und einer ausführbaren Aktion.

## <a name="logon-trigger"></a>Logon Trigger

Logon-Trigger werden durch ihre Startgrenze aktiviert, starten die ausführbare Datei jedoch erst, wenn sich ein angegebener Benutzer anmeldet. Sie können den Anmeldetrigger angeben, der gestartet werden soll, wenn sich ein bestimmter Benutzer anmeldet, indem Sie den Benutzer in der [**UserId-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) der [**ILogonTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) angeben ([**LogonTrigger**](logontrigger.md) für Skripterstellung).

## <a name="logontrigger-examples"></a>LogonTrigger-Beispiele

In den folgenden Beispielen wird Editor gestartet, nachdem sich ein Benutzer anmeldet.

-   [Logon Trigger Example (Scripting) (Beispiel für Logon-Trigger (Skripterstellung))](logon-trigger-example--scripting-.md)
-   [Logon Trigger Example (C++) (Beispiel für Logon-Trigger (C++))](logon-trigger-example--c---.md)
-   [Logon Trigger Example (XML) (Beispiel für Logon-Trigger (XML))](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




