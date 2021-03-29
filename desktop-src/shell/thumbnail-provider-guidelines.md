---
description: Wenn Sie eine Miniaturansicht bereitstellen, sollten die folgenden Richtlinien befolgt werden.
title: Richtlinien für Miniaturansichten
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a1d29992-1347-4574-81b9-b90e2b0938f1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 062c363b4faea9fd07888a55e2dd3896b138c599
ms.sourcegitcommit: 9763c9cb859df3530766b6e65f9dce4f7de87fd2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2020
ms.locfileid: "104102582"
---
# <a name="thumbnail-handler-guidelines"></a>Richtlinien für Miniaturansichten

Wenn Sie eine Miniaturansicht bereitstellen, sollten die folgenden Richtlinien befolgt werden.

-   Stellen Sie Miniaturansichten bereit, die bei einer Auflösung von 256 x 256 Pixel in 32-Bit-Farbe gut angezeigt werden. Eine Miniaturansicht dieser Größe wird vom Lesebereich von Windows Vista verwendet, wenn kein registrierter Vorschau Handler vorhanden ist. Ein Vorschau Handler ist jedoch die bevorzugte Option und sollte nach Möglichkeit bereitgestellt werden.
-   Wenn Sie mehrere Abbilder mit unterschiedlichen Größen erstellen, erstellen Sie nicht die kleineren Bilder aus der größeren, indem Sie die Seite, den Frame oder das Bild zuschneiden. Skalieren Sie das gesamte Bild herunter.
-   Nicht mehrere Seiten, Frames oder Bilder gleichzeitig anzeigen; Verwenden Sie einfach eine. Wenn ein Dokument aus mehreren Seiten besteht, z. b. einem Textdokument oder einem Arbeitsblatt, das aus mehreren Arbeitsblättern besteht, ist die Seite Abdeckung oft die beste Wahl, aber unabhängig davon, welche Option Sie verwenden, verwenden Sie nur eine. Aggregieren Sie keine unterschiedlichen Seiten, was ein übersichtliches aussehen ermöglicht.
-   Windows Vista ist für das horizontale herunter-oder Herunterskalieren von Sampling-Images verantwortlich. Wenn Ihr Handler nach einem größeren Abbild gefragt wird, als Sie verfügbar sind, geben Sie die nächstgelegene Größe an. Versuchen Sie nicht, die Größe Ihres eigenen Bilds dynamisch zu ändern.
-   Gibt immer ein Miniaturbild von Ihrem Handler zurück, anstatt eine spezielle Logik zum Zurückgeben von herkömmlichen Symbolen auszuführen. Unter einer bestimmten Größe zeigt Windows Vista automatisch ein herkömmliches Symbol anstelle der Miniaturansicht an. Weitere Informationen finden Sie im Abschnitt "Miniaturansicht: *Cache und Größen* Anpassung" von Miniatur Ansichts [Handlern](thumbnail-providers.md) .
-   Gibt immer eine Miniaturansicht mit dem Seitenverhältnis der Seite, des Frames oder Bilds zurück. Verwenden Sie Alpha nicht zum Vervollständigen eines Quadrats. Windows Vista ist für die ordnungsgemäße Positionierung eines nicht quadratischen Bilds verantwortlich.
-   Fügen Sie Ihren Miniaturansichten keine Zusatzelemente hinzu. Windows Vista wendet ggf. automatisch Drop Shadows und andere Zusatzelemente an. Es wendet auch spezielle Zusatzelemente für bestimmte Dateitypen an, z. b. Bilder oder Videos.
-   Überlagern Sie keine Dateityp-oder Anwendungsinformationen in der Miniaturansicht. Windows Vista zeigt in der unteren rechten Ecke des Bilds eine typüberlagerung an. Diese Überlagerung basiert auf einem wahrgenommenen Typ, kann jedoch für einzelne Dateitypen festgelegt werden.
-   Um eine bessere Leistung zu erzielen, wenn die Miniaturansicht auf Dateiinhalt basiert – eine Seite eines Dokuments, z. b. –, speichern Sie das Vorschaubild, wenn die Datei gespeichert wird (und daher wahrscheinlich geändert wird), anstatt Sie in Echtzeit zu berechnen. Dies sollte erfolgen, wenn die Berechnung Speicher intensiv ist (mehr als ein oder zwei Sekunden). Wenn dies nicht der Fall ist, werden Sichten, für die eine große Anzahl von Dateien angezeigt wird, deren Miniaturansichten von unterschiedlichen Handlern verarbeitet werden, etwas Zeit in Anspruch nehmen – eine schlechte Benutzer Leistung. In Windows Vista werden Miniaturansichten zwischengespeichert, und es wird auf den Zeitpunkt der letzten Änderung verwiesen, um zu bestimmen, ob eine Miniaturansicht
-   Beachten Sie, dass der Explorer eine Miniaturansicht möglicherweise nicht anzeigt, auch wenn ein Anbieter verfügbar ist. Beispielsweise wird eine Datei, die auf einem Band archiviert wurde, nicht zurückgerufen, um die Miniaturansicht zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Miniatur Ansichts Handler](thumbnail-providers.md)
</dt> <dt>

[Entwickeln von Miniatur Ansichts Handlern](building-thumbnail-providers.md)
</dt> </dl>

 

 



