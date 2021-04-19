---
description: Die callhub-Nachverfolgung ist ein neues Feature in TAPI, Version 3,0.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Callhub-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362338"
---
# <a name="callhub-support"></a>Callhub-Unterstützung

Die callhub-Nachverfolgung ist ein neues Feature in TAPI, Version 3,0. Die callhub-Funktionalität wurde den Programmier Elementen TAPI 2,1 mit der Übermittlung von Windows 2000 hinzugefügt. Ein *callhub* stellt eine Drittanbieter Ansicht eines Aufrufes dar, und die Aufruf Handles von TAPI stellen die erste Ansicht eines Aufrufes dar. Bei der callhub-Nachverfolgung wird der Dienstanbieter aufgefordert, callhubs zu folgen und während der Lebensdauer eines callhubs Informationen über den Aufruf zu erhalten. Wenn neue Parteien beitreten und den callhub verlassen, sollte der Dienstanbieter TAPI informieren.

Ein Dienstanbieter muss keine neuen Funktionen implementieren, um callhub zu unterstützen. Er muss lediglich den **dwcallid** -Member der [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) -Struktur ausfüllen. In TAPI 3 sammelt TAPI alle Aufrufe mit dem gleichen **dwcallid** und erstellt ein callhub-handle, das von der Anwendung zum Nachverfolgen des Aufrufs verwendet werden kann.

 

 
