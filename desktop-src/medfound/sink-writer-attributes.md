---
description: Senkenwriter-Attribute
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Senkenwriter-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130469"
---
# <a name="sink-writer-attributes"></a>Senkenwriter-Attribute

Die folgenden Attribute können verwendet werden, um den senkenwriter zu initialisieren.



| Attribut                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF mit \_ niedriger \_ Latenz](mf-low-latency.md)                                                     | Ermöglicht die Verarbeitung mit niedriger Latenz.                                                                                                                                                                                                    |
| [MF- \_ Lese Schreibvorgänge \_ Deaktivieren \_](mf-readwrite-disable-converters.md)                  | Aktiviert oder deaktiviert Formatkonvertierungen durch den senkenwriter.                                                                                                                                                                         |
| [MF- \_ Lese schreiben \_ Aktivieren von \_ Hardware \_ Transformationen](mf-readwrite-enable-hardware-transforms.md) | Ermöglicht es dem senkenwriter, hardwarebasierte Media Foundation Transformationen (MFTs) zu verwenden.                                                                                                                                                  |
| [asynchroner Rückruf für den MF- \_ Senke \_ \_ \_](mf-sink-writer-async-callback.md)                     | Enthält einen Zeiger auf die Rückruf Schnittstelle der Anwendung für den Senke-Writer.                                                                                                                                                    |
| [MF- \_ Sink- \_ Writer Deaktivieren der \_ \_ Drosselung](mf-sink-writer-disable-throttling.md)             | Gibt an, ob der senderwriter die Rate eingehender Daten einschränkt.                                                                                                                                                                |
| [MF- \_ transcode- \_ ContainerType](mf-transcode-containertype.md)                             | Gibt den Containertyp der Ausgabedatei an.                                                                                                                                                                                   |
| [MFT \_ fieldofuse \_ Unlock- \_ Attribut](mft-fieldofuse-unlock-attribute.md)                  | Enthält einen [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger, der verwendet wird, um ein MFT mit Einschränkungen für das Feld zu entsperren. Weitere Informationen finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung". |
| [MF \_ Sink \_ Writer \_ D3D \_ Manager](mf-sink-writer-d3d-manager.md)                           | Verwenden Sie dieses Attribut, um ein Direct3D-Gerät für alle Video Encoder oder Medien senken bereitzustellen, die vom senkenwriter geladen werden.                                                                                                                   |



 

Verwenden Sie diese Attribute mit den folgenden Methoden und Funktionen:

-   [**Imfreadschreiteclassfactory:: kreateinstancefromuject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**Imfreadschreiteclassfactory:: forateinstancefromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**Mfkreatesinkschreiterfrommediasink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MF | atesinkschreiterfromurl**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Um eines dieser Attribute zu verwenden, rufen Sie zuerst [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen. Verwenden Sie dann die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle, um die gewünschten Attribute im Attribut Speicher festzulegen. Übergeben Sie den **imfattributes** -Zeiger an den *pattributes* -Parameter einer der zuvor aufgeführten Methoden oder Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Imbersink Writer**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



