---
description: Audiodaten Ströme
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Audiodaten Ströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f5c8c74f7507557f374d690a671b62e8b43343
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482534"
---
# <a name="audio-and-subpicture-streams"></a>Audiodaten Ströme

Eine DVD-Video Platte kann bis zu acht Audiostreams aufweisen, die von 0 bis 7 nummeriert sind und jeweils bis zu sechs diskrete Kanäle enthalten. (Beachten Sie, dass Audiodaten Ströme von 0 (null) nummeriert werden, während Titel, Winkel und Eltern Ebenen von eins nummeriert werden.) Nur einer dieser Streams kann zu einem bestimmten Zeitpunkt ausgewählt werden. Für untergeordnete Bilder sind bis zu 32 Streams verfügbar, obwohl jeweils nur ein Stream aktiviert werden kann. Datenträger werden im Allgemeinen mit standardmäßigen Audiodaten und unter bildstreams erstellt, aber eine Anwendung kann es Benutzern ermöglichen, eine Liste aller verfügbaren Streams anzuzeigen und Sie in der von Ihnen bevorzugten Sprache auszuwählen. Die grundlegenden Schritte in diesem Prozess sind sowohl für Audiodaten als auch für teilbildstreams identisch.

1.  Legen Sie die Anzahl der für einen Titel verfügbaren Streams fest.
2.  Iterieren Sie die Streams, und rufen Sie die Datenstrom Attribute für jedes ab.
3.  Rufen Sie den Sprachcode aus dem zurückgegebenen Gebiets Schema Bezeichner (LCID) ab, und erstellen Sie eine lesbare Zeichenfolge.
4.  Füllt ein Listenfeld oder eine andere Benutzeroberfläche (UI)-Steuerelement auf, um dem Benutzer die Auswahl eines bevorzugten Streams zu ermöglichen.

In der DVD-Beispielanwendung veranschaulicht die caudiolangdlg:: makeaudiostreamlist-Methode in Dialogs. cpp die grundlegenden Schritte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



