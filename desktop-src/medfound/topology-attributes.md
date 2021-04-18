---
description: Topologieattribute
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Topologieattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286b6dbfe922461083b49d77ad2351e98d562d3b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106371874"
---
# <a name="topology-attributes"></a>Topologieattribute

Die folgenden Attribute gelten für Topologien.



| Attribut                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ DXVA-Modus für MF-Topologie \_](mf-topology-dxva-mode.md)                                                    | Gibt an, ob der topologielader die Microsoft DirectX Video Acceleration (DXVA) in der Topologie aktiviert.                                                                                                                         |
| [dynamische Änderung der MF- \_ Topologie \_ \_ \_ nicht \_ zulässig](mf-topology-dynamic-change-not-allowed.md)                | Gibt an, ob die Medien Sitzung versucht, die Topologie zu ändern, wenn das Format eines Datenstroms geändert wird.                                                                                                                           |
| [MF- \_ Topologie \_ \_ xvp \_ für \_ Wiedergabe aktivieren](mf-topology-enable-xvp-for-playback.md)                | Gibt an, ob der topologielader den Transcode-Video Prozessor (xvp) aktiviert. für Konvertierungen, Aktivieren der Hardware beschleunigten Farbkonvertierung.                                                                                        |
| [MF- \_ Topologie \_ Aufzählen von \_ Quell \_ Typen](mf-topology-enumerate-source-types.md)                         | Gibt an, ob der topologielader die Medientypen auflistet, die von der Medienquelle bereitgestellt werden.                                                                                                                                     |
| [MF- \_ topologiehardware- \_ \_ Modus](mf-topology-hardware-mode.md)                                            | Gibt an, ob hardwarebasierte Transformationen in die Topologie eingeschlossen werden sollen.                                                                                                                                                            |
| [**MF- \_ Topologie \_ ohne \_ Markin \_ markout**](mf-topology-no-markin-markout-attribute.md)                     | Gibt an, ob die Pipeline nur Stichproben Abtastungen                                                                                                                                                                                      |
| [MF- \_ \_ topologiewiedergabe \_ Framerate](mf-topology-playback-framerate.md)                                  | Gibt die Aktualisierungsrate des Monitors an.                                                                                                                                                                                                |
| [maximal zulässige Anzahl von MF- \_ \_ topologiewiedergabe \_ \_](mf-topology-playback-max-dims.md)                                   | Gibt die Größe des Zielfensters für die Videowiedergabe an.                                                                                                                                                                   |
| [**MF- \_ Topologie \_ ProjectStart**](mf-topology-projectstart-attribute.md)                                 | Gibt die Startzeit der Topologie innerhalb des aktuellen Segments in 100-Nanosecond-Einheiten an.                                                                                                                                             |
| [**MF- \_ Topologie \_ projectstoppt**](mf-topology-projectstop-attribute.md)                                   | Gibt die Endzeit der topologieendzeit innerhalb des aktuellen Segments in 100-Nanosecond-Einheiten an.                                                                                                                                              |
| [**Status der MF- \_ topologieauflösung \_ \_**](mf-topology-resolution-status-attribute.md)                      | Gibt den Status eines Versuchs zum Auflösen einer Topologie an.                                                                                                                                                                          |
| [\_Start Zeit der MF-Topologie \_ \_ \_ bei \_ Präsentations \_ Schalter](mf-topology-start-time-on-presentation-switch.md) | Gibt die Startzeit für Präsentationen an, die nach der ersten Präsentation in die Warteschlange eingereiht werden.                                                                                                                                           |
| [\_Optimierungen der statischen \_ topologiewiedergabe \_ \_](mf-topology-static-playback-optimizations.md)           | Aktiviert statische Optimierungen in der Video Pipeline.                                                                                                                                                                                |
| [MFT \_ fieldofuse \_ Unlock- \_ Attribut](mft-fieldofuse-unlock-attribute.md)                                | Enthält einen [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger, der verwendet wird, um ein MFT mit Einschränkungen für das Feld zu entsperren. Weitere Informationen finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung". |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 



