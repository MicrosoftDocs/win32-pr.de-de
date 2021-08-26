---
description: Das Zeitachsenmodell
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Das Zeitachsenmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e5eeb60dce31fa466a518476bb3da341a3d2fda4fdeaa47ca58a89a904dded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903810"
---
# <a name="the-timeline-model"></a>Das Zeitachsenmodell

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Eine *Zeitachse* ist ein Objekt, das [directShow Editing Services](directshow-editing-services.md) (DES) verwendet, um ein Videobearbeitungsprojekt darzustellen. Ein Bearbeitungsprojekt wird als Sammlung von Quellclips gestartet, die aus Videodateien, Sounddateien oder Stillbilddateien stammen. Eine lineare Sequenz von Clips bildet eine *Spur*. In DirectShow Editing Services (DES) werden Audio und Video auf separaten Spuren platziert.

Spuren können auch überlagerungsgeschichtet werden. Mehrere Audiospuren werden kombiniert und können Audioeffekte wie Einblendungen oder Hall enthalten. Mehrere Videospuren werden verwendet, um Übergänge zu erstellen. Sie können z. B. ein Zurücksetzen von einem Clip zu einem anderen erstellen. Ein weiteres Beispiel ist ein Schlüssel, bei dem der Hintergrund eines Clips aus- und durch eine andere Spur ersetzt wird. (Der Wettervorhersager vor einem Satelite-Bild ist ein Beispiel für die Schlüsselschlüsselung von Farben.)

DES verwendet eine Struktur, um eine Bearbeitung darzustellen:

-   Audio- und Videoclips bilden die Blattknoten oder *Quellobjekte.*
-   Eine Sammlung von Quellen mit einem einheitlichen Medientyp (Audio oder Video) ist eine *Spur.*
-   Eine Auflistung von Spuren ist eine *Komposition.* Eine Komposition wird als Zusammengesetzte aller darin enthaltenen Spuren gerendert. Kompositionen können andere Kompositionen enthalten, die komplexe Anordnungen von Spuren ermöglichen.
-   Eine Sammlung von Kompositionen und Spuren auf oberster Ebene (die alle den gleichen Medientyp darstellen) ist eine *Gruppe*.
-   Ein Satz von einer oder mehreren Gruppen bildet eine *Zeitachse*. Die Zeitachse ist der Stammknoten in der Struktur.

Eine Zeitachse muss mindestens eine Gruppe enthalten. Jede Gruppe stellt einen einzelnen Stream in der endgültigen Produktion dar. Ein typisches Projekt umfasst eine Videogruppe und eine Audiogruppe. Kompositionen sind optional. sie sind vorhanden, um bei Bedarf mehr Struktur bereitzustellen.

Die folgende Abbildung zeigt die Beziehungen zwischen untergeordneten und übergeordneten Daten, die eine Zeitachse bilden:

![Knotenstruktur](images/timeline1.png)

Im Folgenden wird eine Zeitachse als temporale Sequenz dargestellt:

![Abbildung der Zeitachse](images/timeline2.png)

Der Pfeil oben stellt die Richtung der Zeitachse dar, beginnend mit der Zeit 0 (null). Innerhalb der Videogruppe hat Track 1 eine höhere Priorität als Track 0. Die Quellobjekte in Spur 1 verdecken die Objekte in Spur 0. Wenn Track 1 leer ist, "zeigt Track 0 durch". Wie bereits erwähnt, werden Audiospuren einfach kombiniert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit DirectShow-Bearbeitungsdiensten](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 



