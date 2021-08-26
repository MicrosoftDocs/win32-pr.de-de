---
description: Erstellen von Zeitachsenobjekten
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Erstellen von Zeitachsenobjekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c0a2a88b2cd931e6a9d12274f4a2503b4c97d52348b6ed2629c22bf204f302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054780"
---
# <a name="creating-timeline-objects"></a>Erstellen von Zeitachsenobjekten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Der in diesem Artikel vorgestellte Beispielcode beginnt mit einer leeren Zeitachse, aber die gleichen Schritte gelten, wenn Sie ein vorhandenes Projekt laden und diesem Objekte hinzufügen möchten.

Um einen beliebigen Objekttyp auf der Zeitachse zu erstellen, rufen Sie die [**IAMTimeline::CreateEmptyNode-Methode**](iamtimeline-createemptynode.md) auf. Mit dem folgenden Code wird beispielsweise eine neue Gruppe erstellt:


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



Der zweite Parameter ist ein Member der [**TIMELINE \_ MAJOR \_ TYPE-Enumeration.**](timeline-major-type.md) Sie gibt den Typ des zu erstellenden Zeitachsenobjekts an, z. B. eine Gruppe oder eine Spur.

Die **CreateEmptyNode-Methode** erstellt das -Objekt und gibt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle des Objekts**](iamtimelineobj.md) zurück. Außerdem wird die Verweisanzahl für die **IAMTimelineObj-Schnittstelle** erhöht, sodass Sie die Schnittstelle wieder frei geben müssen, wenn Sie sie nicht mehr verwenden. Rufen Sie die [**CoCreateInstance-Funktion nicht**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf. Verwenden Sie stattdessen immer **CreateEmptyNode,** um ein Zeitachsenobjekt zu erstellen, da es das neue Objekt für die Verwendung in einer Zeitachse initialisiert.

Die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) ist eine generische Schnittstelle. Sie bietet Methoden, die allen Typen von Zeitachsenobjekten gemeinsam sind. Jeder Objekttyp macht auch andere Schnittstellen verfügbar. Gruppen machen z. B. die [**IAMTimelineGroup-Schnittstelle**](iamtimelinegroup.md) verfügbar. Sie können Zeiger auf die anderen Schnittstellen abrufen, indem Sie **QueryInterface aufrufen.**

Nachdem Sie ein Objekt erstellt haben, ist es noch kein Teil der Zeitachse. Die Methode zum Hinzufügen eines Objekts zur Zeitachse hängt vom Objekttyp ab. Im folgenden Abschnitt wird beschrieben, wie Der Zeitachse Gruppen, Kompositionen und Spuren hinzugefügt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 
