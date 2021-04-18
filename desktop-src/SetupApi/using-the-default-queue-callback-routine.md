---
description: Die standardmäßige Warteschlangen Rückruf-Routine kann angegeben werden, um Benachrichtigungen zu verarbeiten, die von setupcommitfilequeue gesendet werden, oder Sie kann von einer benutzerdefinierten Rückruf Routine aufgerufen werden, die auf der Funktionalität der Standard Warteschlangen-Rückruf Routine basiert.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Verwenden der Standard Warteschlangen-Rückruf Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347578"
---
# <a name="using-the-default-queue-callback-routine"></a>Verwenden der Standard Warteschlangen-Rückruf Routine

Die standardmäßige Warteschlangen Rückruf-Routine kann angegeben werden, um Benachrichtigungen zu verarbeiten, die von [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)gesendet werden, oder Sie kann von einer benutzerdefinierten Rückruf Routine aufgerufen werden, die auf der Funktionalität der Standard Warteschlangen-Rückruf Routine basiert.

In den folgenden Abschnitten wird erläutert, wie Sie den Kontext initialisieren und beenden, der von einer Standard Warteschlangen-Rückruf Routine verwendet wird. Außerdem wird beschrieben, wie die Standard Warteschlangen-Rückruf Routine mit [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) oder einer benutzerdefinierten Rückruf Routine verwendet wird.

-   [Initialisieren und Beenden des Rückruf Kontexts](initializing-and-terminating-the-callback-context.md)
-   [Aufrufen der Standard Warteschlangen-Rückruf Routine](calling-the-default-queue-callback-routine.md)

 

 



