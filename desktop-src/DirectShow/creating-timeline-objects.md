---
description: Erstellen von Zeitachsen Objekten
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Erstellen von Zeitachsen Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344319"
---
# <a name="creating-timeline-objects"></a>Erstellen von Zeitachsen Objekten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Der Beispielcode in diesem Artikel beginnt mit einer leeren Zeitachse, aber die gleichen Schritte gelten auch, wenn Sie ein vorhandenes Projekt laden und diesem Objekte hinzufügen möchten.

Um einen beliebigen Objekttyp in der Zeitachse zu erstellen, rufen Sie die [**iamtimeline::**](iamtimeline-createemptynode.md) -Methode auf. Mit dem folgenden Code wird beispielsweise eine neue Gruppe erstellt:


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



Der zweite Parameter ist ein Member der [**Timeline- \_ \_ Haupttyp**](timeline-major-type.md) -Enumeration. Gibt den Typ des zu erstellenden Zeitachsen Objekts an, z. b. eine Gruppe oder eine Spur.

Die Methode " **kreateemptynode** " erstellt das Objekt und gibt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Objekts zurück. Außerdem erhöht Sie den Verweis Zähler für die **iamtimelineobj** -Schnittstelle, sodass Sie die Schnittstelle freigeben müssen, wenn Sie die Verwendung abgeschlossen haben. Nennen Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion nicht. Verwenden Sie stattdessen immer "antachse **", um** ein Zeitachsen Objekt zu erstellen, da das neue-Objekt für die Verwendung in einer Zeitachse initialisiert wird.

Die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle ist eine generische Schnittstelle. Es stellt Methoden bereit, die allen Typen von Timeline-Objekten gemeinsam sind. Jeder Objekttyp macht auch andere Schnittstellen verfügbar. Beispielsweise machen Gruppen unter anderem die [**iamtimelinegroup**](iamtimelinegroup.md) -Schnittstelle verfügbar. Sie können Zeiger auf die anderen Schnittstellen abrufen, indem Sie **QueryInterface** aufrufen.

Nachdem Sie ein Objekt erstellt haben, ist es noch kein Teil der Zeitachse. Die Methode zum Hinzufügen eines Objekts zur Zeitachse hängt vom Objekttyp ab. Im folgenden Abschnitt wird beschrieben, wie Sie Gruppen, Kompositionen und Spuren zur Zeitachse hinzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 
