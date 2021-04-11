---
description: Eine Ereignisanzeige Anwendung verwendet die OpenEventLog-Funktion, um das Ereignisprotokoll für eine Ereignis Quelle zu öffnen.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lesen aus dem Ereignisprotokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042098"
---
# <a name="reading-from-the-event-log"></a>Lesen aus dem Ereignisprotokoll

Eine Ereignisanzeige Anwendung verwendet die [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) -Funktion, um das Ereignisprotokoll für eine Ereignis Quelle zu öffnen. Die Ereignisanzeige kann dann mit der [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) -Funktion Ereignisdaten Sätze aus dem Protokoll lesen. **ReadEventLog** gibt einen Puffer zurück, der eine [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Struktur und zusätzliche Informationen enthält, die ein protokolliertes Ereignis beschreiben. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Lesen aus dem Ereignisprotokoll](images/readlog.png)

Beispielcode finden Sie unter [Abfragen von Ereignis Informationen](querying-for-event-source-messages.md).

 

 



