---
description: Das Sensor Objekt stellt einen bestimmten Sensor dar.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Das Sensor Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348727"
---
# <a name="the-sensor-object"></a>Das Sensor Objekt

Das Sensor Objekt stellt einen bestimmten Sensor dar.

Die Sensor-API stellt die einzelnen Sensoren als Sensor Objekt dar. Sie können über die [**iSensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) -Schnittstelle mit einem bestimmten Sensor Objekt arbeiten. Diese Schnittstelle ermöglicht Folgendes:

-   Abrufen von Metadaten über den Sensor, z. b. ID, Typ oder Anzeige Name.
-   Abrufen von Informationen über die spezifischen Daten, die der Sensor bereitstellen kann.
-   Synchrones Abrufen der Daten.
-   Abrufen von Zustandsinformationen, z. b. ob der Sensor bereit ist.
-   Geben Sie an, welche Ereignisse ihr Programm empfängt.
-   Geben Sie die Rückruf Schnittstelle an, die die Sensor-API verwenden kann, um dem Programm Ereignis Benachrichtigungen bereitzustellen.

 

 



