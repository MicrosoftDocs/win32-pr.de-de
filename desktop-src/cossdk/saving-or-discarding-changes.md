---
description: Speichern oder Verwerfen von Änderungen
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Speichern oder Verwerfen von Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860848"
---
# <a name="saving-or-discarding-changes"></a>Speichern oder Verwerfen von Änderungen

Wenn Sie Eigenschaften für ein Element festlegen, werden keine Änderungen tatsächlich im com+-Katalog aufgezeichnet, bis Sie die Änderungen explizit speichern. Verwenden Sie hierzu die [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt für die Auflistung, die das Element enthält.

Wenn Sie Änderungen verwerfen möchten, für die noch kein Commit ausgeführt wurde, können Sie die [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt aufzurufen. Dadurch werden alle persistenten Daten aus dem com+-Katalog für alle Elemente in der Auflistung gelesen, wodurch alle ausstehenden Änderungen gelöscht werden.

Wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)verwenden, führen alle Inkonsistenzen in den von Ihnen ausgewählten Eigenschafts Einstellungen zu einem Fehler, und **SaveChanges** kann das Objekt, das den Fehler zurückgegeben hat, nicht schreiben. Alle Eigenschaften für ein bestimmtes Element werden entweder geschrieben oder können nicht als Ganzes geschrieben werden.

Wenn jedoch Schreibfehler auftreten, sind Sie möglicherweise nicht auf inkompatible Einstellungen zurückzuführen. Möglicherweise ist ein anderer Fehler aufgetreten. Sie müssen die Details des Fehlers überprüfen, um sicher zu sein. Weitere Informationen finden Sie unter [Behandeln von com+-Verwaltungsfehlern](handling-com--administration-errors.md) und [Abhängigkeiten zwischen Eigenschaften](interdependencies-between-properties.md).

Als allgemeine Regel gilt: je mehr Änderungen Sie versuchen, gleichzeitig zu speichern, insbesondere Änderungen an mehreren Objekten, desto wahrscheinlicher ist es, dass Sie eine Fehlermeldung erhalten, und desto schwieriger ist es, eine Nachverfolgung durchführen zu müssen.

Außerdem verfügen Sie zwischen Aufrufen [**von "auffüllen" und "**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)" nicht über eine Sperre für die Elemente in der Sammlung. Konflikte sind möglich. Weitere Informationen finden Sie unter " [erhalten und Festlegen von Eigenschaften](getting-and-setting-properties.md)".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften werden erhalten und festgelegt](getting-and-setting-properties.md)
</dt> <dt>

[Abhängigkeiten zwischen Eigenschaften](interdependencies-between-properties.md)
</dt> <dt>

[Abfragen von verfügbaren Eigenschaften](querying-for-available-properties.md)
</dt> </dl>

 

 



