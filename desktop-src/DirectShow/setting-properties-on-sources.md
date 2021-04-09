---
description: Festlegen von Eigenschaften für Quellen
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: Festlegen von Eigenschaften für Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de58e25cc9fdec34ed285ebbfc2e9cfd3dcdf95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859944"
---
# <a name="setting-properties-on-sources"></a>Festlegen von Eigenschaften für Quellen

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Wenn Sie ein neues Quell Objekt erstellen, müssen Sie einige Eigenschaften festlegen und andere optional festlegen. Sie müssen die folgenden Eigenschaften festlegen.

-   Die Start-und Endzeit Zeiten in Relation zum Rest der Zeitachse. Aufrufen der [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md) -Methode. Legen Sie keine Überlappungs Zeiten für Quell Objekte innerhalb desselben Titels fest, oder es wird ein nicht definiertes Verhalten verursacht.
-   Die Mediendatei, die als Quellclip verwendet werden soll. Nennen Sie [**iamtimelinesrc:: setmedianame**](iamtimelinesrc-setmedianame.md).
-   Die Start-und Endzeit der Medien, relativ zur ursprünglichen Quelldatei. Aufrufen der [**iamtimelinesrc:: setmediatimes**](iamtimelinesrc-setmediatimes.md) -Methode. Ausnahme: Wenn es sich bei der Quelle um ein Image handelt, geben Sie die Medien Zeiten nicht an. Weitere Informationen zu Medien Zeiten finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).

Ein Quell Objekt erbt seinen Medientyp von der übergeordneten Gruppe. Daher ist es nicht erforderlich, einen Medientyp anzugeben.

Zu den optionalen Eigenschaften zählen folgende:

-   Der streckungs Modus. Der streckungs Modus gibt an, wie Microsoft® DirectShow® Bearbeitungs Dienste (des) eine Quelle rendert, deren Größe nicht den Ausgabe Dimensionen entspricht. Standardmäßig wird von des ein Bild gestreckt, ohne das Seitenverhältnis beizubehalten. Alternativ kann des ein Bild zuschneiden oder ein Buchstaben Feld erstellen. Aufrufen der [**iamtimelinesrc:: setstretchmode**](iamtimelinesrc-setstretchmode.md) -Methode, um den streckungs Modus anzugeben.
-   Die Dauer der Quelldatei. Wenn Sie diese Eigenschaft vor dem Festlegen der Medien Zeiten festlegen, überprüft der die Endzeit des Mediums und verkürzt die Endzeit, wenn diese die Datei Dauer überschreitet. Dadurch können später Renderingfehler vermieden werden. Sie können die Dauer der Datei mithilfe des Medien Detektors abrufen, wie unter [Verwenden des Medien Detektors](using-the-media-detector.md)beschrieben. Aufrufen der [**iamtimelinesrc:: setmedialength**](iamtimelinesrc-setmedialength.md) -Methode, um die Datei Dauer anzugeben.
-   Die streamnummer. Standardmäßig verwendet ein Quell Objekt den ersten Stream in der Datei, der mit dem Medientyp der übergeordneten Gruppe übereinstimmt. Wenn eine Datei zwei oder mehr Streams desselben Medientyps enthält, wählen Sie den zu verwendenden Stream aus, indem Sie [**iamtimelinesrc:: setstreamnumber**](iamtimelinesrc-setstreamnumber.md)aufrufen. Sie können das Medien Erkennungs Modul verwenden, um die Anzahl der Streams zu ermitteln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



