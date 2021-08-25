---
description: Streamdeskriptorattribute
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Streamdeskriptorattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db29ef0076415ff07e9ed25f7e6ca3e0588ec25257802fe0c7829ab3178c935
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953230"
---
# <a name="stream-descriptor-attributes"></a>Streamdeskriptorattribute

## <a name="common-stream-descriptor-attributes"></a>Allgemeine Streamdeskriptorattribute

Die folgenden Attribute gelten für Streamdeskriptoren.



| attribute                                                   | BESCHREIBUNG                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MF \_ SD \_ LANGUAGE**](mf-sd-language-attribute.md)        | Gibt die Sprache für einen Stream an.                                                  |
| [MF \_ SD SCHLIEßEN SICH GEGENSEITIG \_ \_ AUS](mf-sd-mutually-exclusive.md) | Gibt an, ob sich ein Stream mit anderen Streams desselben Typs gegenseitig ausdrungen hat. |
| [**MF \_ SD \_ PROTECTED**](mf-sd-protected-attribute.md)      | Gibt an, ob ein Stream geschützten Inhalt enthält.                                |
| [MF \_ SD \_ STREAM \_ NAME](mf-sd-stream-name.md)               | Enthält den Namen eines Streams.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>ASF-Specific Streamdeskriptorattribute

Die folgenden Attribute gelten für Streamdeskriptoren für ASF-Dateien (Advanced Systems Format).



| attribute                                                                                                                | BESCHREIBUNG                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Gibt die durchschnittliche Puffergröße an, die für einen Stream in einer ASF-Datei in Bytes erforderlich ist.            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Gibt die durchschnittliche Datenbitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.        |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE \_ ID \_ INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Gibt die Sprache an, die von einem Stream in einer ASF-Datei verwendet wird.                                    |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Gibt die maximale Puffergröße in Byte an, die für einen Stream in einer ASF-Datei erforderlich ist.            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Gibt die maximale Datenbitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.         |
| [**MF \_ SD \_ ASF \_ METADATA \_ DEVICE \_ CONFORMANCE \_ TEMPLATE**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Gibt die Gerätekonformitätsvorlage für einen Stream in einer ASF-Datei in Bits pro Sekunde an. |
| [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATE**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Gibt die durchschnittliche Bitrate eines Streams in einer ASF-Datei in Bits pro Sekunde an.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>SAMI Media Source Stream Descriptor Attributes

Das folgende Attribut gilt für den Streamdeskriptor für die SAMI-Medienquelle.



| attribute                                                       | BESCHREIBUNG                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ SAMI \_ LANGUAGE**](mf-sd-sami-language-attribute.md) | Enthält den SAMI-Sprachnamen (Synchronized Accessible Media Interchange), der für den Stream definiert ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**JAVASCRIPTStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> </dl>

 

 



