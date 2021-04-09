---
title: Überlegungen zur Programmiersprache
description: Beachten Sie beim Entwickeln von Multicast-Gruppen-Manager-Clients die folgenden Richtlinien.
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, Überlegungen zur Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856504"
---
# <a name="mgm-programming-considerations"></a>Überlegungen zur Programmiersprache

Beachten Sie beim Entwickeln von Multicast-Gruppen-Manager-Clients die folgenden Richtlinien:

-   Funktionsaufrufe müssen innerhalb des routerprozesses erfolgen. Wenn Funktionen von einem anderen Prozess aufgerufen werden, sind die Ergebnisse nicht gültig. der Client interagiert nicht mit dem Multicast-Gruppen-Manager.
-   Clients, die die MGM-API verwenden, müssen eine eigene Fehlerüberprüfung bereitstellen, um sicherzustellen, dass nur gültige Daten an den Multicast Gruppen-Manager übermittelt werden. Von den MGM-Funktionen werden keine ausführlichen Fehlermeldungen zu ungültigen Parametern zurückgegeben. der \_ ungültige \_ Parameter Wert wird ohne Erklärung zurückgegeben.
-   Clients sollten bei der Verwendung von Sperren beim Aufrufen von MGM-Funktionen Vorsicht walten lassen. Dadurch können Deadlocks verhindert werden. Wenn Sie die Funktionen von "MGM" aufrufen, sollten Clients keine Sperren enthalten, die gleichzeitig in einem Rückruf vom Multicast-Gruppen-Manager aufbewahrt werden können.

 

 




