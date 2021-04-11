---
description: Com+-Sammlungen werden aufgefüllt.
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Com+-Sammlungen werden aufgefüllt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342249"
---
# <a name="populating-com-collections"></a>Com+-Sammlungen werden aufgefüllt.

Nachdem Sie eine Sammlung abgerufen haben und bevor Sie direkt mit den darin enthaltenen Elementen arbeiten können, müssen Sie die Auflistung mit der Auffüllen [**-Methode auffüllen**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) . Dadurch werden Daten für den Inhalt der Sammlung aus dem com+-Katalog abgerufen.

Es ist wichtig zu verstehen, dass Sie immer, wenn Sie die COMAdmin-Objekte zum Bearbeiten von Elementen oder Daten in Auflistungen verwenden, tatsächlich an transitiv zwischengespeicherten Daten arbeiten. Sie arbeiten nicht direkt mit dem beibehaltenen Katalog. Nichts, was Sie mit einer Auflistung oder einem ihrer Elemente tun, wird im Katalog widergespiegelt, bis Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für die Auflistung aufgerufen haben. Weitere Details finden Sie unter [Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md).

Alle nachfolgenden Aufrufe [**zum Auffüllen**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)vor dem Aufruf von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)haben den Effekt, ausstehende Änderungen an allen Elementen in der Auflistung zu verwerfen. Auffüllen **füllt immer den** Cache, in dem Sie arbeiten, mit den Daten, die im zugrunde liegenden Katalogdaten Speicher beibehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Navigieren in der com+-Sammlungs Hierarchie](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Abfragen von verfügbaren verwandten Sammlungen](querying-for-available-related-collections.md)
</dt> <dt>

[Abrufen von Auflistungen im com+-Katalog](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



