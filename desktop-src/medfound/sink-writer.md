---
description: Der senkwriter ist eine Komponente zum Codieren von Audiodateien oder Videodateien.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Senke-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344388"
---
# <a name="sink-writer"></a>Senke-Writer

Der senkwriter ist eine Komponente zum Codieren von Audiodateien oder Videodateien.

Das folgende Diagramm zeigt, wie eine Anwendung den senkwriter zum Codieren der Audiodatei und der Audiodatei verwendet.

![ein Diagramm, das den Senke-Writer anzeigt.](images/encoding09.png)

Der Senke Writer hostet eine Medien Senke und optional einen oder mehrere Encoder. Die Encoder konvertieren unkomprimierte Audiodaten oder Videodaten in codierte Bitstreams. Die Medien Senke gibt die Bitstreams in einer Datei aus. Der Senke-Writer führt die folgenden Aufgaben aus:

-   Lädt die Medien Senke.
-   Findet und lädt die Encoder.
-   Verwaltet den Datenfluss zu den Encodern und der Medien Senke.

Die Anwendung übergibt Audiodaten und Videodaten als Eingabe an den senkwriter. Es spielt keine Rolle, wie die Anwendung die Eingabedaten abruft oder generiert. Eine Möglichkeit ist die Verwendung des [Quell Readers](source-reader.md), wie in der folgenden Abbildung dargestellt. Der sendende Writer erfordert jedoch nicht die Verwendung des Quell Readers. Diese beiden Komponenten sind unabhängig voneinander.

![ein Diagramm, in dem der Quell-und der Senke Writer angezeigt werden.](images/encoding02.png)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Verwenden des Senke Writers](using-the-sink-writer.md)
-   [Tutorial: Verwenden des senkwriter zum Codieren von Videos](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Codierung und Dateierstellung](encoding-and-file-authoring.md)
</dt> <dt>

[Übersicht über die Codierung in Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



