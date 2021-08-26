---
description: Der Senkenwriter ist eine Komponente zum Codieren von Audio- oder Videodateien.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Sink Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1cfa60abb9b107030aba18e30175592d637c7676ff44781d62b3f5c1509351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887354"
---
# <a name="sink-writer"></a>Sink Writer

Der Senkenwriter ist eine Komponente zum Codieren von Audio- oder Videodateien.

Das folgende Diagramm zeigt auf hoher Ebene, wie eine Anwendung den Senkenwriter verwendet, um die Audio-/Videodatei zu codieren.

![Ein Diagramm, das den Senkenwriter zeigt.](images/encoding09.png)

Der Senkenwriter hostet eine Mediensenke und optional einen oder mehrere Encoder. Die Encoder konvertieren unkomprimierte Audio- oder Videodaten in codierte Bitstreams. Die Mediensenke gibt die Bitstreams in eine Datei aus. Der Senkenwriter führt die folgenden Aufgaben aus:

-   Lädt die Mediensenke.
-   Sucht und lädt die Encoder.
-   Verwaltet den Datenfluss zu den Encodern und der Mediensenke.

Die Anwendung übergibt Audio-/Videodaten als Eingabe an den Senkenwriter. Es spielt keine Rolle, wie die Anwendung die Eingabedaten erhält oder generiert. Eine Möglichkeit besteht darin, den [Quellleser](source-reader.md)zu verwenden, wie im folgenden Diagramm dargestellt. Der Senkenwriter erfordert jedoch nicht die Verwendung des Quelllesers. Diese beiden Komponenten sind unabhängig.

![Ein Diagramm, das den Quellleser und den Senkenwriter zeigt.](images/encoding02.png)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Verwenden des Senkenwriters](using-the-sink-writer.md)
-   [Tutorial: Verwenden des Sink Writer zum Codieren von Videos](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codierung und Dateierstellung](encoding-and-file-authoring.md)
</dt> <dt>

[Übersicht über die Codierung in Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



