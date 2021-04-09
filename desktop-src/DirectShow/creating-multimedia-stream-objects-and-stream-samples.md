---
description: Erstellen von multimediastreamobjekten und streamingbeispielen
ms.assetid: 1aecdd39-f1b3-490b-b092-86d51439be02
title: Erstellen von multimediastreamobjekten und streamingbeispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cdc30129591bf1c67609ad6d15e8fd8286ae23
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961166"
---
# <a name="creating-multimedia-stream-objects-and-stream-samples"></a>Erstellen von multimediastreamobjekten und streamingbeispielen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 

Objekte, die die [**imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) -Schnittstelle unterstützen, sind die grundlegenden Container für Multimedia-Datenströme. Die **imultimediastream** -Schnittstelle enthält Methoden, mit denen die Datenströme des Objekts aufgelistet werden. Dabei handelt es sich in der Regel um Video-und Audiodaten, die jedoch Daten beliebiger Formate enthalten können, z. b. Untertitel, nur-Text oder SMPTE-Timecode. Die **imultimediastream** -Schnittstelle ist jedoch ein generischer Container. Entwickler können andere Versionen der-Schnittstelle erstellen, die bestimmte Datenformate unterstützen. Objekte, die die [**iammultimediastream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) -Schnittstelle implementieren, können z. b. Datenströme eines beliebigen DirectShow-Datenformats aufzählen und steuern. Da einzelne Datenströme Format spezifisch sind, unterstützen Sie mindestens zwei unterschiedliche Schnittstellen: einen generischen und einen Daten spezifischen. Jeder Stream unterstützt die [**imediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) -Schnittstelle, die Methoden zum Abrufen des Formats und einen Zeiger auf den Stream selbst bereitstellt. Die [**idirectdrawmediastream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) -Schnittstelle hingegen verfügt über Methoden, die speziell das Rendern von Videodaten behandeln. Jede von **imultimediastream** abgeleitete Schnittstelle unterstützt auch das Erstellen von streambeispielen, die grundlegenden Einheiten der Streamingdaten.

Ein multimediaresample ist ein Verweis auf ein Objekt, das die Mediendaten enthält. Bei einem Video Bild handelt es sich hierbei um eine DirectDraw-Oberfläche. Der genaue Inhalt des Beispiels variiert abhängig vom Medientyp (Sound, Text usw.). Da ein Beispiel nur ein Verweis auf das Datenobjekt ist, kann eine beliebige Anzahl von streambeispielen auf das gleiche Objekt verweisen. Die [**istreamsample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) -Schnittstelle stellt Methoden bereit, mit denen die Merkmale eines Beispiels, wie z. b. Start-und Endzeit, Status und Datenstrom Zuordnung, angezeigt und festgelegt werden. Mit der [**istreamsample:: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) -Methode werden die Beispiel Daten im Fall lesbarer Streams aktualisiert. Bei beschreibbaren Streams werden die Beispiel Daten in den Stream geschrieben. In der Regel verwenden Sie die **Update** -Methode in einer Schleife, mit der Streamingdaten gerendert, übertragen oder gespeichert werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur multimediastreamingarchitektur](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



