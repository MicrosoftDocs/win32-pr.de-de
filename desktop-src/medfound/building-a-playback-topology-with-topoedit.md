---
description: Aufbauen einer Wiedergabe Topologie mit topoedit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Aufbauen einer Wiedergabe Topologie mit topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106354888"
---
# <a name="building-a-playback-topology-with-topoedit"></a>Aufbauen einer Wiedergabe Topologie mit topoedit

Topoedit kann eine Wiedergabe Topologie für eine lokale Mediendatei erstellen, indem die Quell-, Transformations-und Ausgabe Knoten automatisch hinzugefügt und verbunden werden. Die Topologie wird von topoedit nicht automatisch aufgelöst. Um die Topologie wiederzugeben, beheben Sie Sie, und verwenden Sie dann die Transport Steuerelemente.

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>So erstellen und wiedergeben Sie eine Topologie für eine Mediendatei

1.  Klicken Sie im Menü **Datei** auf **Datei Rendering**.

    Dadurch wird das Dialogfeld **Medienquelle auswählen** geöffnet.

2.  Navigieren Sie zu dem Ordner, in dem sich die Mediendatei befindet.
3.  Geben Sie im Feld **Dateiname:** den Namen der Datei ein.
4.  Klicken Sie auf **Öffnen**.

    Der Bereich " **Topologie** " zeigt die verbundene Topologie. Intern führt topoedit die folgenden Aufgaben aus:

    -   Listet die Streams in der Mediendatei auf und erstellt die Quellknoten.
    -   Fügt in Abhängigkeit vom Medientyp der Quellknoten Transformations Knoten hinzu, z. b. Decoders.
    -   Fügt die Senke des streamingaudiorenderers (SAR) für den Audiostream und die EVR-Senke (Enhanced Video Renderer) für den Videostream hinzu.
    -   Verbindet die Knoten Eingaben und die Knoten Ausgaben.

5.  Klicken Sie im Menü **Topologie** auf **Topologie auflösen**.
6.  Klicken Sie auf der Symbolleiste auf die Schaltfläche wieder **Gabe** , um die Topologie wiederzugeben Die folgende Abbildung zeigt die **Wiedergabe** Schaltfläche :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wiedergabe Steuerelemente in topoedit](playback-controls-in-topoedit.md)
</dt> <dt>

[Auflösen einer Topologie mit topoedit](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 



