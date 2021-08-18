---
title: Aktualisieren des Schemacaches
description: Alle Informationen, die auf einen Active Directory-Server geschrieben werden, werden anhand des Schemas überprüft.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Aktualisieren des Schemacache-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff477ce97aab2e0e49522309d386a7e1c37b31e3b8171ef20c626fdaaa5b53a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024528"
---
# <a name="updating-the-schema-cache"></a>Aktualisieren des Schemacaches

Alle Informationen, die auf einen Active Directory-Server geschrieben werden, werden anhand des Schemas überprüft. Das Schema wird aus Leistungsgründen auf Verzeichnisservern (Domänencontrollern) im Arbeitsspeicher gespeichert. Die In-Memory-Version wird automatisch aktualisiert, nachdem die Version auf dem Datenträger aktualisiert wurde. Das automatische Update erfolgt fünf Minuten nach anwendung der letzten Änderung. Durch anwenden einer weiteren Änderung am Schema im 5-Minuten-Fenster wird der Timer für weitere 5 Minuten zurückgesetzt. Dieses Verhalten hält den Cache konsistent, kann aber verwirrend sein, da Änderungen erst nach der Aktualisierung des Caches im Schema angezeigt werden, obwohl sie auf den Datenträger angewendet wurden.

Um den Active Directory-Schemacache nach einem Schemaupdate zu aktualisieren, oder wenn Sie das Schemaupdate sofort für Nichtschemavorgänge verwenden möchten, fügen Sie das **schemaUpdateNow-Attribut** (es ist ein Betriebsattribut) dem Stamm-DSE (leerer DN) mit dem Wert 1 hinzu. Ein Schemacacheupdate wird sofort gestartet. Der Aufruf wird blockiert. Wenn der Aufruf ohne Fehler zurückgegeben wird, wird der Cache aktualisiert, und alle Schemaupdates können verwendet werden. Eine Fehlerrückgabe gibt an, dass das Cacheupdate nicht erfolgreich war. Anwendungen, die dieses Feature verwenden müssen, sollten so konzipiert sein, dass sie den blockierenden Schreibvorgang berücksichtigen, insbesondere wenn sie dem Benutzer Feedback geben, wenn das Programm oder Skript interaktiv ausgeführt wird.

Das folgende Codebeispiel ist ein LDIFDE-Beispielskript, das zeigt, wie ein erneutes Laden eines Caches ausgelöst wird.

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

Weitere Informationen zum programmgesteuerten Aktualisieren des Schemacaches finden Sie unter [Beispielcode zum Aktualisieren des Schemacaches.](example-code-for-updating-the-schema-cache.md)

 

 




