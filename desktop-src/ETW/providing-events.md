---
description: Anbieter sind Anwendungen, die die Ereignis Ablauf Verfolgungs Instrumentation enthalten.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Bereitstellen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977633"
---
# <a name="providing-events"></a>Bereitstellen von Ereignissen

Anbieter sind Anwendungen, die die Ereignis Ablauf Verfolgungs Instrumentation enthalten. Nachdem sich ein Anbieter registriert hat, kann ein Controller die Ereignis Ablauf Verfolgung im Anbieter aktivieren bzw. deaktivieren. Der Anbieter definiert seine Interpretation, dass er aktiviert oder deaktiviert wird. Im Allgemeinen werden von einem aktivierten Anbieter Ereignisse generiert, die nicht von einem deaktivierten Anbieter verwendet werden. Auf diese Weise können Sie der Anwendung die Ereignis Ablauf Verfolgung hinzufügen, ohne dass die Ereignisse immer generiert werden müssen.

In diesem Abschnitt erfahren Sie Folgendes:

-   [Ereignisse schreiben](writing-events.md)
-   [Verwandte Ereignisse schreiben](writing-related-events-in-an-end-to-end-scenario.md)
-   [Veröffentlichen Ihres Ereignis Schemas für die Freigabe mit Consumern](publishing-your-event-schema.md)

Informationen zum Steuern von Ereignis Ablauf Verfolgungs Sitzungen finden Sie unter [Steuern von Ereignis Ablauf Verfolgungs Sitzungen](controlling-event-tracing-sessions.md). Informationen zum Verarbeiten von Ereignissen von einem Ereignis Ablauf Verfolgungs Anbieter finden Sie unter Verwenden von [Ereignissen](consuming-events.md).

 

 



