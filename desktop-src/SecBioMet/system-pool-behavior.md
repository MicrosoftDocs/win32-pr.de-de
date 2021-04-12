---
title: System Pool Verhalten
description: Erörterung der Aktionen, die vom System Pool durchgeführt werden, wenn Ereignis Hinweise gesendet werden und keine biometrischen Vorgänge ausstehen.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a82d957b2b1b4968835eec1482662e30765e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388366"
---
# <a name="system-pool-behavior"></a>System Pool Verhalten

In der folgenden Erörterung werden die Aktionen, die vom System Pool ausgeführt werden, wenn Ereignis Hinweise gesendet werden und keine biometrischen Vorgänge ausstehen, hervorgehoben.

## <a name="event-dispatching"></a>Ereignis Verteilung

Wenn eine biometrische Einheit einen Ereignis Hinweis generiert, verwendet der System Pool einen kaskadierenden Filter, um den Hinweis zu senden und ihm eine der folgenden Prioritätsstufen zuzuweisen:

-   Hohe Priorität wird expliziten übereinstimmenden und Registrierungsanforderungen zugewiesen, die von-Clients generiert werden.
-   Die mittlere Priorität wird unerwarteten oder nicht beanspruchten übereinstimmenden oder Registrierungs Ereignissen zugewiesen.
-   Einem Navigations Ereignis werden niedrige Priorität zugewiesen.

Aufzeichnungs Ereignisse werden in der folgenden Reihenfolge übermittelt:

-   Wenn das aktuelle Fokus Fenster auf einen übereinstimmenden oder einen Registrierungsvorgang wartet, wird das Beispiel verarbeitet und an den Client gesendet, der das aktuelle Fokus Fenster besitzt.
-   Wenn das Aufzeichnungs Ereignis vom aktuellen Fokus Fenster nicht beansprucht wird und ein nicht erforderter Ereignishandler beim Windows-biometrischen Dienst registriert wurde, wird das Aufzeichnungs Ereignis an diesen Handler gesendet.
-   Wenn das Ereignis weiterhin nicht beansprucht wird, wird es verworfen.

Wenn das Ereignis ein Navigations Ereignis ist und ein Navigations Ereignishandler beim Windows-biometrischen Dienst registriert wurde, wird das Aufzeichnungs Ereignis an diesen Handler gesendet. Wenn kein Ereignishandler vorhanden ist, wird das Ereignis verworfen.

## <a name="idle-mode"></a>Leerlauf Modus

Wenn keine Clients auf den Abschluss der expliziten übereinstimmenden oder Registrierungsanforderungen warten, bestimmt der System Pool, ob automatisch wiederholte Aufzeichnungs Anforderungen generiert werden sollen, und sendet die resultierende Ereignis Notiz an den nicht beanspruchten Ereignishandler, oder er wartet auf Navigations Ereignisse und sendet Sie an den Navigations Ereignishandler.

Wenn ein nicht erforderter Ereignishandler beim Windows-biometrischen Dienst registriert wurde, führt der System Pool die folgenden Aktionen aus:

-   Der Navigationsmodus für den Sensor ist deaktiviert.
-   Nicht beanspruchte Vorgänge werden unabhängig vom Fenster Fokus an den Ereignishandler gesendet.
-   Wenn für einen biometrischen Vorgang keine ausstehenden Anforderungen vorliegen, wird eine automatische Erfassung ausgeführt.

Wenn ein Navigations Handler beim Windows-biometrischen Dienst registriert wurde, führt der System Pool Folgendes aus:

-   Die biometrischen Einheiten im System Pool werden in einen Navigations Zustand versetzt, wenn keine biometrischen Vorgänge ausstehen.
-   Navigations Ereignisse sind deaktiviert, wenn ein Client eine Übereinstimmungs-oder Registrierungs Ereignis Notiz sendet.
-   Wenn ein nicht erforderter Ereignishandler registriert wurde, werden Navigations Ereignisse deaktiviert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Privater Sensor Pool](private-sensor-pool.md)
</dt> <dt>

[Sensor Pools](sensor-pools.md)
</dt> <dt>

[System Sensor Pool](system-sensor-pool.md)
</dt> </dl>

 

 




