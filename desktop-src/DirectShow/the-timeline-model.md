---
description: Das Zeitachsen Modell
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Das Zeitachsen Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560360"
---
# <a name="the-timeline-model"></a>Das Zeitachsen Modell

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Eine *Zeitachse* ist ein Objekt, das von [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) verwendet wird, um ein Video Bearbeitungs Projekt darzustellen. Ein Bearbeitungs Projekt wird als Auflistung von Quell Clips gestartet, die aus Videodateien, Audiodateien oder noch Bilddateien entnommen werden. Eine lineare Sequenz von Clips bildet eine *Spur*. In DirectShow-Bearbeitungs Diensten werden Audiodateien und Videos in separaten Spuren abgelegt.

Spuren können auch geschichtet werden. Mehrere Audiospuren werden miteinander gemischt und können Audioeffekte enthalten, wie z. b. "Fades" oder "Reverb". Zum Erstellen von Übergängen werden mehrere Videospuren verwendet. Beispielsweise können Sie eine Löschung von einem Clip zu einem anderen erstellen. Ein weiteres Beispiel ist ein Chroma-Schlüssel, in dem der Hintergrund eines Clips abgeblendet und durch eine andere Spur ersetzt wird. (Das Wettervorhersage vor einem Satelite-Image ist ein Beispiel für die Chroma-Schlüssel Erstellung.)

DES verwendet eine Baumstruktur zur Darstellung einer Bearbeitung:

-   Audiodateien und Videoclips bilden die Blattknoten oder *Quell* Objekte.
-   Eine Auflistung von Quellen mit einem einheitlichen Medientyp (Audiodatei oder Video) ist eine *Spur*.
-   Eine Auflistung von Spuren ist eine *Komposition*. Eine Komposition wird als zusammengesetzte aller darin enthaltenen Spuren gerendert. Kompositionen können andere Kompositionen enthalten, die komplexe Anordnungen von Spuren ermöglichen.
-   Eine Auflistung von Kompositionen und Nachverfolgen der obersten Ebene (alle, die denselben Medientyp darstellen) ist eine *Gruppe*.
-   Ein Satz von einer oder mehreren Gruppen bildet eine *Zeitachse*. Die Zeitachse ist der Stamm Knoten in der Struktur.

Eine Zeitachse muss mindestens eine Gruppe enthalten. Jede Gruppe stellt einen einzelnen Datenstrom in der endgültigen Produktion dar. Ein typisches Projekt umfasst eine Videogruppe und eine Audiogruppe. Die Komposition ist optional. Sie sind vorhanden, um bei Bedarf mehr Struktur bereitzustellen.

Die folgende Abbildung zeigt die Beziehungen zwischen untergeordneten und übergeordneten Elementen, die eine Zeitachse bilden:

![Knoten Struktur](images/timeline1.png)

Das folgende Beispiel zeigt eine Zeitachse als Temporale Sequenz:

![Zeitachsen Abbildung](images/timeline2.png)

Der Pfeil oben stellt die Richtung der Zeitachse dar, beginnend ab der Zeit NULL. In der Videogruppe hat Track 1 eine höhere Priorität als Track 0. Die Quell Objekte in Track 1 verschleiern diese in der Nachverfolgung 0. Wenn Track 1 leer ist, wird Nachverfolgung 0 angezeigt. Wie bereits erwähnt, werden Audiospuren einfach gemischt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in DirectShow-Bearbeitungs Dienste](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 



