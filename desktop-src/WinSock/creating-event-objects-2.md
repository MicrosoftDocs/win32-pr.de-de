---
description: Der Ws2-32.dll stellt Einrichtungen für die Erstellung von Ereignisobjekten sowohl für Anwendungen als auch für Dienstanbieter zur Verfügung, obwohl in den meisten Fällen Ereignisobjekte \_ von Anwendungen erstellt werden.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Erstellen von Ereignisobjekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab867e6398db4b5c97303c8739431d7baaca311daf8d103f4375721e96a864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051698"
---
# <a name="creating-event-objects"></a>Erstellen von Ereignisobjekten

Der Ws2-32.dll stellt Einrichtungen für die Erstellung von Ereignisobjekten sowohl für Anwendungen als auch für Dienstanbieter zur Verfügung, obwohl in den meisten Fällen Ereignisobjekte \_ von Anwendungen erstellt werden. Ereignisobjektdienste werden Windows Sockets-Dienstanbietern über [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) zur Verfügung gestellt, einfach als praktischen Mechanismus für jede interne Verarbeitung, die von derselben profitieren kann. Beachten Sie, dass das Ereignisobjekthand handle nur im Kontext des aufrufenden Prozesses gültig ist. In Windows umgebungen erfolgt die Umsetzung von Ereignisobjekten über die nativen Ereignisdienste, die vom Betriebssystem bereitgestellt werden.

 

 



