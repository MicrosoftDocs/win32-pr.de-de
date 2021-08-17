---
description: In den Setupfunktionen ist eine Standardrückrufroutine (SetupDefaultQueueCallback) enthalten, die Sie zum Verarbeiten von Benachrichtigungen verwenden können, die von SetupCommitFileQueue zurückgegeben werden.
ms.assetid: c6ba6398-4119-4bdd-b264-1bc645800b03
title: Standardroutine für Warteschlangenrückrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a85c70cae5cccd8302caa1b3eb414bf523b4d9826eda6bc5ad2b65e9f7bfd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887446"
---
# <a name="default-queue-callback-routine"></a>Standardroutine für Warteschlangenrückrufe

In den Setupfunktionen ist eine Standardrückrufroutine [**(SetupDefaultQueueCallback)**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)enthalten, die Sie zum Verarbeiten von Benachrichtigungen verwenden können, die von [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)zurückgegeben werden.

In den folgenden Abschnitten wird das Format der Standardroutine für den Warteschlangenrückruf erläutert. Dabei wird die Standardroutine für Warteschlangenrückrufe mit [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)verwendet. Außerdem wird erläutert, wie Sie eine Filterrückrufroutine erstellen, die auf der Funktionalität der Standardroutine für Warteschlangenrückrufe aufbaut.

-   [Informationen zur Standardroutine für Warteschlangenrückrufe](about-the-default-queue-callback-routine.md)
-   [Verwenden der Standardroutine für Warteschlangenrückrufe](using-the-default-queue-callback-routine.md)
-   [Standardreferenz zur Warteschlangenrückrufroutine](default-queue-callback-routine-reference.md)

 

 



