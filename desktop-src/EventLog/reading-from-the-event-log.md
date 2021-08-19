---
description: Eine Ereignisanzeigeanwendung verwendet die OpenEventLog-Funktion, um das Ereignisprotokoll für eine Ereignisquelle zu öffnen.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lesen aus dem Ereignisprotokoll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d0756ba7d9609bca285ce33d69738984badf7effff8867fc5c3e1943b09145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151535"
---
# <a name="reading-from-the-event-log"></a>Lesen aus dem Ereignisprotokoll

Eine Ereignisanzeigeanwendung verwendet die [**OpenEventLog-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) um das Ereignisprotokoll für eine Ereignisquelle zu öffnen. Die Ereignisanzeige kann dann die [**ReadEventLog-Funktion**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) verwenden, um Ereignisdatensätze aus dem Protokoll zu lesen. **ReadEventLog** gibt einen Puffer zurück, der eine [**EVENTLOGRECORD-Struktur**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) und zusätzliche Informationen enthält, die ein protokolliertes Ereignis beschreiben. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Lesen aus dem Ereignisprotokoll](images/readlog.png)

Beispielcode finden Sie unter [Abfragen von Ereignisinformationen.](querying-for-event-source-messages.md)

 

 



