---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Verwenden des Senke Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959367"
---
# <a name="using-the-sink-writer"></a>Verwenden des Senke Writers

## <a name="overview"></a>Übersicht

### <a name="file-container-types"></a>Datei Container Typen

Der senkwriter verfügt über integrierte Unterstützung für mehrere Datei Containertypen. Eine komplette Liste finden Sie unter [MF \_ transcode \_ ContainerType](mf-transcode-containertype.md). Sie können zusätzliche Containertypen unterstützen, indem Sie eine benutzerdefinierte [Medien Senke](media-sinks.md)schreiben. Der Datei Container wird beim Erstellen einer neuen Instanz des Senke Writers angegeben.

### <a name="stream-formats"></a>Streamformate

Die Anwendung muss für jeden Stream Folgendes angeben:

-   Das *Eingabeformat* ist das Format, das die Anwendung an den senkenwriter sendet.
-   Das *Ausgabeformat* ist das Format, das in die Datei geschrieben wird.

Die Eingabe-und Ausgabeformate können entweder komprimiert oder unkomprimiert sein. Der Senke Writer unterstützt die folgenden Kombinationen:

-   Unkomprimierte Eingabe mit komprimierter Ausgabe. Dies ist der typische Fall, der zum Codieren oder transcodieren von Szenarien verwendet wird. Es muss ein Microsoft Media Foundation Encoder verfügbar sein, der den Eingabetyp akzeptiert und in den Ausgabetyp codiert.
-   Komprimierte Eingabe mit identischer Ausgabe. Verwenden Sie diese Kombination, um eine Datei ohne Transcodierung zu reaktivieren.
-   Unkomprimierte Eingabe mit identischer Ausgabe. Verwenden Sie diese Kombination, um unkomprimierte Audiodaten oder Videos in einen Datei Container zu schreiben.

Der sendende Writer unterstützt keine Videogröße, keine Frame-Raten-Konvertierung oder audioprobennahme, es sei denn, diese Funktionen werden vom Encoder bereitgestellt. Andernfalls kann die Anwendung [digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md) verwenden, um die Eingabedaten zu konvertieren, bevor die Daten an das

## <a name="creating-the-sink-writer"></a>Erstellen des Senke Writers

Es gibt zwei Funktionen, die den Senke-Writer erstellen:

-   [**Mfkreatesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) übernimmt die URL einer Ausgabedatei oder einen Zeiger auf einen Bytestream. Diese Funktion erstellt die Medien Senke intern.
-   [**Mfkreatesinkschreiterfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) übernimmt einen Zeiger auf eine Medien Senke, die bereits von der Anwendung erstellt wurde.

Wenn Sie eine der integrierten Medien senken verwenden, ist die [**mfkreatesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) -Funktion vorzuziehen, da der Aufrufer die Medien Senke nicht konfigurieren muss.

Die [**MF | atesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) -Methode bietet verschiedene Optionen zum Angeben des Typs des Datei Containers. Im einfachsten Fall verwendet die-Funktion die Dateinamenerweiterung in der URL, um den Datei Container auszuwählen. Weitere Informationen finden Sie auf der Seite Funktionsreferenz.

Der folgende Code gibt z. b. den Dateinamen "Output. wmv" für die URL an. Basierend auf der Dateinamenerweiterung lädt der senkenwriter die [ASF-Medien Senke](asf-media-sinks.md) , um eine ASF-Datei (Advanced Systems Format) zu erstellen.


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



Im Fall von [**mfkreatesinkschreibfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)wird der Dateityp von der Medien Senke bestimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Senke-Writer](sink-writer.md)
</dt> </dl>

 

 



