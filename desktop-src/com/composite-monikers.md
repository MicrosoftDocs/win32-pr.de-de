---
title: Zusammengesetzte Moniker
description: Eines der nützlichsten Features von Monikern ist, dass Sie Moniker verketten oder zusammen verfassen können.
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5375bb505ff3737fb4e0cdea894790d93c0051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714274"
---
# <a name="composite-monikers"></a>Zusammengesetzte Moniker

Eines der nützlichsten Features von Monikern ist, dass Sie Moniker verketten oder zusammen verfassen können. Ein zusammen *gesetzter Moniker* ist ein Moniker, bei dem es sich um eine Komposition von anderen Monikern handelt und die Beziehung zwischen den Teilen bestimmt werden kann. Auf diese Weise können Sie den vollständigen Pfad zu einem Objekt mit zwei oder mehr Monikern zusammenstellen, die den partiellen Pfaden entsprechen. Sie können Moniker der gleichen Klasse (z. b. zwei dateimoniker) oder verschiedener Klassen (z. b. ein dateimoniker und einen elementmoniker) verfassen. Wenn Sie Ihre eigene Monikerklasse schreiben möchten, können Sie auch Ihre Moniker mit Datei-oder elementmonikern verfassen. Der grundlegende Vorteil einer zusammengesetzten besteht darin, dass Sie einen Teil des Codes zum Implementieren aller möglichen Moniker bietet, bei denen es sich um eine Kombination aus einfacheren Monikern handelt. Dadurch wird die Notwendigkeit spezifischer benutzerdefinierter Monikerklassen erheblich reduziert.

Da Moniker verschiedener Klassen miteinander zusammengesetzt werden können, bieten Moniker die Möglichkeit, mehreren Namespaces beizutreten. Das Dateisystem definiert einen gemeinsamen Namespace für Objekte, die als Dateien gespeichert sind, da alle Anwendungen den Pfadnamen eines Dateisystems verstehen. Ebenso definiert ein Container Objekt auch einen privaten Namespace für die darin enthaltenen Objekte, da kein Container die von einem anderen Container generierten Namen versteht. Moniker erlauben, dass diese Namespaces verknüpft werden, da dateimoniker und elementmoniker zusammengesetzt werden können. Ein monikerclient kann den Namespace nach allen Objekten durchsuchen, die einen einzigen Mechanismus verwenden. Der Client ruft einfach [**IMoniker:: bindjeobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für den Moniker auf, und der monikercode übernimmt den Rest. Ein [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) -Rückruf für eine zusammengesetzte erstellt einen Namen mithilfe der Verkettung aller anzeigen amen der einzelnen Moniker.

Außerdem können Sie mit der monikerkomposition angepasste Erweiterungen zum Namespace für-Objekte hinzufügen, da Sie eine eigene Monikerklasse schreiben können.

Manchmal können zwei Moniker bestimmter Klassen auf besondere Weise kombiniert werden. Ein dateimoniker, der einen unvollständigen Pfad darstellt, und ein anderer dateimoniker, der einen relativen Pfad darstellt, können kombiniert werden, um einen einzelnen dateimoniker zu bilden, der den vollständigen Pfad Beispielsweise könnten die dateimoniker "c: \\ work \\ Art" mit dem relativen dateimoniker ". \\ " zusammengesetzt werden. Backup \\myfile.doc "to equal" c: \\ work \\ Backup \\myfile.doc ". Dies ist ein Beispiel für eine *nicht generische Komposition*.

Die *generische Komposition* hingegen lässt die Verbindung zweier Moniker zu, unabhängig von der Art der Klassen. Sie könnten z. b. einen elementmoniker in einem dateimoniker verfassen, dies ist natürlich nicht anders.

Da eine nicht generische Komposition von der Klasse der beteiligten Moniker abhängt, werden die Details durch die Implementierung einer bestimmten Monikerklasse definiert. Sie können neue Typen von nicht generischen Kompositionen definieren, wenn Sie eine neue Monikerklasse schreiben. Im Gegensatz dazu werden generische Kompositionen von OLE definiert. Moniker, die als Ergebnis der generischen Komposition erstellt werden, werden als generische zusammengesetzte Moniker bezeichnet.

Diese drei Klassen, dateimoniker, elementmoniker und generische zusammengesetzte Moniker arbeiten zusammen, und Sie sind die am häufigsten verwendeten Klassen von Monikern.

Monikerclients sollten [**IMoniker:: compoabwith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) aufrufen, um eine zusammengesetzte für den Moniker mit einem anderen zu erstellen. Der Moniker, für den er aufgerufen wird, entscheidet intern, ob er eine generische oder nicht generische Komposition ausführen kann. Wenn die monikerimplementierung feststellt, dass eine generische Komposition verwendbar ist, stellt OLE [**die Funktion "**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) die Funktion", um dies zu vereinfachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anti-Moniker](anti-monikers.md)
</dt> <dt>

[Klassenmoniker](class-monikers.md)
</dt> <dt>

[Dateimoniker](file-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> <dt>

[Zeigermoniker](pointer-monikers.md)
</dt> </dl>

 

 




