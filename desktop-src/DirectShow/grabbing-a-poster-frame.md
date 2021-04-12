---
description: Ein Poster-Frame wird gepackt.
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Ein Poster-Frame wird gepackt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482694"
---
# <a name="grabbing-a-poster-frame"></a>Ein Poster-Frame wird gepackt.

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In diesem Artikel wird beschrieben, wie ein Poster-Frame aus einer digitalen Mediendatei mit dem [Media Detector-Objekt (mediadet)](media-detector--mediadet.md) , das mit [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md)bereitgestellt wird, angezeigt wird.

Der Medien Detektor ist ein Hilfsobjekt, das Formatinformationen aus einer Medien Quelldatei erhalten kann. Außerdem kann ein Bitmap-Bild von einem Videostream in der Quelldatei abgeleitet werden. Wenn Sie davon ausgehen, dass die Datei suchbar ist, können Sie das Bild von einem beliebigen Punkt in der Datei abrufen. Das zurückgegebene Image weist immer das 24-Bit-RGB-Format auf.

Der Medien Detektor ist kein Filter, und die Anwendung muss nicht den Filter Graph-Manager verwenden oder ein Filter Diagramm erstellen. Intern erstellt der Medien Detektor ein Filter Diagramm, das den [**Beispiel-Grabber Filter**](sample-grabber-filter.md)enthält. Zum Abrufen einer Bitmap sucht das Medien Erkennungs Tool das Filter Diagramm und hält es an und ruft dann die Bitmap aus dem Sample Grabber-Filter ab. Die Anwendung kommuniziert mit dem Medien Erkennungs Modul über die [**imediadet**](imediadet.md) -Schnittstelle. Der Medien Detektor ist ein gutes Beispiel für das Kapseln eines Filter Diagramms in ein Hilfsobjekt, um Anwendungen vor Diagramm bezogenen Details zu schützen.

Das Medien Erkennungs Modul funktioniert in zwei Modi. Wenn Sie es erstmalig erstellen, befindet sich der Medien Detektor im Modus "Informationserfassung". Sie können den Namen einer Mediendatei angeben und Informationen zu den einzelnen Streams in der Datei erhalten, z. b. den Formattyp, die Frame Rate oder die Dauer. Wenn die Datei einen Videostream enthält, können Sie den Medien Detektor in den Modus "Bitmap-Abruf" wechseln und Bitmaps aus der Quelle abrufen. Wenn Sie dies tun, können Sie das Medien Erkennungs Modul jedoch nicht wieder in den ursprünglichen Modus wechseln. Er ist dauerhaft an den Videostream angefügt. Wenn Sie mit einem anderen Stream oder einer anderen Datei arbeiten möchten, müssen Sie eine neue Instanz des Medien Detektors erstellen.

> [!Note]  
> In den Codebeispielen in diesem Tutorial wird die ATL-Klasse **CComPtr** verwendet, die automatisch Verweis Zähler verwaltet. Wenn Sie es vorziehen, unformatierte Schnittstellen Zeiger zu verwenden, denken Sie daran, alle Schnittstellen freizugeben, wenn Sie damit abgeschlossen sind. Aus Gründen der Übersichtlichkeit lassen die Codebeispiele einen Großteil der Fehlerüberprüfung aus, die von einer Anwendung durchgeführt werden sollte. Überprüfen Sie im Arbeitscode immer **HRESULT** -Werte.

 

Folgende Themen werden in diesem Lernprogramm behandelt:

-   [Schritt 1: Erstellen des Windows-Frameworks](step-1--create-the-windows-framework.md)
-   [Schritt 2: Hinzufügen eines Menübefehls, um einen Poster-Frame zu erfassen](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Schritt 3: Implementieren der Frame-Grabbing-Funktion](step-3--implement-the-frame-grabbing-function.md)
-   [Schritt 4: Zeichnen der Bitmap im Client Bereich](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungs Diensten](using-directshow-editing-services.md)
</dt> </dl>

 

 



