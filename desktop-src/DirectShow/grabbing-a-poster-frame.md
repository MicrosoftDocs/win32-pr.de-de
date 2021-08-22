---
description: Greifen eines Posterrahmens
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Greifen eines Posterrahmens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6668526d83f17c4ceab260f3a31ed43d19ec1d142bd8f8fdae080161350ded8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536570"
---
# <a name="grabbing-a-poster-frame"></a>Greifen eines Posterrahmens

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

In diesem Artikel wird beschrieben, wie Sie einen Posterrahmen aus einer digitalen Mediendatei anzeigen, indem Sie das [Media Detector-Objekt (MediaDet)](media-detector--mediadet.md) verwenden, das mit [directShow Editing Services bereitgestellt wird.](directshow-editing-services.md)

Die Medienerkennung ist ein Hilfsobjekt, das Formatinformationen aus einer Medienquellendatei erhalten kann. Sie kann auch ein Bitmapbild aus einem Videostream in der Quelldatei greifen. Wenn die Datei durchsetzbar ist, können Sie das Image von einem beliebigen Punkt in der Datei abrufen. Das zurückgegebene Bild hat immer das 24-Bit-RGB-Format.

Die Medienerkennung ist kein Filter, und die Anwendung muss nicht den Filter Graph Manager verwenden oder ein Filterdiagramm erstellen. Intern erstellt die Medienerkennung ein Filterdiagramm, das den [**Sample Grabber Filter enthält.**](sample-grabber-filter.md) Um eine Bitmap zu erhalten, sucht und hält die Medienerkennung das Filterdiagramm an und ruft dann die Bitmap aus dem Filter Sample Grabber ab. Die Anwendung kommuniziert mit dem Media Detector über die [**IMediaDet-Schnittstelle.**](imediadet.md) Die Medienerkennung ist ein gutes Beispiel für das Kapseln eines Filterdiagramms in einem Hilfsobjekt, um Anwendungen vor graphbezogenen Details zu schützen.

Die Medienerkennung wird in zwei Modi betrieben. Wenn Sie sie zum ersten Mal erstellen, befindet sich die Medienerkennung im Modus "Informationssammlung". Sie können den Namen einer Mediendatei angeben und Informationen zu den einzelnen Streams in der Datei erhalten, z. B. den Formattyp, die Bildfrequenz oder die Dauer. Wenn die Datei einen Videostream enthält, können Sie die Medienerkennung in den Modus "Bitmapgrab" wechseln und Bitmaps aus der Quelle abrufen. Sobald Sie dies tun, können Sie die Media Detector jedoch nicht wieder in den ursprünglichen Modus wechseln. sie ist dauerhaft an diesen Videostream angefügt. Um mit einem anderen Stream oder einer anderen Datei zu arbeiten, müssen Sie eine neue Instanz der Medienerkennung erstellen.

> [!Note]  
> In den Codebeispielen in diesem Tutorial wird die ATL **CComPtr-Klasse** verwendet, die die Verweisanzahl automatisch verwaltet. Wenn Sie rohe Schnittstellenzeder verwenden möchten, denken Sie daran, jede Schnittstelle frei zu geben, wenn Sie damit fertig sind. Außerdem wird in den Codebeispielen zur Besserung ein Teil der Fehlerüberprüfung weggelassen, die eine Anwendung ausführen sollte. Überprüfen Sie im funktionierenden Code immer **die HRESULT-Werte.**

 

Folgende Themen werden in diesem Lernprogramm behandelt:

-   [Schritt 1: Erstellen des Windows Frameworks](step-1--create-the-windows-framework.md)
-   [Schritt 2: Hinzufügen eines Menübefehls zum Greifen eines Posterrahmens](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Schritt 3: Implementieren der Frame-Grabbing Funktion](step-3--implement-the-frame-grabbing-function.md)
-   [Schritt 4: Zeichnen der Bitmap im Clientbereich](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow-Bearbeitungsdiensten](using-directshow-editing-services.md)
</dt> </dl>

 

 



