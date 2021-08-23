---
description: Abrufen von Sammlungen im COM+-Katalog
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Abrufen von Sammlungen im COM+-Katalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf70f6fe6a7ab25ebed0338e56db1abfc0b869134725d52108b83473b9182d5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812584"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>Abrufen von Sammlungen im COM+-Katalog

Daten im COM+-Katalog werden in einer Hierarchie von Sammlungen gespeichert. Im Verwaltungstool Komponentendienste werden viele dieser Sammlungen als Ordner in der Konsolenstruktur angezeigt. Auf Auflistungen, die nicht als Ordner angezeigt werden, kann nur programmgesteuert zugegriffen werden. Sammlungen dienen als Container für Elemente. Die Elemente in einer bestimmten Auflistung sind alle von einem konsistenten Typ. Das heißt, sie alle stellen die gleiche Art von Element dar, und es kann eine beliebige Anzahl von Elementen in einer Auflistung geben. Die Anwendungssammlung [**enthält**](applications.md) beispielsweise ein Element für jede COM+-Anwendung, die auf dem Computer installiert ist. Diese Sammlung wird im Verwaltungstool als Ordner **COM+-Anwendungen** angezeigt.

Die Auflistungen treten in einer hierarchischen Struktur auf, da die elemente, die sie enthalten, einer innigen Reihenfolge des Einschlusses folgen. Da Komponenten beispielsweise in einer COM+-Anwendung installiert werden, wird die [**Components-Sammlung**](components.md) logisch unter der [**Anwendungssammlung subsumiert.**](applications.md) Um die in dieser bestimmten Anwendung installierten Komponenten  zu enthalten, gibt es für jedes Element in der Anwendungssammlung eine eigene **Components-Sammlung.**

Sie müssen immer dann eine Sammlung für den Katalog abrufen, wenn Sie ein Element abrufen und Eigenschaften für ihn festlegen möchten. Im Allgemeinen müssen Sie mehrere Auflistungen schrittweise durchschritten, um zum element zu kommen, das Sie möchten. Informationen dazu finden Sie unter Navigieren in der [COM+-Sammlungshierarchie.](navigating-the-com--collection-hierarchy.md)

Nachdem Sie eine Sammlung abgerufen haben und direkt mit den elementen arbeiten können, die sie enthält, müssen Sie die Sammlung auffüllen, die Daten für den Inhalt der Sammlung aus dem COM+-Katalog abruft. Weitere Informationen finden Sie unter [Aufpopulieren von COM+-Sammlungen.](populating-com--collections.md)

Darüber hinaus können Sie eine Funktion verwenden, mit der Sie dynamisch abfragen können, um zu sehen, welche zugehörigen Sammlungen aus einer bestimmten Sammlung verfügbar sind, die Sie halten. Weitere Informationen finden Sie unter [Abfragen verfügbarer verwandter Auflistungen.](querying-for-available-related-collections.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Verwaltungsvorgänge innerhalb von Transaktionen](com--administration-operations-within-transactions.md)
</dt> <dt>

[Behandeln von COM+-Verwaltungsfehlern](handling-com--administration-errors.md)
</dt> <dt>

[Einführendes Beispiel mit dem COM+-Verwaltungskatalog](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Übersicht über die COMAdmin-Objekte](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Festlegen von Eigenschaften und Speichern von Änderungen am COM+-Katalog](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



