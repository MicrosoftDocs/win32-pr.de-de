---
description: Speichern oder Verwerfen von Änderungen
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Speichern oder Verwerfen von Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01c000a6fc9fbe7e8e25e50c041f1b5a0e1250dfe089245ef035213905e5737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915931"
---
# <a name="saving-or-discarding-changes"></a>Speichern oder Verwerfen von Änderungen

Wenn Sie Eigenschaften für ein Element festlegen, werden keine Änderungen am COM+-Katalog aufgezeichnet, bis Sie änderungen explizit speichern. Verwenden Sie hierzu die [**SaveChanges-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für das [**COMAdminCatalogCollection-Objekt**](comadmincatalogcollection.md) für die Auflistung, die das Element enthält.

Wenn Sie Änderungen verwerfen möchten, für die noch kein Committed vorgenommen wurde, können Sie die [**Populate-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) für das [**COMAdminCatalogCollection-Objekt**](comadmincatalogcollection.md) aufrufen. Dadurch werden alle persistenten Daten aus dem COM+-Katalog für alle Elemente in der Sammlung eingelesen, und alle ausstehenden Änderungen werden effektiv gelöscht.

Wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)verwenden, führen alle inkonsistenten Eigenschafteneinstellungen, die Sie ausgewählt haben, zu einem Fehler, und **SaveChanges** kann das Objekt, das den Fehler zurückgegeben hat, nicht schreiben. Alle Eigenschaften für ein bestimmtes Element werden entweder geschrieben oder können nicht als Ganzes geschrieben werden.

Wenn jedoch Schreibfehler auftreten, sind sie möglicherweise nicht auf inkompatible Einstellungen zurückver führen. Ein anderer Fehler ist möglicherweise aufgetreten. Sie müssen die Details des Fehlers überprüfen, um sicher zu sein. Weitere Informationen finden Sie unter [Behandeln von COM+-Verwaltungsfehlern](handling-com--administration-errors.md) und [Abhängigkeiten zwischen Eigenschaften.](interdependencies-between-properties.md)

Im Allgemeinen gilt: Wenn Sie versuchen, Änderungen gleichzeitig zu speichern, insbesondere Änderungen an mehreren Objekten, desto wahrscheinlicher ist es, dass Sie einen Fehler erhalten und desto schwieriger ist es, sie zu finden.

Darüber hinaus verfügen Sie zwischen [**Aufrufen von Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) und [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)nicht über eine Sperre für die Elemente in der Auflistung. Ein -Inhalt ist möglich. Weitere Informationen finden Sie unter [Getting and Setting Properties (Abrufen und Festlegen von Eigenschaften).](getting-and-setting-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abrufen und Festlegen von Eigenschaften](getting-and-setting-properties.md)
</dt> <dt>

[Abhängigkeiten zwischen Eigenschaften](interdependencies-between-properties.md)
</dt> <dt>

[Abfragen verfügbarer Eigenschaften](querying-for-available-properties.md)
</dt> </dl>

 

 



