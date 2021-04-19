---
description: MPEG1Source-Beispiel
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: MPEG1Source-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359937"
---
# <a name="mpeg1source-sample"></a>MPEG1Source-Beispiel

Zeigt, wie Sie eine benutzerdefinierte Medienquelle in Microsoft Media Foundation schreiben. Im Beispiel wird eine Medienquelle implementiert, die MPEG-1-System Schicht-Streams analysiert und Beispiele generiert, die MPEG-1-Nutzlasten enthalten.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**IMF bytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**Imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMF Media Stream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

Bevor Sie dieses Beispiel untersuchen, sollten Sie sich das [Beispiel für wavsource](wavsource-sample.md)ansehen, das eine einfachere Implementierung einer Medienquelle ermöglicht. Im MPEG1Source-Beispiel werden einige Features hinzugefügt, die in den meisten realen Implementierungen einer Medienquelle zu finden sind:

-   Mehrere Datenströme
-   Asynchrone Methoden
-   Asynchrone e/a

Im Windows SDK für Windows Server 2008 enthält dieses Beispiel auch einen MPEG-1-Beispiel Video Decoder, der den Zeit Code für jeden Videorahmen anzeigt. (In diesem Fall wird der MPEG-1-Bitstream nicht decodiert.)

Ab dem Windows SDK für Windows 7 wurde der Decoder in ein separates Beispiel verschoben. Siehe [Decoder-Beispiel](decoder-sample.md).

## <a name="usage"></a>Verbrauch

Im MPEG1Source-Beispiel wird eine DLL erstellt, bei der es sich um einen com-Server für die Medienquelle, den bytestreamhandler der Medienquelle und den Decoder-MFT handelt. Vor der Verwendung der Medienquelle müssen Sie die dll registrieren.

Wenn Sie die Medienquelle verwenden möchten, können Sie das [basicplayback-Beispiel](/previous-versions//bb970475(v=vs.85))ausführen. Der quellresolver lädt automatisch die Medienquelle, wenn Sie eine MPEG-1-Datei für die Wiedergabe auswählen. (Wenn ein Fehler auftritt, stellen Sie sicher, dass Sie die MPEG1Source-dll erfolgreich registriert haben.)

Sie können auch das Tool topoedit verwenden, um eine Wiedergabe Topologie zu erstellen, die die Medienquelle enthält. Weitere Informationen zu topoedit finden Sie unter [topoedit](topoedit.md).

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Medienquellen](media-sources.md)
</dt> <dt>

[Schema Handler und Byte-Stream Handler](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Tutorial: Schreiben einer benutzerdefinierten Medienquelle](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[Wavsource-Beispiel](wavsource-sample.md)
</dt> </dl>

 

 
