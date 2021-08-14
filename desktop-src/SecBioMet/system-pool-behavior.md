---
title: Systempoolverhalten
description: Erläuterung der Aktionen, die vom Systempool ausgeführt werden, wenn Ereignishinweise gesendet werden und keine biometrischen Vorgänge ausstehen.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923cfff4b36bd14d100ce1f73db455be5261d75dc2c5be1eddc8f9d6af87fce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911593"
---
# <a name="system-pool-behavior"></a>Systempoolverhalten

In der folgenden Erläuterung werden die Aktionen hervorgehoben, die vom Systempool ausgeführt werden, wenn Ereignishinweise gesendet werden und keine biometrischen Vorgänge ausstehen.

## <a name="event-dispatching"></a>Ereignisdisponierung

Wenn eine biometrische Einheit einen Ereignishinweis generiert, verwendet der Systempool einen kaskadierenden Filter, um den Hinweis zu senden und ihm eine der folgenden Prioritätsebenen zuzuweisen:

-   Expliziten Abgleichs- und Registrierungsanforderungen, die von Clients generiert werden, wird eine hohe Priorität zugewiesen.
-   Mittlere Priorität wird unerwarteten oder nicht beanspruchten Abgleichs- oder Registrierungsereignissen zugewiesen.
-   Navigationsereignissen wird eine niedrige Priorität zugewiesen.

Erfassungsereignisse werden in der folgenden Reihenfolge übermittelt:

-   Wenn das aktuelle Fokusfenster auf einen Abgleich oder einen Registrierungsvorgang wartet, wird das Beispiel verarbeitet und an den Client gesendet, der das aktuelle Fokusfenster besitzt.
-   Wenn das Erfassungsereignis vom aktuellen Fokusfenster nicht beansprucht wird und ein nicht beanspruchter Ereignishandler beim Windows biometrischen Diensts registriert wurde, wird das Erfassungsereignis an diesen Handler gesendet.
-   Wenn das Ereignis nicht beansprucht wird, wird es verworfen.

Wenn das Ereignis ein Navigationsereignis ist und ein Navigationsereignishandler beim Windows biometrischen Diensts registriert wurde, wird das Erfassungsereignis an diesen Handler gesendet. Wenn kein Ereignishandler vorhanden ist, wird das Ereignis verworfen.

## <a name="idle-mode"></a>Leerlaufmodus

Wenn keine Clients auf den Abschluss expliziter Abgleichs- oder Registrierungsanforderungen warten, bestimmt der Systempool, ob wiederholte Erfassungsanforderungen automatisch generiert und der resultierende Ereignishinweis an den nicht angeforderten Ereignishandler gesendet oder auf Navigationsereignisse gewartet und an den Navigationsereignishandler gesendet werden soll.

Wenn ein nicht beanspruchter Ereignishandler beim Windows Biometrischer Dienst registriert wurde, führt der Systempool die folgenden Aktionen aus:

-   Der Navigationsmodus für den Sensor ist deaktiviert.
-   Nicht beanspruchte Vorgänge werden unabhängig vom Fensterfokus an den Ereignishandler gesendet.
-   Wenn keine ausstehenden Anforderungen für einen biometrischen Vorgang vorliegen, wird eine automatische Erfassung durchgeführt.

Wenn ein Navigationshandler beim Windows biometrischen Dienst registriert wurde, führt der Systempool folgende Schritte aus:

-   Die biometrischen Einheiten im Systempool werden in einen Navigationszustand versetzt, wenn keine biometrischen Vorgänge ausstehen.
-   Navigationsereignisse werden deaktiviert, wenn ein Client eine Übereinstimmungs- oder Registrierungsereignisbenachrichtigung sendet.
-   Wenn ein Handler für nicht beanspruchte Ereignisse registriert wurde, werden Navigationsereignisse deaktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Privater Sensorpool](private-sensor-pool.md)
</dt> <dt>

[Sensorpools](sensor-pools.md)
</dt> <dt>

[Systemsensorpool](system-sensor-pool.md)
</dt> </dl>

 

 




