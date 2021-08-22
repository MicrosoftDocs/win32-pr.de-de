---
description: Die Sensor-API kann Ereignisbenachrichtigungen bereitstellen.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Informationen zu Sensor-API-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af21bfed2a36c0c79fa46811221afbf2fcf87a4a5f15cf21adfbeaac8601f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003893"
---
# <a name="about-sensor-api-events"></a>Informationen zu Sensor-API-Ereignissen

Die Sensor-API kann Ereignisbenachrichtigungen bereitstellen.

Wenn Sie sich für den Empfang von Ereignissen registrieren, müssen Sie entweder über [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) oder [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)einen Zeiger auf eine Rückrufschnittstelle bereitstellen. Sie müssen die Methoden der Rückrufschnittstelle in Ihrem Code implementieren. Die Sensor-API definiert die folgenden Rückrufschnittstellen:

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implementieren Sie diese Schnittstelle, um Ereignisse von Sensoren zu empfangen. Sensoren können Ihre Anwendung über neue Daten, Änderungen des Sensorzustands, die Trennung des Sensors und benutzerdefinierte Ereignisse benachrichtigen, die vom Sensorhersteller definiert werden.
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implementieren Sie diese Schnittstelle, um Ereignisse vom Sensor-Manager zu empfangen. Der Sensor-Manager kann Ihre Anwendung benachrichtigen, wenn ein Sensor verbunden wird, und ist daher möglicherweise für die Verwendung verfügbar.

Sie können Ereignisbenachrichtigungen abbrechen, indem [**Sie SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) erneut aufrufen. Dieses Mal übergeben Sie einen **NULL-Wert** über den -Parameter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sensor-API-Ereignissen](using-sensor-api-events.md)
</dt> </dl>

 

 
