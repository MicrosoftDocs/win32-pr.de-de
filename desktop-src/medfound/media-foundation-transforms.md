---
description: Media Foundation Transformationen
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Media Foundation Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61057831383c808a3e05cbe2e9cd779b46522a7a3d52d379b936f27c549d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268700"
---
# <a name="media-foundation-transforms"></a>Media Foundation Transformationen

Media Foundation Transforms (MFTs) stellen ein generisches Modell für die Verarbeitung von Mediendaten zur Verfügung. MFTs werden für Decoder, Encoder und digitale Signalprozessoren (DSPs) verwendet. Kurz gesagt: Alles, was sich in der Medienpipeline zwischen der Medienquelle und der Mediensenke befindet, ist ein MFT.

In diesem Abschnitt werden das MFT-Programmiermodell und die Implementierung eines MFT mit Empfehlungen für bestimmte Typen von MFTs, z. B. Decoder, beschrieben.



| Thema                                                                    | BESCHREIBUNG                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu MFTs](about-mfts.md)                                             | Bietet eine kurze Übersicht über MFTs.                                                                                                                                                                   |
| [Grundlegendes MFT-Verarbeitungsmodell](basic-mft-processing-model.md)             | Beschreibt das grundlegende Modell für die Verarbeitung von Daten mit MFT ausführlicher.                                                                                                                           |
| [Asynchrone MFTs](asynchronous-mfts.md)                               | Beschreibt ein asynchrones Verarbeitungsmodell, das eine Alternative zum Basismodell ist.<br/> Die asynchrone Verarbeitung wurde in Windows 7 eingeführt. Dieses Modell wird nicht von jedem MFT unterstützt.<br/> |
| [Registrieren und Aufzählen von MFTs](registering-and-enumerating-mfts.md) | Registrieren eines MFT und Aufzählen von MFTs in der Registrierung                                                                                                                                   |
| [Nutzungseinschränkungen](field-of-use-restrictions.md)               | Beschreibt den Mechanismus zum Entsperren eines MFT mit Verwendungseinschränkungen.                                                                                                                    |
| [Vergleich von MFTs und DMOs](comparison-of-mfts-and-dmos.md)           | Fasst die Unterschiede zwischen MFTs und DMOs zusammen.                                                                                                                                                   |
| [Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)                         | Richtlinien zum Schreiben eines benutzerdefinierten MFT.                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Pipeline](media-foundation-pipeline.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> <dt>

[**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




