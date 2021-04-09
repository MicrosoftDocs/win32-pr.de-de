---
title: Statische und automatische statische Routen
description: In der Regel werden Routen zu Remote Netzwerken durch Routing Protokolle dynamisch abgerufen.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3faa8931e0fee5c75f598b920b7b97a1e0e829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947997"
---
# <a name="static-and-autostatic-routes"></a>Statische und automatische statische Routen

In der Regel werden Routen zu Remote Netzwerken durch Routing Protokolle dynamisch abgerufen. *Der Administrator kann jedoch auch einen* Ausgangs Ausgangs für die Routing Tabelle angeben, indem er Routen manuell bereitstellt. Diese Routen werden als *statisch* bezeichnet. Eine statische Route ist einer Schnittstelle zugeordnet, die das Remote Netzwerk darstellt. Im Gegensatz zu dynamischen Routen werden statische Routen auch dann beibehalten, wenn der Router neu gestartet wird oder die Schnittstelle deaktiviert ist.

Eine *Automatische statische* Route wird durch ein Routing Protokoll abgerufen, aber sobald Sie sich wie eine statische Route verhält, verhält sie sich. Der Vorgang zum Abrufen von automatisch statischen Routen lautet wie folgt: der IP-oder IPX-routermanager gibt eine Anforderung aus, dass ein Routing Protokoll die Routing Informationen für eine bestimmte Schnittstelle aktualisiert. Die Ergebnisse des Updates werden dann in statische Routen konvertiert. Beachten Sie, dass nur bestimmte Routing Protokolle Anforderungen für automatische, statische Routen Aktualisierungen unterstützen.

 

 




