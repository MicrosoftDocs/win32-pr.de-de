---
description: Sink Writer-Attribute
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Sink Writer-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bf64dd4279ef2e35ed86f50c4444412b3cc70205f6aad52adac8a41895af11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012368"
---
# <a name="sink-writer-attributes"></a>Sink Writer-Attribute

Die folgenden Attribute können verwendet werden, um den Senkenwriter zu initialisieren.



| attribute                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GERINGE LATENZ BEI MF \_ \_](mf-low-latency.md)                                                     | Ermöglicht die Verarbeitung mit geringer Latenz.                                                                                                                                                                                                    |
| [MF \_ READWRITE \_ DISABLE \_ CONVERTERS](mf-readwrite-disable-converters.md)                  | Aktiviert oder deaktiviert Formatkonvertierungen durch den Senkenwriter.                                                                                                                                                                         |
| [MF \_ READWRITE ENABLE HARDWARE TRANSFORMS (MF-READWRITE \_ AKTIVIEREN VON \_ \_ HARDWARETRANSFORMATIONEN)](mf-readwrite-enable-hardware-transforms.md) | Ermöglicht dem Senkenwriter die Verwendung hardwarebasierter Media Foundation Transformationen (MFTs).                                                                                                                                                  |
| [ASYNCHRONER MF \_ SINK \_ \_ \_ WRITER-RÜCKRUF](mf-sink-writer-async-callback.md)                     | Enthält einen Zeiger auf die Rückrufschnittstelle der Anwendung für den Senkenwriter.                                                                                                                                                    |
| [DEAKTIVIEREN DER \_ DROSSELUNG DURCH MF SINK \_ \_ \_ WRITER](mf-sink-writer-disable-throttling.md)             | Gibt an, ob der Senkenschreiber die Rate eingehender Daten einschränkt.                                                                                                                                                                |
| [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md)                             | Gibt den Containertyp der Ausgabedatei an.                                                                                                                                                                                   |
| [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md)                  | Enthält einen [**FIELDFieldOfUseMFTUnlock-Zeiger,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) der zum Entsperren eines MFT mit Verwendungseinschränkungen verwendet wird. Weitere Informationen finden Sie unter [Verwendungseinschränkungen.](field-of-use-restrictions.md) |
| [MF \_ SINK \_ WRITER \_ D3D \_ MANAGER](mf-sink-writer-d3d-manager.md)                           | Verwenden Sie dieses Attribut, um ein Direct3D-Gerät für alle Videoencoder oder Mediensenken zur Verfügung zu stellen, die vom Senkenwriter geladen werden.                                                                                                                   |



 

Verwenden Sie diese Attribute mit den folgenden Methoden und Funktionen:

-   [**WRITEReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**WRITEReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Um eines dieser Attribute zu verwenden, rufen Sie zuerst [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attributspeicher zu erstellen. Verwenden Sie dann die [**BENUTZERDEFINIERTEAttributes-Schnittstelle,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) um die gewünschten Attribute für den Attributspeicher fest zu legen. Übergeben Sie **den ZEIGER FÜR ATTRIBUTEAttributes** auf den *pAttributes-Parameter* einer der zuvor aufgeführten Methoden oder Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**BESinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



