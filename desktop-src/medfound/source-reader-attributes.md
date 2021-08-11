---
description: Quellleseattribute
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Quellleseattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7bd9c5b3c5a71fb1b91515400fb0cf3670bd3b73b6635c811dcc79bd05e74f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238328"
---
# <a name="source-reader-attributes"></a>Quellleseattribute

Die folgenden Attribute können verwendet werden, um den [Quellleser zu initialisieren.](source-reader.md)



| attribute                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GERINGE LATENZ BEI MF \_ \_](mf-low-latency.md)                                                                               | Ermöglicht die Verarbeitung mit geringer Latenz.                                                                                                                                                                                                    |
| [MF \_ READWRITE \_ DISABLE \_ CONVERTERS](mf-readwrite-disable-converters.md)                                            | Aktiviert oder deaktiviert Formatkonvertierungen durch den Quellreader.                                                                                                                                                                       |
| [MF \_ READWRITE \_ AKTIVIEREN VON \_ \_ HARDWARETRANSFORMATIONEN](mf-readwrite-enable-hardware-transforms.md)                           | Ermöglicht dem Quellleser die Verwendung hardwarebasierter Media Foundation (MFTs).                                                                                                                                                |
| [ASYNCHRONER RÜCKRUF \_ DES MF-QUELLLESERS \_ \_ \_](mf-source-reader-async-callback.md)                                           | Enthält einen Zeiger auf die Rückrufschnittstelle der Anwendung für den Quellreader.                                                                                                                                                  |
| [\_ \_ MF-QUELLLESER \_ D3D-MANAGER \_](mf-source-reader-d3d-manager.md)                                                 | Enthält einen Zeiger auf die Microsoft [Direct3D-Geräte-Manager](direct3d-device-manager.md).                                                                                                                                        |
| [MF \_ SOURCE \_ READER \_ DISABLE \_ DXVA](mf-source-reader-disable-dxva.md)                                               | Gibt an, ob der Quellleser die DirectX-Videobeschleunigung (DXVA) für den Videodecoder aktiviert.                                                                                                                                |
| [\_MF-QUELLLESER \_ \_ TRENNEN \_ MEDIASOURCE BEIM \_ \_ HERUNTERFAHREN](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Gibt an, ob der Quellreader die Medienquelle herunter fährt.<br/> Gilt nur, wenn die Anwendung den Quellleser aus einem vorhandenen Medienquellenobjekt erstellt.<br/>                                           |
| [\_MF-QUELLLESER \_ \_ AKTIVIEREN DER \_ \_ ERWEITERTEN \_ VIDEOVERARBEITUNG](mf-source-reader-enable-advanced-video-processing.md)     | Ermöglicht die erweiterte Videoverarbeitung durch den Quellleser, [](source-reader.md)einschließlich Farbraumkonvertierung, Deinterlacing, Video-Größen- und Bildfrequenzkonvertierung.                                                           |
| [\_MF-QUELLLESER \_ \_ AKTIVIEREN DER \_ \_ VIDEOVERARBEITUNG](mf-source-reader-enable-video-processing.md)                        | Ermöglicht die eingeschränkte Videoverarbeitung durch den Quellleser.                                                                                                                                                                             |
| [\_ \_ MEDIASOURCE-KONFIGURATION DES \_ \_ MF-QUELLLESERS](mf-source-reader-mediasource-config.md)                                   | Enthält Konfigurationseigenschaften für die Medienquelle.                                                                                                                                                                            |
| [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md)                                            | Enthält einen [**FIELDFieldOfUseMFTUnlock-Zeiger,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) der zum Entsperren eines MFT mit Verwendungseinschränkungen verwendet wird. Weitere Informationen finden Sie unter [Verwendungseinschränkungen.](field-of-use-restrictions.md) |



 

Verwenden Sie diese Attribute mit den folgenden Methoden und Funktionen:

-   [**WRITEReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**WRITEReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Um eines dieser Attribute zu verwenden, rufen Sie zuerst [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attributspeicher zu erstellen. Verwenden Sie dann die [**BENUTZERDEFINIERTEAttributes-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) um die gewünschten Attribute für den Attributspeicher festlegen. Übergeben Sie **den ATTRIBUTATTRIBUTES-Zeiger** an den *pAttributes-Parameter* einer der zuvor aufgeführten Methoden oder Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Quellleser](source-reader.md)
</dt> <dt>

[**VERERBUNGQuelleLeser**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




