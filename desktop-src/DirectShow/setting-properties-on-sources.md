---
description: Festlegen von Eigenschaften für Quellen
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: Festlegen von Eigenschaften für Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06908f4f15a6d1107ce15e71679c92ec8065725ed883a6561df5cd21af3e13c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965020"
---
# <a name="setting-properties-on-sources"></a>Festlegen von Eigenschaften für Quellen

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Wenn Sie ein neues Quellobjekt erstellen, gibt es einige Eigenschaften, die Sie festlegen müssen, und andere, die Sie optional festlegen können. Sie müssen die folgenden Eigenschaften festlegen.

-   Die Start- und Beendigungszeiten relativ zum Rest der Zeitachse. Rufen Sie die [**IAMTimelineObj::SetStartStop-Methode**](iamtimelineobj-setstartstop.md) auf. Legen Sie keine Überlappungszeiten für Quellobjekte innerhalb derselben Spur fest, da dies zu nicht definiertem Verhalten führt.
-   Die Mediendatei, die als Quellclip verwendet werden soll. Rufen Sie [**IAMTimelineSrc::SetMediaName auf.**](iamtimelinesrc-setmedianame.md)
-   Die Start- und Beendigungszeiten des Mediums relativ zur ursprünglichen Quelldatei. Rufen Sie die [**IAMTimelineSrc::SetMediaTimes-Methode**](iamtimelinesrc-setmediatimes.md) auf. Ausnahme: Wenn es sich bei der Quelle um ein Standbild handelt, geben Sie die Medienzeiten nicht an. Weitere Informationen zu Medienzeiten finden Sie unter [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Ein Quellobjekt erbt seinen Medientyp von der übergeordneten Gruppe, sodass es nicht erforderlich ist, einen Medientyp anzugeben.

Optionale Eigenschaften umfassen Folgendes:

-   Der Stretchmodus. Der Stretchingmodus gibt an, wie Microsoft® DirectShow® Editing Services (DES) eine Quelle rendert, deren Größe nicht mit den Ausgabedimensionen übereinstimmt. Standardmäßig streckt DES ein Bild, ohne das Seitenverhältnis zu erhalten. Alternativ kann DES ein Bild zuschneiden oder ein Letterbox erstellen. Rufen Sie die [**IAMTimelineSrc::SetStretchMode-Methode**](iamtimelinesrc-setstretchmode.md) auf, um den Stretchmodus anzugeben.
-   Die Dauer der Quelldatei. Wenn Sie diese Eigenschaft festlegen, bevor Sie die Medienzeiten festlegen, überprüft DES die Beendigungszeit des Mediums und schneidet die Beendigungszeit ab, wenn sie die Dateidauer überschreitet. Dadurch können Später Renderingfehler vermieden werden. Sie können die Dauer der Datei mithilfe der Medienerkennung abrufen, wie unter [Verwenden der Medienerkennung](using-the-media-detector.md)beschrieben. Rufen Sie die [**IAMTimelineSrc::SetMediaLength-Methode**](iamtimelinesrc-setmedialength.md) auf, um die Dateidauer anzugeben.
-   Die Streamnummer. Standardmäßig verwendet ein Quellobjekt den ersten Stream in der Datei, der dem Medientyp der übergeordneten Gruppe entspricht. Wenn eine Datei zwei oder mehr Streams desselben Medientyps enthält, wählen Sie den zu verwendenden Datenstrom aus, indem [**Sie IAMTimelineSrc::SetStreamNumber**](iamtimelinesrc-setstreamnumber.md)aufrufen. Sie können die Medienerkennung verwenden, um die Anzahl der Streams zu ermitteln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Quellen](working-with-sources.md)
</dt> </dl>

 

 



