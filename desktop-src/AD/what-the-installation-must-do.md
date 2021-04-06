---
title: Was die Installation tun muss
description: Auf neue Attribute, auf die in Schritt 3 verwiesen wird, muss von ihrer OID verwiesen werden, da der neue Attribut Name an dieser Stelle nicht im Schema Cache vorhanden ist.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Was die Installation tun muss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947371"
---
# <a name="what-the-installation-must-do"></a>Was die Installation tun muss

Anwendungen, die das Schema erweitern, müssen Updates anwenden, wie im folgenden Verfahren beschrieben.

**So wenden Sie beim Erweitern des Schemas Updates an**

1.  Fügen Sie die neuen Attribute hinzu.
2.  Fügen Sie die neuen Klassen hinzu.
3.  Fügen Sie die neuen Attribute zu Klassen hinzu.
4.  Löst einen Cache erneuten Ladevorgang aus.

Auf neue Attribute, auf die in Schritt 3 verwiesen wird, muss von ihrer OID verwiesen werden, da der neue Attribut Name an dieser Stelle nicht im Schema Cache vorhanden ist.

Schritt 4 ist nicht erforderlich, wenn die Erweiterungen nicht sofort verwendet werden. die Erweiterungen werden je nach System Auslastung in ungefähr 5 Minuten im Schema Cache angezeigt. Weitere Informationen zum Schema Cache und zum erneuten Laden des Caches finden Sie unter [Aktualisieren des Schema Caches](updating-the-schema-cache.md).

 

 




