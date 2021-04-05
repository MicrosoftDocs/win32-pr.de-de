---
description: Streamdeskriptorattribute
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Streamdeskriptorattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753841"
---
# <a name="stream-descriptor-attributes"></a>Streamdeskriptorattribute

## <a name="common-stream-descriptor-attributes"></a>Allgemeine streamdeskriptorattribute

Die folgenden Attribute gelten für streamdeskriptoren.



| Attribut                                                   | BESCHREIBUNG                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MF \_ SD- \_ Sprache**](mf-sd-language-attribute.md)        | Gibt die Sprache für einen Datenstrom an.                                                  |
| [MF- \_ SD \_ gegenseitig \_ ausschließen](mf-sd-mutually-exclusive.md) | Gibt an, ob sich ein Stream mit anderen Streams desselben Typs gegenseitig ausschließt. |
| [**MF \_ SD- \_ geschützt**](mf-sd-protected-attribute.md)      | Gibt an, ob ein Stream geschützte Inhalte enthält.                                |
| [MF-SD-Daten \_ \_ Strom \_ Name](mf-sd-stream-name.md)               | Enthält den Namen eines Streams.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>Attribute des ASF-Specific Stream-Deskriptors

Die folgenden Attribute gelten für streamdeskriptoren für ASF-Dateien (Advanced Systems Format).



| Attribut                                                                                                                | BESCHREIBUNG                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ extstraumprop \_ AVG \_ bufferSize**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Gibt die durchschnittliche Puffergröße an, die für einen Datenstrom in einer ASF-Datei (in Bytes) benötigt wird.            |
| [**MF SD-Datei (in Bytes) \_ \_ \_ \_ \_ \_**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Gibt die durchschnittliche Daten Bitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.        |
| [**MF \_ SD \_ - \_ Datei-ID der extstrinmprop- \_ Sprache \_ ID \_ Index**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Gibt die Sprache an, die von einem Datenstrom in einer ASF-Datei verwendet wird.                                    |
| [**MF \_ SD. \_ ASF \_ extstraumprop \_ Max \_ bufferSize**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Gibt die maximale Puffergröße an, die für einen Datenstrom in einer ASF-Datei (in Bytes) benötigt wird.            |
| [**MF \_ SD \_ , \_ \_ maximal zulässige \_ Daten \_ Bitrate**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Gibt die maximale datenbitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.         |
| [**Vorlage für die \_ Geräte Konformität der MF SD- \_ \_ \_ metadatengeräte \_ \_**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Gibt die Geräte Konformitäts Vorlage für einen Datenstrom in einer ASF-Datei in Bits pro Sekunde an. |
| [**MF \_ SD, \_ ASF \_ streambitraten \_ Bitrate**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Gibt die durchschnittliche Bitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Deskriptorattribute des Sami-Medien-Quelldaten Stroms

Das folgende Attribut gilt für den Datenstrom Deskriptor für die Sami Media-Quelle.



| Attribut                                                       | BESCHREIBUNG                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MF, \_ SD, \_ Samisch \_**](mf-sd-sami-language-attribute.md) | Enthält den für den Stream definierten Sami-Sprachnamen (für den verfügbaren Medienaustausch). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMF-Deskriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



