---
description: Hauptmedientypen
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Hauptmedientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549575"
---
# <a name="major-media-types"></a>Hauptmedientypen

In einem Medientyp beschreibt der *Haupttyp* die Gesamtkategorie der Daten, z. B. Audio oder Video. Der *Untertyp*, sofern vorhanden, verfeinern den Haupttyp weiter. Wenn der Haupttyp beispielsweise video ist, kann der Untertyp 32-Bit-RGB-Video sein. Untertypen unterscheiden auch codierte Formate, z.B. H.264-Video, von nicht komprimierten Formaten.

Haupttyp und Untertyp werden durch GUIDs identifiziert und in den folgenden Attributen gespeichert:



| attribute                                             | Beschreibung |
|-------------------------------------------------------|-------------|
| [MF \_ \_ MT-HAUPTTYP \_](mf-mt-major-type-attribute.md) | Haupttyp. |
| [MF \_ \_ MT-UNTERTYP](mf-mt-subtype-attribute.md)        | Untertyp.    |



 

Die folgenden Haupttypen sind definiert.



| Haupttyp                    | Beschreibung                                                                                                                                                | Untertypen                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **MFMediaType \_ Audio**        | Audio.                                                                                                                                                     | [Audiountertyp-GUIDs](audio-subtype-guids.md).      |
| **MFMediaType \_ Binary**       | Binärer Stream.                                                                                                                                             | Keine.                                                |
| **MFMediaType \_ FileTransfer** | Ein Stream, der Datendateien enthält.                                                                                                                         | Keine.                                                |
| **MFMediaType \_ HTML**         | HTML-Stream.                                                                                                                                               | Keine.                                                |
| **MFMediaType-Image \_**        | Noch-Bilddatenstrom.                                                                                                                                        | [WIC-GUIDs und CLSIDs](../wic/-wic-guids-clsids.md).       |
| **MFMediaType-Metadaten \_**        | Metadatenstream.                                                                                                                                        | Keine.       |
| **MFMediaType \_ Protected**    | Geschützte Medien.                                                                                                                                           | Der Untertyp gibt das Inhaltsschutzschema an. |
| **MFMediaType \_ Perception**   | Datenströme von einem Kamerasensor oder einer Verarbeitungseinheit, die unformatiert Videodaten auslösen und verstehen und ein Verständnis der Umgebung oder der Menschen in ihr bieten. | Keine.                                                |
| **MFMediaType \_ SAMI**         | Synchronisierte SAMI-Untertitel (Accessible Media Interchange).                                                                                                 | Keine.                                                |
| **MFMediaType-Skript \_**       | Skriptstream.                                                                                                                                             | Keine.                                                |
| **MFMediaType-Stream \_**       | Multiplexstream oder elementarer Stream.                                                                                                                   | [GuiDs des Streamuntertyps](stream-subtype-guids.md)     |
| **\_MFMediaType-Video**        | Video.                                                                                                                                                     | [Video-Untertyp-GUIDs](video-subtype-guids.md).      |



 

Komponenten von Drittanbietern können neue Haupttypen und neue Untertypen definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 
