---
description: Verwalten von Videobearbeitungsprojekten
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Verwalten von Videobearbeitungsprojekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe226f4fdc43889daac8e978086c67bd81c5d8d822902e7c041bf500f2836fb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584450"
---
# <a name="managing-video-editing-projects"></a>Verwalten von Videobearbeitungsprojekten

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Die folgenden Tipps helfen Ihnen beim Verwalten von Projekten in [DirectShow Editing Services](directshow-editing-services.md).

Änderungen an der Zeitachse

-   Wenn Sie die Zeitachse nach dem Erstellen des Filterdiagramms ändern, rufen Sie [**erneut IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) auf, um das Front-End neu zu erstellen. In der Regel wirkt sich dies nicht auf den Rest des Diagramms aus. Gelegentlich muss die Render-Engine jedoch das gesamte Diagramm löschen, bevor das Front-End neu erstellt wird. (Dies geschieht beispielsweise, wenn Sie eine Gruppe hinzufügen oder entfernen.) Die **ConnectFrontEnd-Methode** gibt S WARN OUTPUTRESET zurück, um zu \_ \_ signalisieren, dass das Diagramm gelöscht wurde. In diesem Fall muss Ihre Anwendung den Renderingabschnitt des Graphen neu erstellen.
-   Um alle Objekte vollständig aus der Zeitachse zu entfernen, rufen Sie die [**IAMTimeline::ClearAllGroups-Methode**](iamtimeline-clearallgroups.md) auf.

**Bereinigung**

-   Wenn Sie mit der Verwendung einer Render-Engine fertig sind, rufen Sie die [**IRenderEngine::ScrapIt-Methode**](irenderengine-scrapit.md) auf. Geben Sie wie bei jedem COM-Objekt jeden Schnittstellenzeiger frei, wenn Sie ihn nicht mehr verwenden.
-   Die Render-Engine hält keine Verweisanzahl auf der Zeitachse. Geben Sie die Zeitachse nicht frei, bevor Sie sie nicht mehr verwenden, und rufen Sie **zuerst ScrapIt** in der Render-Engine auf.
-   Wenn Sie alle Verweise auf eine Zeitachse frei geben, verwenden Sie keines der Objekte in dieser Zeitachse, auch wenn Sie die Verweisanzahl für sie halten.

**Mehrere Zeitachseninstanzen**

-   Verschieben Sie zeitachsenobjekte nicht zwischen Zeitachsen. Jedes Objekt in einer Zeitachse muss von dieser Zeitachse erstellt werden. Die Zeitachse enthält einen internen Cache mit Informationen zu den von ihr erstellten Objekten. Das Verschieben von Zeitachsenobjekten kann den Cache unterbrechen.
-   Verwenden Sie nie dieselbe Instanz einer Render-Engine mit mehr als einer Zeitachse. Die Render-Engine enthält einen Cache mit Informationen zur Zeitachse. Mehrere Zeitachsen unterbrechen den Cache und führen zu unvorhersehbaren Ergebnissen. Wenn Sie zwei aktive Zeitachsen benötigen, erstellen Sie separate Instanzen von Render-Engines für jede Zeitachse.
-   Eine Zeitachse kann mehrere Render-Engine verwenden, aber nicht gleichzeitig. Löschen Sie die alte Render-Engine, bevor Sie eine andere Render-Engine verwenden. (Sie würden dies in der Regel tun, wenn Sie von der einfachen Render-Engine für die Vorschauversion zur intelligenten Render-Engine zum Schreiben von Dateien wechseln.)

**Persistenz**

-   Das Filterdiagramm ist nicht persistent, wenn Sie das Projekt in einer XML-Datei speichern. Daher verlieren Sie alle Informationen im Zusammenhang mit der intelligenten Neukomprimierung, dem Komprimierungsformat oder den Komprimierungsparametern. Die Anwendung muss diese Parameter wiederherstellen, nachdem sie ein Projekt geladen hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungsdiensten](using-directshow-editing-services.md)
</dt> </dl>

 

 



