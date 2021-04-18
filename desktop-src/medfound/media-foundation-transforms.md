---
description: Media Foundation Transformationen
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Media Foundation Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361126"
---
# <a name="media-foundation-transforms"></a>Media Foundation Transformationen

Media Foundation Transformationen (MFTs) stellen ein generisches Modell zum Verarbeiten von Mediendaten bereit. MFTs werden für Decoders, Encoder und digitale Signalprozessoren (DSPs) verwendet. Kurz gesagt: alles, was sich in der Medien Pipeline zwischen der Medienquelle und der Medien Senke befindet, ist eine MFT.

In diesem Abschnitt werden das MFT-Programmiermodell und die Implementierung von MFT beschrieben, mit Empfehlungen für bestimmte Typen von MFTs, wie z. b. Decoders.



| Thema                                                                    | BESCHREIBUNG                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu MFTs](about-mfts.md)                                             | Bietet eine kurze Übersicht über MFTs                                                                                                                                                                   |
| [Einfaches MFT-Verarbeitungsmodell](basic-mft-processing-model.md)             | Beschreibt das grundlegende Modell für die Verarbeitung von Daten mit einem MFT ausführlicher.                                                                                                                           |
| [Asynchrone MFTs](asynchronous-mfts.md)                               | Beschreibt ein asynchrones Verarbeitungsmodell, das eine Alternative zum grundlegenden Modell ist.<br/> Die asynchrone Verarbeitung wurde in Windows 7 eingeführt. Nicht jedes MFT unterstützt dieses Modell.<br/> |
| [Registrieren und Auflisten von MFTs](registering-and-enumerating-mfts.md) | Informationen zum Registrieren eines MFT und zum Aufzählen von MFTs in der Registrierung.                                                                                                                                   |
| [Einschränkungen bei der Verwendung des Felds](field-of-use-restrictions.md)               | Beschreibt den Mechanismus zum Entsperren eines MFT mit Einschränkungen für das Feld.                                                                                                                    |
| [Vergleich von MFTs und DMOs](comparison-of-mfts-and-dmos.md)           | Fasst die Unterschiede zwischen MFTs und DMOS zusammen.                                                                                                                                                   |
| [Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)                         | Richtlinien zum Schreiben einer benutzerdefinierten MFT.                                                                                                                                                                |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Pipeline](media-foundation-pipeline.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> <dt>

[**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




