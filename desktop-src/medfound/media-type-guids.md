---
description: Hauptmedientypen
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Hauptmedientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec660dcb86cfd1da5a80bef106ee8ddd17cf1e89899fea6b824fba5ab9be04e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715300"
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
| **MFMediaType \_ Binary**       | Binärer Datenstrom.                                                                                                                                             | Keine.                                                |
| **MFMediaType \_ FileTransfer** | Ein Stream, der Datendateien enthält.                                                                                                                         | Keine.                                                |
| **MFMediaType \_ HTML**         | HTML-Stream.                                                                                                                                               | Keine.                                                |
| **\_MFMediaType-Bild**        | Noch-Bilddatenstrom.                                                                                                                                        | [WIC-GUIDs und CLSIDs](../wic/-wic-guids-clsids.md).       |
| **\_MFMediaType-Metadaten**        | Metadatenstream.                                                                                                                                        | Keine.       |
| **MFMediaType \_ Protected**    | Geschützte Medien.                                                                                                                                           | Der Untertyp gibt das Inhaltsschutzschema an. |
| **MFMediaType \_ Perception**   | Streams von einem Kamerasensor oder einer Verarbeitungseinheit aus, die rohe Videodaten begründet und versteht und ein Verständnis der Umgebung oder der Darin enthaltenen Menschen bietet. | Keine.                                                |
| **MFMediaType \_ SAMI**         | Synchronisierte SAMI-Untertitel (Accessible Media Interchange).                                                                                                 | Keine.                                                |
| **\_MFMediaType-Skript**       | Skriptstream.                                                                                                                                             | Keine.                                                |
| **\_MFMediaType-Stream**       | Multiplexstream oder elementarer Stream.                                                                                                                   | [Stream-Untertyp-GUIDs](stream-subtype-guids.md)     |
| **\_MFMediaType-Video**        | Video.                                                                                                                                                     | [Video-Untertyp-GUIDs](video-subtype-guids.md).      |



 

Komponenten von Drittanbietern können neue Haupttypen und neue Untertypen definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ARCHEMEDIATYPE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 
