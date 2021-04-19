---
description: Filter für Überlagerungs Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filter für Überlagerungs Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342558"
---
# <a name="overlay-mixer-2-filter"></a>Filter für Überlagerungs Mixer 2

Der Filter für den Overlay-Mixer 2 ist mit dem [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter identisch, außer:

-   Es werden nur Medientypen mit [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Formaten unterstützt.
-   Sie hat einen höheren Wert, der die automatische Hinzufügung zu einem Filter Diagramm ermöglicht.

Der Overlay-Mixer 2 wird bereitgestellt, damit der Filter Graph-Manager ihn dem Diagramm hinzufügt, wenn er ein nicht-DVD-MPEG-2-Video rendert. Die Wahl, ob der Overlay-Mixer oder der Überlagerungs-Mixer 2 verwendet werden soll, wird von der Komponente behandelt, die das Diagramm erstellt, entweder mit dem Filter Graph-Manager, dem Erfassungs Diagramm-Generator oder dem DVD-Diagramm-Generator. Aus Sicht der Anwendung sind Sie derselbe Filter mit denselben Schnittstellen und Funktionen.

Die folgende Tabelle enthält spezifische Informationen zum Overlay-Mixer 2. Alle anderen Filterdaten finden Sie in der Dokumentation für den Overlay-Mixer.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Eingabe-PIN-Medientypen</td>
<td>Formattyp: Format_VIDEOINFO2</td>
</tr>
<tr class="even">
<td>CLSID Filtern</td>
<td>CLSID_OverlayMixer2</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Verdienst</a></td>
<td><ul>
<li>MERIT_UNLIKELY</li>
<li>Windows Vista oder höher: MERIT_DO_NOT_USE</li>
</ul></td>
</tr>
</tbody>
</table>



 

In Windows Vista oder höher ist die Verwendung des Filters für den Overlay-Mixer 2 \_ nicht sinnvoll, \_ \_ da die neueren Videorenderer (VMR-7, VMR-9 und EVR) alle **VIDEOINFOHEADER2** -Formate unterstützen, und daher ist es nicht notwendig, den Overlay-Mixer zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



