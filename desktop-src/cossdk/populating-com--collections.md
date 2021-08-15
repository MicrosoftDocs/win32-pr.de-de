---
description: Auffüllen von COM+-Sammlungen
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Auffüllen von COM+-Sammlungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256c246a4f5d176e6b706515d02c0dd5cf68f7ae5a9aff7f89949da14510636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990670"
---
# <a name="populating-com-collections"></a>Auffüllen von COM+-Sammlungen

Nachdem Sie eine Auflistung abgerufen haben und direkt mit den darin enthaltenen Elementen arbeiten können, müssen Sie die Auflistung mithilfe der [**Populate-Methode auffüllen.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) Dadurch werden Daten für den Inhalt der Sammlung aus dem COM+-Katalog abgerufen.

Es ist wichtig zu verstehen, dass Sie bei jeder Verwendung der COMAdmin-Objekte zum Bearbeiten von Elementen oder Daten in Sammlungen tatsächlich an vorübergehend zwischengespeicherten Daten arbeiten. Sie arbeiten nicht direkt mit dem persistenten Katalog. Nichts, was Sie mit einer Sammlung oder einem ihrer Elemente tun, wird im Katalog widergespiegelt, bis Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für die Sammlung aufrufen. Weitere Informationen finden Sie unter [Speichern oder Verwerfen von Änderungen.](saving-or-discarding-changes.md)

Alle nachfolgenden [**Aufrufe von Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)vor dem Aufruf von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)haben zur Folge, dass ausstehende Änderungen an allen Elementen in der Auflistung verworfen werden. **Auffüllen** füllt immer den Cache auf, in dem Sie arbeiten, mit den Daten, die im zugrunde liegenden Katalogdatenspeicher beibehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigieren in der COM+-Sammlungshierarchie](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Abfragen verfügbarer verwandter Sammlungen](querying-for-available-related-collections.md)
</dt> <dt>

[Abrufen von Sammlungen im COM+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



