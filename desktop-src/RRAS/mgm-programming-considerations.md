---
title: Überlegungen zur MGM-Programmierung
description: Beachten Sie beim Entwickeln von Multicast-Gruppen-Manager-Clients die folgenden Richtlinien.
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, Überlegungen zur Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a749406384068cc7dce54fab237c261926149aaf9b2fbdca23327c7b75f3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029625"
---
# <a name="mgm-programming-considerations"></a>Überlegungen zur MGM-Programmierung

Beachten Sie beim Entwickeln von Multicastgruppen-Manager-Clients die folgenden Richtlinien:

-   Funktionsaufrufe müssen innerhalb des Routerprozesses vorgenommen werden. Wenn Funktionen von einem anderen Prozess aufgerufen werden, sind ihre Ergebnisse ungültig. Der Client interagiert nicht mit dem Multicastgruppen-Manager.
-   Clients, die die MGM-API verwenden, müssen eine eigene Fehlerüberprüfung bereitstellen, um sicherzustellen, dass nur gültige Daten an den Multicastgruppen-Manager übergeben werden. MGM-Funktionen geben keine detaillierten Fehlermeldungen zu ungültigen Parametern zurück. Der ERROR \_ INVALID \_ PARAMETER-Wert wird ohne Erklärung zurückgegeben.
-   Clients sollten beim Aufrufen von MGM-Funktionen mit Bedacht Sperren verwenden. Dadurch können Deadlocks verhindert werden. Beim Aufrufen von MGM-Funktionen sollten Clients keine Sperren enthalten, die gleichzeitig in einem Rückruf des Multicastgruppen-Managers gehalten werden können.

 

 




