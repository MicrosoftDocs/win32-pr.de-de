---
title: Systemmonitor-Ereignisse
description: 'Die Systemmonitor-Klasse weist die folgenden Ereignisse auf:'
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337136"
---
# <a name="systemmonitor-events"></a>Systemmonitor-Ereignisse

Die [**Systemmonitor**](systemmonitor.md) -Klasse weist die folgenden Ereignisse auf:

-   [**Oncounteradded**](systemmonitor-oncounteradded.md)
-   [**Oncounterdeleted**](-systemmonitor-oncounterdeleted.md)
-   [**Oncounterselected**](-systemmonitor-oncounterselected.md)
-   [**Ondblclick**](-systemmonitor-ondblclick.md)
-   [**Onsamplecollected**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> Sie müssen den Ereignishandler zurückgeben, bevor das [**Aktualisierungs Intervall**](systemmonitor-updateinterval.md) abläuft. Andernfalls zeigt sysmon ein Meldungs Feld an, das dem Benutzer anzeigt, dass es für das vorherige Aktualisierungs Intervall keine Stichproben von zählungs Werten gibt.

 

 

 




