---
description: Overlay Mixer 2-Filter
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Overlay Mixer 2-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b51dceb2a7f82a91fe30275cacfaad4ad78eded
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987353"
---
# <a name="overlay-mixer-2-filter"></a>Overlay Mixer 2-Filter

Der Overlay Mixer 2-Filter ist mit dem Overlay Mixer-Filter identisch, [außer:](overlay-mixer-filter.md)

-   Es werden nur Medientypen mit [**VIDEOINFOHEADER2-Formaten**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) unterstützt.
-   Es hat einen höheren Wert, wodurch es automatisch einem Filterdiagramm hinzugefügt werden kann.

Das Overlay Mixer 2 wird bereitgestellt, damit der Filter-Graph-Manager es dem Diagramm hinzugibt, wenn das MPEG-2-Video ohne DVD gerendert wird. Die Entscheidung, ob Overlay Mixer oder Overlay Mixer 2 verwendet werden soll, wird von der Komponente verarbeitet, die das Diagramm erstellt, entweder vom Filter Graph Manager, dem Capture Graph Builder oder dem DVD Graph Builder. Aus Anwendungssicht sind sie derselbe Filter mit den gleichen Schnittstellen und Funktionen.

Die folgende Tabelle enthält informationen, die spezifisch für overlay Mixer 2 sind. Alle anderen Filterdaten finden Sie in der Dokumentation zum Overlay-Mixer.




| Bezeichnung | Wert |
|--------|-------|
| Eingabepin-Medientypen | Formattyp: Format_VIDEOINFO2 | 
| Filtern der CLSID | CLSID_OverlayMixer2 | 
| <a href="merit.md">Verdienst</a> | <ul><li>MERIT_UNLIKELY</li><li>Windows Vista oder höher: MERIT_DO_NOT_USE</li></ul> | 




 

In Windows Vista oder höher ist der Vorteil des Overlay Mixer 2-Filters NICHT VERWENDEN, da die neueren Videorenderer \_ \_ \_ (VMR-7, VMR-9 und EVR) alle **VIDEOINFOHEADER2-Formate** unterstützen und daher die Overlay-Mixer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> </dl>

 

 



