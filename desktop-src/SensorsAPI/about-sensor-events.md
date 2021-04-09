---
description: Die Sensor-API kann Ereignis Benachrichtigungen bereitstellen.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Informationen zu Sensor-API-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867620"
---
# <a name="about-sensor-api-events"></a>Informationen zu Sensor-API-Ereignissen

Die Sensor-API kann Ereignis Benachrichtigungen bereitstellen.

Wenn Sie sich beim Empfangen von Ereignissen über [**iSensor:: seteventsink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) oder [**isensormanager:: seteventsink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)registrieren, müssen Sie einen Zeiger auf eine Rückruf Schnittstelle bereitstellen. Sie müssen die Methoden der Rückruf Schnittstelle in Ihrem Code implementieren. Die Sensor-API definiert die folgenden Rückruf Schnittstellen:

-   [**Isenevents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implementieren Sie diese Schnittstelle, um Ereignisse von Sensoren zu empfangen. Sensoren können Ihre Anwendung über neue Daten, Änderungen am Sensor Zustand, Sensor Trennung und benutzerdefinierte Ereignisse benachrichtigen, die vom Sensorhersteller definiert werden.
-   [**Isensormanagerevents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implementieren Sie diese Schnittstelle, um Ereignisse vom Sensor-Manager zu empfangen. Der Sensor-Manager kann die Anwendung Benachrichtigen, wenn ein Sensor eine Verbindung herstellt und daher möglicherweise zur Verwendung verfügbar ist.

Sie können Ereignis Benachrichtigungen abbrechen, indem Sie " [**lteventsink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) " erneut aufrufen. dieses Mal wird ein **null** -Wert über den-Parameter übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sensor-API-Ereignissen](using-sensor-api-events.md)
</dt> </dl>

 

 
