---
description: Decodierung
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Decodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867319"
---
# <a name="decoding"></a>Decodierung

Um Metadaten ordnungsgemäß zu unterstützen, müssen Decoder-Autoren folgende Aktionen ausführen:

-   Implementieren Sie die [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) -und [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstellen.
-   Implementieren Sie [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) auf dem Frame-Decoder. Wenn der Codec Metadaten auf Container Ebene unterstützt, muss diese Schnittstelle sowohl für den Decoder auf Container Ebene als auch für den Frame Decoder implementiert werden.
-   Beim Decodieren des bildstreams muss [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) aufgerufen werden, um einen metadatenreader für jeden Metadatenblock zu instanziieren. (Alle neuen metadatenleser, die der Codec implementiert, müssen bei WIC registriert werden.)

    Der Decoder sollte keine eigenen metadatenleser erstellen, sondern stattdessen WIC verwenden, um Sie basierend auf den metadatenblöcken im Datenstrom zu erstellen. Der Decoder muss dies für alle gefundenen Blöcke ausführen, auch wenn Sie dem docoder nicht nativ bekannt sind, da zukünftige metadatenleser möglicherweise auf dem System installiert sind, die verstehen, wie diese Metadatenblöcke behandelt werden.

-   Wenn kein Metadatenhandler für einen-Block vorhanden ist, instanziieren Sie den unbekannten metadatenreader, indem Sie die Optionen für die Metadatenerstellung verwenden.
-   Machen Sie die Auflistung von metadatenlesern über die [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) -Schnittstelle verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



