---
description: Verwenden des Senkenschreibers
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Verwenden des Senkenschreibers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4fa472bd1a5121454b3ffb06def7082508432b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110488"
---
# <a name="using-the-sink-writer"></a>Verwenden des Senkenschreibers

## <a name="overview"></a>Übersicht

### <a name="file-container-types"></a>Dateicontainertypen

Der Senkenwriter verfügt über integrierte Unterstützung für mehrere Dateicontainertypen. Eine vollständige Liste finden Sie unter [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md). Sie können zusätzliche Containertypen unterstützen, indem Sie eine benutzerdefinierte [Mediensenke schreiben.](media-sinks.md) Der Dateicontainer wird angegeben, wenn Sie eine neue Instanz des Senkenwriters erstellen.

### <a name="stream-formats"></a>Streamformate

Für jeden Stream muss die Anwendung Folgendes angeben.

-   Das *Eingabeformat ist* das Format, das die Anwendung an den Senkenwriter sendet.
-   Das *Ausgabeformat* ist das Format, das in die Datei geschrieben wird.

Die Eingabe- und Ausgabeformate können entweder komprimiert oder unkomprimiert werden. Der Senkenwriter unterstützt die folgenden Kombinationen:

-   Unkomprimierte Eingabe mit komprimierter Ausgabe. Dies ist der typische Fall und wird für Codierungs- oder Transcodierungsszenarien verwendet. Ein Microsoft Media Foundation encoder muss verfügbar sein, der den Eingabetyp akzeptiert und in den Ausgabetyp codiert.
-   Komprimierte Eingabe mit identischer Ausgabe. Verwenden Sie diese Kombination, um eine Datei ohne Transcodierung neu zu erstellen.
-   Unkomprimierte Eingabe mit identischer Ausgabe. Verwenden Sie diese Kombination, um unkomprimierte Audio- oder Videodaten in einen Dateicontainer zu schreiben.

Der Senkenwriter unterstützt keine Videoänderung, Bildfrequenzkonvertierung oder Audio-Resampling, es sei denn, diese Funktionen werden vom Encoder bereitgestellt. Andernfalls kann die Anwendung [Digital Signal Processors](windowsmediadigitalsignalprocessors.md) verwenden, um die Eingabedaten zu konvertieren, bevor die Daten an gesendet werden.

## <a name="creating-the-sink-writer"></a>Erstellen des Senkenwriters

Es gibt zwei Funktionen, die den Senkenwriter erstellen:

-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) verwendet die URL einer Ausgabedatei oder einen Zeiger auf einen Bytestream. Diese Funktion erstellt die Mediensenke intern.
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) verwendet einen Zeiger auf eine Mediensenke, die bereits von der Anwendung erstellt wurde.

Wenn Sie eine der integrierten Mediensenken verwenden, ist die [**MFCreateSinkWriterFromURL-Funktion**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) vorzuziehen, da der Aufrufer die Mediensenke nicht konfigurieren muss.

Die [**MFCreateSinkWriterFromURL-Methode**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) bietet mehrere Optionen zum Angeben des Dateicontainertyps. Im einfachsten Fall verwendet die Funktion die Dateinamenerweiterung in der URL, um den Dateicontainer auszuwählen. Weitere Informationen finden Sie auf der Funktionsreferenzseite.

Der folgende Code gibt beispielsweise den Dateinamen "output.wmv" für die URL an. Basierend auf der Dateinamenerweiterung lädt der Senkenwriter die [ASF-Mediensenke,](asf-media-sinks.md) um eine ASF-Datei (Advanced Systems Format) zu erstellen.


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



Im Fall von [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)wird der Dateityp durch die Mediensenke bestimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sink Writer](sink-writer.md)
</dt> </dl>

 

 



