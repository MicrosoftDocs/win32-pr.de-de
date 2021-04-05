---
title: Aktualisieren des Schema Caches
description: Alle Informationen, die auf einen Active Directory Server geschrieben werden, werden anhand des Schemas überprüft.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Aktualisieren des Schema Cache-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707517"
---
# <a name="updating-the-schema-cache"></a>Aktualisieren des Schema Caches

Alle Informationen, die auf einen Active Directory Server geschrieben werden, werden anhand des Schemas überprüft. Das Schema wird aus Leistungsgründen im Arbeitsspeicher auf Verzeichnisservern (Domänen Controllern) gespeichert. Die in-Memory-Version wird automatisch aktualisiert, nachdem die auf dem Datenträger aktualisierte Version aktualisiert wurde. Das automatische Update erfolgt fünf Minuten nach dem Anwenden der letzten Änderung. Wenn Sie im 5-Minuten-Fenster eine weitere Änderung am Schema anwenden, wird der Timer für weitere fünf Minuten zurückgesetzt. Dieses Verhalten sorgt für einen konsistenten Cache, kann jedoch verwirrend sein, da Änderungen nicht im Schema angezeigt werden, bis der Cache aktualisiert wird, auch wenn Sie auf den Datenträger angewendet wurden.

Um den Active Directory Schema Cache nach einer Schema Aktualisierung zu aktualisieren, oder wenn Sie die Schema Aktualisierung für nicht-Schema-Vorgänge sofort verwenden möchten, fügen Sie das Attribut **schemaUpdateNow** (es ist ein Betriebs Attribut) dem Stamm-DSE (leeres DN) mit dem Wert 1 hinzu. Ein Schema Cache Update wird sofort gestartet. Der-Befehl blockiert. Wenn der-Rückruf ohne Fehler zurückgegeben wird, wird der Cache aktualisiert, und alle Schema Aktualisierungen sind zur Verwendung bereit. Ein Fehler gibt an, dass das Cache Update nicht erfolgreich war. Anwendungen, die dieses Feature verwenden müssen, sollten für den blockierenden Schreibvorgang konzipiert werden, insbesondere bei der Bereitstellung des Benutzer Feedbacks, wenn das Programm oder Skript interaktiv ausgeführt wird.

Das folgende Codebeispiel zeigt ein LDIFDE-Beispielskript, das zeigt, wie ein erneutes Laden des Caches auslöst.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Weitere Informationen zum programmgesteuerten Aktualisieren des Schema Caches finden Sie unter [Beispiel Code zum Aktualisieren des Schema Caches](example-code-for-updating-the-schema-cache.md).

 

 




