---
title: Statische und autostatic Routen
description: In der Regel werden Routen zu Remotenetzwerken dynamisch über Routingprotokolle abgerufen.
ms.assetid: af2f2039-8131-4ca9-98bf-6aeb7a511034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0206190c86c75e4e50ce390cf3f084db956671de6efebe21022151879362ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127830"
---
# <a name="static-and-autostatic-routes"></a>Statische und autostatic Routen

In der Regel werden Routen zu Remotenetzwerken dynamisch über Routingprotokolle abgerufen. Der Administrator kann jedoch auch *ein Seeding* für die Routingtabelle ausführen, indem er Routen manuell bereitstellt. Diese Routen werden als *statische* bezeichnet. Eine statische Route ist einer Schnittstelle zugeordnet, die das Remotenetzwerk darstellt. Im Gegensatz zu dynamischen Routen werden statische Routen auch dann beibehalten, wenn der Router neu gestartet oder die Schnittstelle deaktiviert ist.

Eine *autostatic* Route wird über ein Routingprotokoll abgerufen, verhält sich jedoch wie eine statische Route. Der Prozess zum Abrufen automatisch statischer Routen sieht wie folgt aus: Der IP- oder IPX-Router-Manager gibt eine Anforderung aus, dass ein Routingprotokoll die Routinginformationen für eine bestimmte Schnittstelle aktualisiert. Die Ergebnisse des Updates werden dann in statische Routen konvertiert. Beachten Sie, dass nur bestimmte Routingprotokolle Anforderungen für automatisch statische Routenupdates unterstützen.

 

 




