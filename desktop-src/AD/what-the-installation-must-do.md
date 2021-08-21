---
title: Was muss die Installation tun?
description: Auf neue Attribute, auf die in Schritt 3 verwiesen wird, muss seine OID verweisen, da der neue Attributname zu diesem Zeitpunkt nicht im Schemacache vorhanden ist.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Was muss die Installation von AD tun?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3dcf125a171fba921a5341ad5f3de8bbe5d791d4eb4dc072f551345df3218ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182173"
---
# <a name="what-the-installation-must-do"></a>Was muss die Installation tun?

Anwendungen, die das Schema erweitern, müssen Updates wie im folgenden Verfahren beschrieben anwenden.

**So wenden Sie Updates beim Erweitern des Schemas an**

1.  Fügen Sie die neuen Attribute hinzu.
2.  Fügen Sie die neuen Klassen hinzu.
3.  Fügen Sie klassen die neuen Attribute hinzu.
4.  Lösen Sie ein erneutes Laden des Caches aus.

Auf neue Attribute, auf die in Schritt 3 verwiesen wird, muss seine OID verweisen, da der neue Attributname zu diesem Zeitpunkt nicht im Schemacache vorhanden ist.

Schritt 4 ist nicht erforderlich, wenn die Erweiterungen nicht sofort verwendet werden. Die Erweiterungen werden je nach Systemauslastung in ca. 5 Minuten im Schemacache angezeigt. Weitere Informationen zum Schemacache und zum Auslösen eines erneuten Ladens des Caches finden Sie unter [Aktualisieren des Schemacaches.](updating-the-schema-cache.md)

 

 




