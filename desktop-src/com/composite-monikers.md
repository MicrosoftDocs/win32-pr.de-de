---
title: Zusammengesetzte Moniker
description: Eines der nützlichsten Features von Monikern ist, dass Sie Moniker miteinander verketten oder zusammenstellen können.
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad815cdb89dda7f58fe1507d43a07a14d24875309668297e20ec51114dd65d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737026"
---
# <a name="composite-monikers"></a>Zusammengesetzte Moniker

Eines der nützlichsten Features von Monikern ist, dass Sie Moniker miteinander verketten oder zusammenstellen können. Ein *zusammengesetzter Moniker* ist ein Moniker, der eine Zusammensetzung anderer Moniker ist und die Beziehung zwischen den Teilen bestimmen kann. Auf diese Weise können Sie den vollständigen Pfad zu einem Objekt zusammenstellen, wenn zwei oder mehr Moniker angegeben werden, die partiellen Pfaden entsprechen. Sie können Moniker derselben Klasse (z. B. zwei Dateimoniker) oder aus verschiedenen Klassen (z. B. einem Dateimoniker und einem Elementmoniker) zusammenstellen. Wenn Sie Ihre eigene Monikerklasse schreiben würden, könnten Sie ihre Moniker auch mit Datei- oder Elementmonikern zusammenstellen. Der grundlegende Vorteil eines zusammengesetzten -Codes ist, dass er Ihnen einen Codeteil bietet, um jeden möglichen Moniker zu implementieren, bei dem es sich um eine Kombination einfacher Moniker handelt. Dies reduziert die Notwendigkeit bestimmter benutzerdefinierter Monikerklassen erheblich.

Da Moniker verschiedener Klassen miteinander zusammengesetzt werden können, bieten Moniker die Möglichkeit, mehrere Namespaces zu verbinden. Das Dateisystem definiert einen allgemeinen Namespace für Objekte, die als Dateien gespeichert sind, da alle Anwendungen einen Dateisystempfadnamen verstehen. Ebenso definiert ein Containerobjekt auch einen privaten Namespace für die objekte, die es enthält, da kein Container die von einem anderen Container generierten Namen versteht. Moniker ermöglichen das Hinzufügen dieser Namespaces, da Dateimoniker und Elementmoniker zusammengesetzt werden können. Ein Monikerclient kann den Namespace mit einem einzigen Mechanismus nach allen Objekten durchsuchen. Der Client ruft einfach [**IMoniker::BindToObject für**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) den Moniker auf, und der Monikercode verarbeitet den Rest. Ein Aufruf von [**IMoniker::GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) für einen zusammengesetzten erstellt einen Namen unter Verwendung der Verkettung aller Anzeigenamen der einzelnen Moniker.

Da Sie außerdem Eine eigene Monikerklasse schreiben können, können Sie mit der Monikerkomposition benutzerdefinierte Erweiterungen zum Namespace für -Objekte hinzufügen.

Manchmal können zwei Moniker bestimmter Klassen auf besondere Weise kombiniert werden. Beispielsweise kann ein Dateimoniker, der einen unvollständigen Pfad darstellt, und ein anderer Dateimoniker, der einen relativen Pfad darstellt, kombiniert werden, um einen einzelnen Dateimoniker zu bilden, der den vollständigen Pfad darstellt. Beispielsweise könnten die Dateimoniker "c: work art" mit dem \\ \\ relativen Dateimoniker "." zusammengesetzt werden. \\ backup \\myfile.doc" auf "c: \\ \\ Arbeitssicherungs-myfile.doc". \\ Dies ist ein Beispiel für *eine nicht allgemeine Komposition.*

*Die generische Komposition* hingegen ermöglicht die Verbindung von zwei beliebigen Monikern, unabhängig davon, welche Klassen sie haben. Beispielsweise könnten Sie einen Elementmoniker in einem Dateimoniker zusammenstellen, obwohl dies natürlich nicht umgekehrt der Reihe nach ist.

Da eine nichtgenerische Komposition von der Klasse der beteiligten Moniker abhängt, werden ihre Details durch die Implementierung einer bestimmten Monikerklasse definiert. Sie können neue Typen nichtgenerischer Kompositionen definieren, wenn Sie eine neue Monikerklasse schreiben. Im Gegensatz dazu werden generische Kompositionen durch OLE definiert. Moniker, die als Ergebnis der generischen Komposition erstellt werden, werden als generische zusammengesetzte Moniker bezeichnet.

Diese drei Klassen, Dateimoniker, Elementmoniker und generische zusammengesetzte Moniker arbeiten zusammen und sind die am häufigsten verwendeten Klassen von Monikern.

Monikerclients sollten [**IMoniker::ComposeWith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) aufrufen, um einen zusammengesetzten für Moniker mit einem anderen zu erstellen. Der Moniker, für den er aufgerufen wird, entscheidet intern, ob er eine generische oder nicht generische Komposition verwenden kann. Wenn die Monikerimplementierung feststellt, dass eine generische Komposition verwendet werden kann, stellt OLE die [**CreateGenericComposite-Funktion**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) zur Verfügung, um dies zu vereinfachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Antimoniker](anti-monikers.md)
</dt> <dt>

[Klassenmoniker](class-monikers.md)
</dt> <dt>

[Dateimoniker](file-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> <dt>

[Zeigermoniker](pointer-monikers.md)
</dt> </dl>

 

 




