---
title: DVD
description: DVD
ms.assetid: b3634a28-b1d6-44a5-97e4-fcc1f655d652
keywords:
- Windows Media Player, Migrieren von DVDs
- Windows Media Player-Objektmodell, DVDs
- Objektmodell, DVDs
- Windows Media Player ActiveX-Steuerelement, DVDs
- ActiveX-Steuerelement, DVDs
- Windows Media Player Mobile ActiveX-Steuerelement, DVDs
- Windows Media Player Mobile, Migrieren von DVDs
- Migrations Handbuch, DVDs
- DVD-Migration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e0a19818ac01b5e3d6138f896f26fe674c5ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711627"
---
# <a name="dvd"></a>DVD

Das ActiveX-Steuerelement von Windows Media Player 6,4 enthält ein **DVD** -Objekt, das eine Vielzahl von Methoden und Eigenschaften verfügbar macht, und ein Ereignis, um speziell mit DVD-Inhalten umzugehen. Um beispielsweise die Anzahl der verfügbaren DVD-Titel zu ermitteln, verwenden Sie **Player6**. **titlesavailable** -Eigenschaft:


```C++
var numTitles = WMP64.DVD.TitlesAvailable;

```



Mit dem Objektmodell Windows Media Player 7 oder höher wird ein stärker integrierter Ansatz für DVD implementiert. DVD-spezifische Eigenschaften, Methoden und Ereignisse werden nur bei Bedarf implementiert. Andernfalls funktionieren vorhandene Objektmodell Funktionen wie erwartet mit DVD-Medien. Wenn Sie z. b. die Anzahl der verfügbaren DVD-Titel ermitteln möchten, wenn Sie Windows Media Player 7 oder höher verwenden, rufen Sie ein **Wiedergabe** Listen Objekt aus dem **CDROM** -Objekt ab:


```C++
var dvdTitles = WMP9.cdromCollection.item(0).playlist;

```



Im vorangehenden Beispiel wird ein **Wiedergabe** Listen Objekt mit einem ersten Eintrag abgerufen, der das DVD-Medium auf dem ersten Laufwerk darstellt. Zusätzliche Einträge stellen einzelne DVD-Titel dar. Daher kann die Anzahl der verfügbaren Titel wie folgt berechnet werden:


```C++
var numTitles = dvdTitles.count - 1;

```



Im folgenden finden Sie die wichtigsten Unterschiede, die bei der Migration von Version 6,4 zu beachten sind:

-   Die DVD-Wiedergabe wird nur unterstützt, wenn Windows Media Player für Windows XP oder höher und das Betriebssystem Windows XP oder höher verwendet werden.
-   DVD-ROM-Laufwerke werden genau wie CD-ROM-Laufwerke mit dem **cdromcollection** -Objekt aufgelistet.
-   Einzelne DVD-ROM-Laufwerke werden mithilfe des **CDROM** -Objekts verwaltet.
-   Das **DVD** -Objekt erweitert das Objektmodell mit Methoden und einer Eigenschaft, die speziell für die Arbeit mit DVD vorgesehen ist.
-   Es gibt zwei neue Ereignisse: **openplaylistswitch** und **domainchange**, speziell für die Arbeit mit DVD.
-   Der DVD-Inhalt wird mithilfe von **Wiedergabe** Listen Objekten und **Medien** Objekten organisiert.
-   DVD-Sprachen werden mithilfe der sprach Funktionalität verwaltet **, die im Steuerelement Objekt (** Windows Media Player 9 oder höher) verfügbar ist.
-   Transport Steuerelemente und Positionsinformationen für DVD funktionieren identisch mit denen für andere digitale Medientypen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Handbuch für die Migration des Objektmodells**](object-model-migration-guide.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements mit Visual Basic**](using-the-windows-media-player-control-with-visual-basic.md)
</dt> </dl>

 

 




