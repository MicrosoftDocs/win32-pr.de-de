---
title: SystemMonitor-Ereignisse
description: Die SystemMonitor-Klasse verfügt über die folgenden Ereignisse.
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3584eed86abcaef019f0fc8f8bd794a80abca1143286317189889231bbc2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882946"
---
# <a name="systemmonitor-events"></a>SystemMonitor-Ereignisse

Die [**SystemMonitor-Klasse**](systemmonitor.md) verfügt über die folgenden Ereignisse:

-   [**OnCounterAdded**](systemmonitor-oncounteradded.md)
-   [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
-   [**OnCounterSelected**](-systemmonitor-oncounterselected.md)
-   [**OnDblClick**](-systemmonitor-ondblclick.md)
-   [**OnSampleCollected**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> Sie müssen vom Ereignishandler zurückgeben, bevor das [**Updateintervall**](systemmonitor-updateinterval.md) abläuft. Andernfalls zeigt SYSMON ein Meldungsfeld an, das dem Benutzer anzeigt, dass für das vorherige Aktualisierungsintervall keine Stichproben von Indikatorwerten entnommen werden konnten.

 

 

 




