---
description: Topologieattribute
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Topologieattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db599a9d55e960bbb38043aa8932cd66ae0cbb6d9b376f403c1886faf3155c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972849"
---
# <a name="topology-attributes"></a>Topologieattribute

Die folgenden Attribute gelten für Topologien.



| attribute                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_MF-TOPOLOGIE \_ – \_ DXVA-MODUS](mf-topology-dxva-mode.md)                                                    | Gibt an, ob das Topologieladeprogramm die Microsoft DirectX-Videobeschleunigung (DXVA) in der Topologie aktiviert.                                                                                                                         |
| [DYNAMISCHE \_ ÄNDERUNG DER MF-TOPOLOGIE \_ NICHT \_ \_ \_ ZULÄSSIG](mf-topology-dynamic-change-not-allowed.md)                | Gibt an, ob die Mediensitzung versucht, die Topologie zu ändern, wenn sich das Format eines Streams ändert.                                                                                                                           |
| [MF \_ TOPOLOGY ENABLE XVP FOR PLAYBACK (MF-TOPOLOGIE \_ AKTIVIEREN VON \_ XVP FÜR DIE \_ \_ WIEDERGABE)](mf-topology-enable-xvp-for-playback.md)                | Gibt an, ob das Topologieladeprogramm den Transcode Video Processor (XVP) aktiviert. für Konvertierungen, wodurch die hardwarebeschleunigte Farbkonvertierung aktiviert wird.                                                                                        |
| [\_MF-TOPOLOGIE \_ ENUMERIEREN \_ VON \_ QUELLTYPEN](mf-topology-enumerate-source-types.md)                         | Gibt an, ob das Topologieladeprogramm die von der Medienquelle bereitgestellten Medientypen aufzählt.                                                                                                                                     |
| [\_MF-TOPOLOGIE– \_ \_ HARDWAREMODUS](mf-topology-hardware-mode.md)                                            | Gibt an, ob hardwarebasierte Transformationen in die Topologie eingeschlossen werden sollen.                                                                                                                                                            |
| [**\_MF-TOPOLOGIE \_ OHNE \_ MARKIN \_ MARKOUT**](mf-topology-no-markin-markout-attribute.md)                     | Gibt an, ob die Pipeline Stichproben abschneiden soll.                                                                                                                                                                                      |
| [\_MF-TOPOLOGIE \_ – \_ WIEDERGABEFRAMERATE](mf-topology-playback-framerate.md)                                  | Gibt die Aktualisierungsrate des Monitors an.                                                                                                                                                                                                |
| [\_MF-TOPOLOGIE \_ – WIEDERGABE \_ \_ MAX. DIMS](mf-topology-playback-max-dims.md)                                   | Gibt die Größe des Zielfensters für die Videowiedergabe an.                                                                                                                                                                   |
| [**\_ \_ MF-TOPOLOGIEPROJEKTSTART**](mf-topology-projectstart-attribute.md)                                 | Gibt die Startzeit der Topologie innerhalb des aktuellen Segments in Einheiten von 100 Nanosekunden an.                                                                                                                                             |
| [**\_ \_ MF-TOPOLOGIEPROJEKTETOP**](mf-topology-projectstop-attribute.md)                                   | Gibt die Topologiestoppzeit innerhalb des aktuellen Segments in Einheiten von 100 Nanosekunden an.                                                                                                                                              |
| [**\_AUFLÖSUNGSSTATUS DER MF-TOPOLOGIE \_ \_**](mf-topology-resolution-status-attribute.md)                      | Gibt den Status eines Versuchs an, eine Topologie aufzulösen.                                                                                                                                                                          |
| [STARTZEIT \_ DER MF-TOPOLOGIE \_ BEI \_ \_ \_ \_ PRÄSENTATIONSSCHALTER](mf-topology-start-time-on-presentation-switch.md) | Gibt die Startzeit für Präsentationen an, die nach der ersten Präsentation in die Warteschlange eingereiht werden.                                                                                                                                           |
| [\_MF-TOPOLOGIE \_ – STATISCHE \_ \_ WIEDERGABEOPTIMIERUNGEN](mf-topology-static-playback-optimizations.md)           | Aktiviert statische Optimierungen in der Videopipeline.                                                                                                                                                                                |
| [MFT \_ FIELDOFUSE \_ \_ UNLOCK-Attribut](mft-fieldofuse-unlock-attribute.md)                                | Enthält einen [**POINTERFieldOfUseMFTUnlock-Zeiger,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) der zum Entsperren eines MFT mit Verwendungsfeldeinschränkungen verwendet wird. Weitere Informationen finden Sie unter [Field of Use Restrictions](field-of-use-restrictions.md). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**TOPOLOGIE**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 



