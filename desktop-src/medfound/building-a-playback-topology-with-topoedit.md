---
description: Erstellen einer Wiedergabetopologie mit TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Erstellen einer Wiedergabetopologie mit TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a71ae353c11108fe7c844d8ddd6441e652e007646b91f44c6fe2b480a22a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035428"
---
# <a name="building-a-playback-topology-with-topoedit"></a>Erstellen einer Wiedergabetopologie mit TopoEdit

TopoEdit kann eine Wiedergabetopologie für eine lokale Mediendatei erstellen, indem die Quell-, Transformations- und Ausgabeknoten automatisch hinzugefügt und verbunden werden. TopoEdit löst die Topologie nicht automatisch auf. Um die Topologie wieder zu verwenden, lösen Sie sie auf, und verwenden Sie dann die Transportsteuerelemente.

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>So erstellen und spielen Sie eine Topologie für eine Mediendatei ab

1.  Klicken Sie **im Menü** Datei auf **Datei rendern.**

    Dadurch wird das **Dialogfeld Medienquelle** auswählen geöffnet.

2.  Navigieren Sie zu dem Ordner, in dem sich die Mediendatei befindet.
3.  Geben Sie **im Feld Dateiname:** den Namen der Datei ein.
4.  Klicken Sie auf **Öffnen**.

    Im **Topologiebereich wird** die verbundene Topologie angezeigt. Intern führt TopoEdit die folgenden Aufgaben aus:

    -   Enumeriert die Streams in der Mediendatei und erstellt die Quellknoten.
    -   Je nach Medientyp der Quellknoten fügt Transformationsknoten hinzu, z. B. Decoder.
    -   Fügt die SAR-Senke (Streaming Audio Renderer) für den Audiostream und die EVR-Senke (Enhanced Video Renderer) für den Videostream hinzu.
    -   Verbindet die Knoteneingaben und die Knotenausgabe.

5.  Klicken Sie **im Menü Topologie** auf Topologie **auflösen.**
6.  Klicken Sie auf **der Symbolleiste** auf die Schaltfläche Wiedergabe, um die Topologie wieder anzuzeigen. Die folgende Abbildung zeigt die **Wiedergabeschaltfläche** :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiedergabesteuerelemente in TopoEdit](playback-controls-in-topoedit.md)
</dt> <dt>

[Auflösen einer Topologie mit TopoEdit](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



