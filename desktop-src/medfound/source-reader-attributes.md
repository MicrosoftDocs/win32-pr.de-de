---
description: Attribute des Quell Readers
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Attribute des Quell Readers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f425710139b2aebf23ff13a2593ba6931c78fe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753864"
---
# <a name="source-reader-attributes"></a>Attribute des Quell Readers

Die folgenden Attribute können zum Initialisieren des [Quell Readers](source-reader.md)verwendet werden.



| Attribut                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF mit \_ niedriger \_ Latenz](mf-low-latency.md)                                                                               | Ermöglicht die Verarbeitung mit niedriger Latenz.                                                                                                                                                                                                    |
| [MF- \_ Lese Schreibvorgänge \_ Deaktivieren \_](mf-readwrite-disable-converters.md)                                            | Aktiviert oder deaktiviert Formatkonvertierungen durch den Quell Reader.                                                                                                                                                                       |
| [MF- \_ Lese schreiben \_ Aktivieren von \_ Hardware \_ Transformationen](mf-readwrite-enable-hardware-transforms.md)                           | Ermöglicht dem Quell Leser die Verwendung von hardwarebasierten Media Foundation Transformationen (MFTs).                                                                                                                                                |
| [\_ \_ \_ Async- \_ Rückruf für den MF-Quell Leser](mf-source-reader-async-callback.md)                                           | Enthält einen Zeiger auf die Rückruf Schnittstelle der Anwendung für den Quell Reader.                                                                                                                                                  |
| [MF- \_ Quell \_ Leser \_ D3D \_ Manager](mf-source-reader-d3d-manager.md)                                                 | Enthält einen Zeiger auf den Microsoft [Direct3D-Device Manager](direct3d-device-manager.md).                                                                                                                                        |
| [MF- \_ Quell \_ Leser \_ deaktiviert \_ DXVA](mf-source-reader-disable-dxva.md)                                               | Gibt an, ob der Quell Leser eine DirectX-Videobeschleunigung (DXVA) im Video Decoder ermöglicht.                                                                                                                                |
| [der MF- \_ Quell \_ Leser \_ trennt \_ MediaSource \_ beim \_ Herunterfahren.](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Gibt an, ob der Quell Leser die Medienquelle herunterfährt.<br/> Gilt nur, wenn die Anwendung den Quell Leser aus einem vorhandenen Medienquellen Objekt erstellt.<br/>                                           |
| [MF- \_ Quell \_ Leser Aktivieren der \_ \_ erweiterten \_ Video \_ Verarbeitung](mf-source-reader-enable-advanced-video-processing.md)     | Ermöglicht die erweiterte Videoverarbeitung durch den [Quell Leser](source-reader.md), einschließlich der Farb Raum Konvertierung, der Deinterlacing, der Videogröße und der Konvertierung von Frameraten.                                                           |
| [MF- \_ Quell \_ Leser Aktivieren der \_ \_ Video \_ Verarbeitung](mf-source-reader-enable-video-processing.md)                        | Ermöglicht die eingeschränkte Videoverarbeitung durch den Quell Reader.                                                                                                                                                                             |
| [\_ \_ \_ MediaSource-Konfiguration für MF-Quell Leser \_](mf-source-reader-mediasource-config.md)                                   | Enthält Konfigurations Eigenschaften für die Medienquelle.                                                                                                                                                                            |
| [MFT \_ fieldofuse \_ Unlock- \_ Attribut](mft-fieldofuse-unlock-attribute.md)                                            | Enthält einen [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger, der verwendet wird, um ein MFT mit Einschränkungen für das Feld zu entsperren. Weitere Informationen finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung". |



 

Verwenden Sie diese Attribute mit den folgenden Methoden und Funktionen:

-   [**Imfreadschreiteclassfactory:: kreateinstancefromuject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**Imfreadschreiteclassfactory:: forateinstancefromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MF | atesourcereaderfromb-testream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**Mfkreatesourcereaderfrommediasource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MF | atesourcereaderfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Um eines dieser Attribute zu verwenden, rufen Sie zuerst [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen. Verwenden Sie dann die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle, um die gewünschten Attribute im Attribut Speicher festzulegen. Übergeben Sie den **imfattributes** -Zeiger an den *pattributes* -Parameter einer der zuvor aufgeführten Methoden oder Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Quell Leser](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




