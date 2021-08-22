---
description: Einführung in DirectShow Editing Services
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Einführung in DirectShow Editing Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d12470b45e0b39c32c983176f07444a5136b9e97b99cc5be142974d05178f58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952548"
---
# <a name="introduction-to-directshow-editing-services"></a>Einführung in DirectShow Editing Services

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Der Kern von DirectShow ist eine leistungsstarke Architektur für die Verarbeitung von Streamingmedien. Eine Anwendung kann damit Multimediainhalte wiedergeben, die in einer Vielzahl von Formaten erstellt wurden, ohne dass sich der Entwickler um die Dateikomprimierung und andere mühsame Details kümmern muss. Vor [DirectShow Editing Services](directshow-editing-services.md) (DES) fehlte DirectShow jedoch die Flexibilität, die für die nicht lineare Bearbeitung erforderlich war.

Angenommen, Sie möchten eine Videosequenz erstellen, die aus 4 Sekunden aus Quelle A, gefolgt von 10 Sekunden aus Quelle B und 5 Sekunden aus Quelle C besteht. Dies können Sie relativ einfach erreichen, indem Sie nur die Haupt-DirectShow-API verwenden.

Aber was geschieht, wenn Sie entschieden haben, dass Quelle C vor Quelle B und nicht nachher kommen sollte. , dass die Sequenz 8 Sekunden von Quelle A und nicht von 4 verwenden soll; und dass die gesamte Produktion eine separate Audiospur benötigt, die im Hintergrund wiedergegeben wird? Selbst kleinere Änderungen wie diese können schwierig zu implementieren sein. Das soeben beschriebene Szenario ist jedoch ein triviales Bearbeitungsprojekt in DES– Sie können dies mit einer Handvoll Methodenaufrufen durchführen.

Im Folgenden finden Sie einige der Features, die DES für DirectShow bietet:

-   Ein Zeitachsenmodell, das Video- und Audiospuren in geschachtelten Ebenen organisiert und die Bearbeitung der endgültigen Produktion vereinfacht
-   Die Möglichkeit, eine Vorschau eines Videoprojekts online anzuzeigen
-   Project Persistenz über ein XML-basiertes Format
-   Unterstützung für Video- und Audioeffekte sowie Übergänge zwischen Videospuren (z. B. Einblendungen und Zurücksetzungen)
-   Mehr als 100 Standardmäßige Zurücksetzungen, wie von der Society of Motion Picture and Tv Engineers (SMPTE) definiert
-   Schlüsselung basierend auf Farbton, Leuchtdichte, RGB-Wert oder Alphawert
-   Automatische Konvertierung von Bildraten und Audiosamplingraten, sodass eine Produktionsumgebung heterogene Quellen verwenden kann
-   Ändern der Größe oder Zuschneiden von Videos

Einschränkungen:

-   DES unterstützt keine MPEG-2- oder H.264-Videoquellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Bearbeitungsdienste](directshow-editing-services.md)
</dt> </dl>

 

 



