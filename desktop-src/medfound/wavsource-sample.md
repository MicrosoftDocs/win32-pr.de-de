---
description: WavSource-Beispiel
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: WavSource-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba8ab5bfd5ae1ccfb4df4c90b447c412e9e835a403d496834224f012f8bad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972539"
---
# <a name="wavsource-sample"></a>WavSource-Beispiel

Zeigt, wie eine benutzerdefinierte Medienquelle in Microsoft Media Foundation erstellt wird. Im Beispiel wird eine Medienquelle implementiert, die WAV-Audiodateien analysiert.

Dieses Beispiel ist ein relativ einfaches Beispiel für eine Medienquelle:

-   Es gibt nur einen Stream, sodass kein Code zum Implementieren der Streamauswahl vorhanden ist.
-   Die Medienquelle implementiert keine Ratensteuerung (d.b. schnelle Vorwärts- oder Umgekehrtwiedergabe).
-   Alle Quell- und Streammethoden werden als synchrone Methoden implementiert.
-   Da der Datenteil einer WAV-Datei ein einzelner Block von nicht komprimierten PCM-Audiodaten ist, muss die Medienquelle während der Wiedergabe keine Paketheader lesen oder den Stream auf andere Weise analysieren, außer den anfänglichen [**WAVEFORMAT-Header**](/windows/win32/api/mmreg/ns-mmreg-waveformat) zu lesen.

Ein erweitertes Beispiel für eine Medienquelle finden Sie im [MPEG1Source-Beispiel.](mpeg1source-sample.md)

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**GIGABYTEByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**WFMEDIASOURCE**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**WFMEDIASTREAM**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Verbrauch

Das WavSource-Beispiel erstellt eine DLL, die ein COM-Server für die Medienquelle und den Bytestreamhandler der Medienquelle ist. Bevor Sie die Medienquelle verwenden, müssen Sie die DLL registrieren.

Um die Medienquelle zu verwenden, können Sie [basicPlayback](/previous-versions//bb970475(v=vs.85))ausführen. Der Quell resolver lädt die Medienquelle automatisch, wenn Sie eine WAV-Datei für die Wiedergabe auswählen. (Wenn ein Fehler auftritt, stellen Sie sicher, dass Sie die WavSource-DLL erfolgreich registriert haben.)

Sie können auch das Tool TopoEdit verwenden, um eine Wiedergabetopologie zu erstellen, die die Medienquelle enthält. Weitere Informationen zu TopoEdit finden Sie unter [TopoEdit](topoedit.md).

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [github-Repository Windows klassischen Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[MPEG1Source-Beispiel](mpeg1source-sample.md)
</dt> <dt>

[Schemahandler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Schreiben einer benutzerdefinierten Medienquelle](writing-a-custom-media-source.md)
</dt> </dl>

 

 
