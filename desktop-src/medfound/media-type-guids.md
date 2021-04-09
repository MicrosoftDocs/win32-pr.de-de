---
description: Wichtige Medientypen
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Wichtige Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961190"
---
# <a name="major-media-types"></a>Wichtige Medientypen

In einem Medientyp beschreibt der *Haupttyp* die Gesamtkategorie der Daten, z. b. Audiodaten oder Videos. Wenn der *Untertyp* vorhanden ist, wird der Haupttyp weiter verfeinert. Wenn der Haupttyp z. b. "Video" ist, kann der Untertyp "32-Bit RGB Video" lauten. Untertypen unterscheiden auch codierte Formate, wie z. b. H. 264-Video, von nicht komprimierten Formaten.

Der Haupttyp und der Untertyp werden von GUIDs identifiziert und in den folgenden Attributen gespeichert:



| Attribut                                             | BESCHREIBUNG |
|-------------------------------------------------------|-------------|
| [Haupt-Typ des MF- \_ MT \_ \_](mf-mt-major-type-attribute.md) | Der Haupttyp. |
| [MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md)        | Untertyp.    |



 

Die folgenden Haupttypen sind definiert.



| Haupttyp                    | BESCHREIBUNG                                                                                                                                                | Untertypen                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **MF MediaType \_ -Audiodatei**        | Audio.                                                                                                                                                     | [Audiountertyp-GUIDs](audio-subtype-guids.md).      |
| **MF MediaType- \_ Binärdatei**       | Binärer Datenstrom.                                                                                                                                             | Keine.                                                |
| **MF MediaType- \_ Filetransfer** | Ein Datenstrom, der Datendateien enthält.                                                                                                                         | Keine.                                                |
| **MF MediaType- \_ HTML**         | HTML-Stream.                                                                                                                                               | Keine.                                                |
| **MF MediaType- \_ Image**        | Image Datenstrom.                                                                                                                                        | [WIC-GUIDs und CLSIDs](../wic/-wic-guids-clsids.md).       |
| **MF MediaType \_ geschützt**    | Geschützte Medien.                                                                                                                                           | Der Untertyp gibt das Inhalts Schutzschema an. |
| **MF MediaType- \_ Wahrnehmung**   | Datenströme von einem Kamerasensor oder einer Verarbeitungseinheit, die auf unformatierte Videodaten und das Verständnis der Umgebung oder der Menschen in der IT-Abteilung verzichten. | Keine.                                                |
| **MF MediaType \_ Sami**         | Synchronisierte, barrierefreie Medienaustausch Beschriftungen (Sami).                                                                                                 | Keine.                                                |
| **MF MediaType- \_ Skript**       | Skript Datenstrom.                                                                                                                                             | Keine.                                                |
| **MF MediaType-Daten \_ Strom**       | Multiplexed-Stream oder elementare Datenstrom.                                                                                                                   | [Stream-Untertyp-GUIDs](stream-subtype-guids.md)     |
| **MF MediaType- \_ Video**        | Video.                                                                                                                                                     | [Video Untertyp-GUIDs](video-subtype-guids.md).      |



 

Komponenten von Drittanbietern können neue Haupttypen und neue Untertypen definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Medientypen](media-types.md)
</dt> </dl>

 

 
