---
description: Das Sensorobjekt stellt einen bestimmten Sensor dar.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Das Sensorobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ad666153be31958bb758ca4b504e10591ccbe29c9d37355499c9d22c5aae2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666410"
---
# <a name="the-sensor-object"></a>Das Sensorobjekt

Das Sensorobjekt stellt einen bestimmten Sensor dar.

Die Sensor-API stellt jeden Sensor als Sensorobjekt dar. Sie können mit einem bestimmten Sensorobjekt über die [**ISensor-Schnittstelle**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) arbeiten. Diese Schnittstelle ermöglicht Ihnen:

-   Rufen Sie Metadaten zum Sensor ab, z. B. id, type oder friendly name.
-   Rufen Sie Informationen zu den spezifischen Daten ab, die der Sensor bereitstellen kann.
-   Rufen Sie die Daten synchron ab.
-   Rufen Sie Zustandsinformationen ab, z. B. ob der Sensor bereit ist.
-   Geben Sie an, welche Ereignisse ihr Programm empfangen soll.
-   Geben Sie die Rückrufschnittstelle an, die die Sensor-API verwenden kann, um Ihrem Programm Ereignisbenachrichtigungen zur Verfügung zu stellen.

 

 



